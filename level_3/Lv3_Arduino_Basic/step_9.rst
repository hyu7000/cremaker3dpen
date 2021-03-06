전처리
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

.. raw:: html

    <style> 
    .orangecircle {color:#ff5300; font-size:20px} 
    .blackcircle {color:black; font-size:20px} 
    .bluecircle {color:#3172f4; font-size:20px}
    .skybluecircle {color:#00FFFF; font-size:20px}
    .yellowcircle {color:#fbbc05; font-size:20px}
    .subtitle {color:black; font-weight:bold; font-size:28px}
    .subtitlesmall {color:black; font-weight:bold; font-size:24px}
    .blackbold {color:black; font-weight:bold;}
    .redbold {color:red; font-weight:bold;}
    </style>

.. role:: orangecircle
.. role:: blackcircle
.. role:: bluecircle
.. role:: skybluecircle
.. role:: yellowcircle
.. role:: subtitle
.. role:: subtitlesmall
.. role:: blackbold
.. role:: redbold

| 아두이노를 업로드하신 경험이 있으시다면, 아두이노를 업로드하기 전에 컴파일을 진행하는 것을 보았을 겁니다.
|

.. image:: ../../images/Lv3/Chapter_5/Step9_1.png
   :width: 500
   :align: center

|
| 컴파일은 보드(아두이노)가 이해할 수 있는 기계어로 변경해주는 것을 의미합니다. 이 컴파일 과정 전에 처리되는 과정이 하나 더 있습니다.
| 말 그대로 :blackbold:`전처리` 과정입니다.
|

.. image:: ../../images/Lv3/Chapter_5/Step9_2.jpg
   :width: 700
   :align: center

|
| 종종 소스 코드에는 #define과 같은 코드가 있습니다. 이 코드들이 전처리문이라고 하는 코드들로, 전처리 과정에서 코드들로 변환이 됩니다. 
| 그렇다면, 전처리문에는 어떤 것들이 있는지 알아봅니다.
|
 
.. image:: ../../images/Lv3/Chapter_5/Step9_3.jpg
   :width: 700
   :align: center

|
| 다양한 전처리문이 있습니다만, 우리는 3D 펜에 사용될만한 코드들만 확인해보면 #include 와 #define 입니다.
| #include는 라이브러리를 포함할 때 사용된다니 그렇다 하고, #define은 사용할만한 이유가 번뜩 생각나지 않으실 겁니다.
| 3D 펜 정도의 프로젝트에서 #define을 사용하면 좋은 예시를 한번 보겠습니다.

.. code-block:: c++
   :linenos:
   
   digitalWrite(13,HIGH);

|
| :hoverxref:`digitalWrite <hoverxref:digitalWrite>` 코드는 디지털 13번 핀 출력을 HIGH 로 출력하도록 하는 함수입니다. 여기에서는 어떤 정보를 얻을 수 있나요?
| 얻을 수 있는 정보는 13번 핀에 HIGH 가 출력된다. 입니다.
| 아래 코드는 전처리문을 포함시켰습니다.
| 

.. code-block:: c++
   :linenos:

   #define LED 13
   
   digitalWrite(LED,HIGH);

|
| 이 코드에서는 하나의 정보를 더 얻어갈 수 있습니다. LED 에 연결된 핀에 HIGH가 출력된다. 라는 정보를 얻을 수 있습니다.
| 여기에서는 한 줄짜리 간단한 코드를 사용하였지만, 몇 백줄, 몇 만줄 코드를 다루게 되면, 이런 작은 습관은 도움이 됩니다.
|

| '아니 그러면 굳이 전처리기를 써야되냐? 아래처럼 하면 안되냐?' 고 묻고 싶으신 분들이 보여주는 코드입니다.
|

.. code-block:: c++
   :linenos:

   int led = 13;
   
   digitalWrite(led,HIGH);

|
| '어떠냐? 같은 정보를 얻어갈 수 있는데, 왜 전처리기를 써야 하냐?' 고 물으실 수 있습니다. 하지만 이런 경우에는 int 자료형 변수가 :hoverxref:`선언 <hoverxref:declaration>` 이 되면, 보드에서 메모리를 차지하게 됩니다.
| 적은 수의 변수 :hoverxref:`선언 <hoverxref:declaration>` 은 문제가 되지 않지만, 많아질 수록 문제가 생길 수 있습니다.
| 전처리문는 컴파일하기전에 전처리되기 때문에 메모리를 차지하지 않게 됩니다.
| 
| 어려운 이야기 였을 수 있지만, 전처리문이 필요없지 않고 잘 쓰면 유용하다고 알아두시면 좋겠습니다. 
|
| 전처리문을 사용할 때는 규칙이 있는데 이 규칙을 지켜서 코드를 작성해야 합니다.
| 
| 1. 전처리문의 끝에는 ; 세미콜론을 붙이지 않음
| 2. 전처리문은 한줄에 하나씩 작성
| 3. 전처리문의 이름은 대문자로 작성해주는 관습이 있음.(전처리문임을 빠르게 인지하기 위함)