조건문
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

| 특정 상태에 따라 실행하는 코드가 다르게 설정해주는 것이 조건문입니다.
| 예를 들어 '학생 점수가 70점이상이면 A 로 표시하고, 70점 이하면 B 로 표시하라' 라고 설정해주는데 필요한 것이 조건문입니다.
| 레벨2에서는 모든 조건문을 살펴보기보다 주로 많이 사용되는 것들을 위주로 설명합니다.
|

.. image:: ../../images/Lv2/Chapter_6/Step4_1.jpg
   :width: 600
   :align: center

|
| 위 그림에서 :blackbold:`점수 > 70 인가?` 에 해당되는 부분이 조건문에 해당됩니다.
| 아두이노뿐만 아니라 대부분의 프로그래밍 언어에서 조건문은 유사한 방식으로 작동됩니다.
| 이 그림을 코드로 변경하면 다음과 같습니다.

.. image:: ../../images/Lv2/Chapter_6/Step4_2.jpg
   :width: 800
   :align: center

|
| 조건문은 if로 시작합니다. if(조건) 에서 '조건' 부분이 참인지 거짓인지 판단하고, 결과에 따라 실행하는 부분이 다릅니다. else는 '그 밖에, 또 다른' 뜻을 가지고 있기 때문에, 조건이 참이 아닐 경우에 실행됩니다.
| else 부분은 필수가 아니기 때문에 코드에 있어도 되고, 없어도 됩니다.
|
| 아래 코드에서는 a에 어떤 값이 저장될지 생각해보세요.

.. code-block:: c++

   int a;
   int b = 75;
   if( b>70 && b<80)
   {
    a = 100;
   }
   else
   {
    a = 0;
   }

| 정답

.. toggle::

    | a 변수에는 100이 저장되었습니다.

| 또한 코드에서 중괄호는 여러군데 위치할 수 있습니다. 코드의 순서가 바뀌지 않는다면, 위치는 변경되어도 됩니다.
| 아래 코드 모두 같은 기능을 수행합니다.
|

.. image:: ../../images/Lv2/Chapter_6/Step4_3.jpg
   :width: 800
   :align: center

|
| 또한 아래와 같이 조건을 여러개를 설정하고 싶은 경우에도, 조건문을 활용할 수 있습니다.
|

.. image:: ../../images/Lv2/Chapter_6/Step4_4.jpg
   :width: 600
   :align: center

|
| 2개의 조건문을 사용하여, 조건에 따라 A, B, C를 구별할 수 있게 합니다. 이런 구조를 코드로 나타내면 다음과 같습니다.
|

.. image:: ../../images/Lv2/Chapter_6/Step4_5.jpg
   :width: 800
   :align: center

|
| 위와 같은 형식으로 조건이 2개뿐만 아니라 else if(조건)의 형태로 여러개의 조건들을 이어서 구성할 수 있습니다.
|
| 아래 코드에서는 a에 어떤 값이 저장될지 생각해보세요.

.. code-block:: c++

    char a;
    int b = 50;
    if(b>70)
    {
        a = 'A';
    }
    else if(b>60)
    {
        a = 'B';
    }
    else if(b>50)
    {
        a = 'C';
    }
    else
    {
        a = 'D';
    }

| 정답

.. toggle::

    | a 변수에는 문자 D가 저장되었습니다.
    | ' ' 기호는 문자임을 표시해주는 것 임으로 저장할 때는 함께 저장되지 않습니다.