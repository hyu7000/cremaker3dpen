반복문
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

| 어떤 조건이 계속 참이면, 특정 코드를 계속해서 반복하게 하는 것이 반복문입니다.
| 구조는 아래 그림과 같습니다.
|

.. image:: ../../images/Lv2/Chapter_6/Step5_1.jpg
   :width: 600
   :align: center

|
| 반복문이 시작되면, 초기값을 설정합니다. 이어서 조건을 확인합니다. 조건이 '참'이면, 코드를 실행하고, 횟수를 증가 시키거나 감소시킵니다. 이어서 다시 조건을 확인하고, 다시 코드를 실행하는 과정을 반복합니다.
| 이후 조건이 '거짓'이 되면, 반복문을 종료합니다.
| 코드로 변경하면 다음과 같습니다.
|

.. image:: ../../images/Lv2/Chapter_6/Step5_2.jpg
   :width: 600
   :align: center

|
| 반복문은 for문이라고도 표시되며, 괄호에는 (초기값 설정;조건;값 증감)으로 구성됩니다. 보통 조건에는 초기값과 관련되어 있습니다. 그림처럼 초기값인 횟수가 5보다 작은 경우에만 반복하게 되어 있습니다. 그리고 코드를 실행하면, 횟수가 1증가 함으로,
| 이 반복문의 경우는 코드를 총 5회까지 반복 실행합니다.
|
| 아래 코드에서는 최종적으로 a에 어떤 값이 저장될지 생각해보세요.
|

.. code-block:: c++

   int a = 0;
   for(int i = 0; i<4 ;i++)
   {
    a = a + i;
   }

| 정답

.. toggle::

    | a 변수에는 6 이 저장되었습니다.

| for 반복문뿐아니라 while 반복문도 있습니다.
| 

.. image:: ../../images/Lv3/Chapter_5/Step5_3.jpg
   :width: 600
   :align: center

|
| for문과 비슷하지만 초기값과 증감이 없습니다. 조건만 맞으면, 무한히 반복하게 됩니다.
| 

.. image:: ../../images/Lv3/Chapter_5/Step5_4.jpg
   :width: 300
   :align: center

|
| while 문은 조건 확인 -> 코드 실행 -> 조건 확인 순서대로 진행됩니다.
| 만일 도중에 break; 가 있으면, while 문은 break; 코드가 있는 지점에서 종료됩니다.
|
| 아래 코드에서는 최종적으로 a에 어떤 값이 저장될지 생각해보세요.
|

.. code-block:: c++

   int a = 0;

   while(true) // 조건 자체가 true 임으로 무한히 반복
   {
      a = a + 2;

      if(a > 5)
      {
         break;
      }
   }

| 정답

.. toggle::

    | a 변수에는 6 이 저장되었습니다.

|
| while 문과 관련된 do ~ while 문도 있지만, 3D 펜을 작동시키는 정도의 수준에서는 사용되지 않기 때문에 설명을 생략합니다.