부품 리스트
+++++++++++++++++++

DC 모터
^^^^^^^^^^^^

.. image:: ../images/Lv1/Chapter_2/Geared_DC_Motor.png
   :width: 600
   :align: center

|
| DC 모터는 3D 펜에서 재료를 밀어내는 역할을 합니다. 

| DC 모터는 전기를 주면 회전하는 부품으로 아래와 같은 제품에서 많이 사용됩니다.
|
| 1. RC카
| 2. 폰
| 3. 선풍기
|
| 우리가 사용할 DC 모터는 기어가 여러개 같이 부착된 DC 모터입니다. DC 모터 위쪽엔 이빨 모양의 바퀴가 있고, 이 바퀴가 재료를 밀어내는 역할을 합니다.

노즐
^^^^^^^^^^^^

.. image:: ../images/Lv1/Chapter_2/Nozzle.png
   :width: 600
   :align: center

|
| 정확히는 노즐에는 2개의 부품이 있습니다. 
|

.. image:: ../images/Lv1/Chapter_2/Nozzle2.png
   :width: 600
   :align: center

|
| 열선(A)과 온도센서(B)입니다. 열선은 말그대로 온도를 높여주는 역할을 하는 부품이고, 온도센서는 현재온도가 어느 정도인지 측정해주는 역할을 합니다.
| 이 열선으로 온도를 올리면, 필라멘트가 녹으면서 통과할 수 있게 됩니다.
| 온도센서, 열선은 단순히 저항이기 때문에 +, - 의 구분이 없습니다.

디스플레이
^^^^^^^^^^^^

.. image:: ../images/Lv1/Chapter_2/0.91_OLED.jpg
   :width: 400
   :align: center

|
| 디스플레이는 현재 온도, 설정 온도, 속도 등 여러 상태를 보여줄 수 있는 화면 입니다.
| 대각선길이가 0.91인치(2.3114cm)로 0.91 디스플레이라고도 불립니다.
| 레벨 1 에서는 이 디스플레이를 활용, 사용하는것은 다루지 않습니다.

보드 기판
^^^^^^^^^^^^

.. image:: ../images/Lv1/Chapter_2/Board.png
   :width: 600
   :align: center

|
| 보드 기판은 PCB 라고도 불립니다. 이 보드 기판의 역할은 부품을 고정하고, 배선을 단순하게 해주는 것입니다.
| 만일 PCB를 사용하지 않고 배선, 테스트를 하게 되면 아래와 같이 복잡해집니다.
|

.. image:: ../images/Lv1/Chapter_2/BreadBoard.png
   :width: 400
   :align: center
   
|
| 보드 기판에는 여러 부품들이 부착되어 있습니다. 대표적으로 스위치 버튼입니다.
| 스위치 버튼은 DC모터를 시계방향으로 돌릴 것인지, 반시계 방향으로 돌릴 것인지 아니면, 온도를 어느정도로 설정할 것인지 결정하는데 도움을 주는 부품입니다. 스위치는 총 4개이며, 기판에 붙어 있습니다.

.. image:: ../images/Lv1/Chapter_2/Resistance.jpg
   :width: 30%
.. image:: ../images/Lv1/Chapter_2/Push_Switch.jpg
   :width: 30%
.. image:: ../images/Lv1/Chapter_2/Capacitor.jpg
   :width: 30%

| 또한 각종 칩, 저항들이 부착되어 있습니다.

메인 보드
^^^^^^^^^^^^

.. image:: ../images/Lv1/Chapter_2/Arduino_Nano.jpg
   :width: 600
   :align: center

|
| 메인 보드는 아두이노 나노라는 것입니다. 과학, 코딩에 관심이 있었다면, 아두이노라는 말은 들어본 적이 있을 겁니다. 아두이노 나노를 이용하여 코딩을 진행할 것입니다.
| 아두이노 나노에는 디지털 핀이 13번까지 있고, 아날로그 핀이 8개 있습니다. 레벨 1에서는 디지털핀, 아날로그 핀이 있다는 것만 알아두시면 됩니다.