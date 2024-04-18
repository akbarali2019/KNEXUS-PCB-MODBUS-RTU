# KNEXUS-PCB-MODBUS-RTU
한국환경기계분석연구원㈜ KNEXUS PCB – MODBUS RTU

## 1. 통신
 
1.1 프로토콜 : Modbus-RTU (RS485) 
1.2 Function CODE : 0x04 (Read Input Registers)
1.3 BaudRate : 9600bps (8,N,1) 고정 
1.4 DATA Field 전송방식 : 빅엔디언

![image](https://github.com/akbarali2019/KNEXUS-PCB-MODBUS-RTU/assets/52565814/ab1ee338-b95c-4634-aa03-ec43933baf18)

1.5 데이터 측정
KNEXUS PCB는 아날로그 데이터를 0과 4095의 범위에서 디지털 데이터로 보정한다. 예시, 센서 min과 max 값이 4mA~20mA이면 0은 4mA를 의미하고 4095는 20mA를 의미한다.

1.6 통신포맷

![image](https://github.com/akbarali2019/KNEXUS-PCB-MODBUS-RTU/assets/52565814/18044930-7c75-4052-a7ad-5b3d5887b094)

## 2. KNEXUS PCB 연결도

SlaveID 기준값 = 1 -> (PCB가 Slave으로 하나만 있는 경우)
추가 PCB -> (Slave으로 PCB가 2개 이하 있는 경우 SlaveID가 수동으로 각각 설치해야됨) 

![image](https://github.com/akbarali2019/KNEXUS-PCB-MODBUS-RTU/assets/52565814/91c266e7-5fca-420e-b488-cf5318d5a55b)

# Packet Example

![image](https://github.com/akbarali2019/KNEXUS-PCB-MODBUS-RTU/assets/52565814/7df0b58b-7509-4db0-bec9-f9817411c12f)

# 멀티마스터를 사용하는 경우 장치 연결 방법을 자세히 설명하는 추가 다이어그램

![image](https://github.com/akbarali2019/KNEXUS-PCB-MODBUS-RTU/assets/52565814/6346ba28-db27-4bd6-a889-090a9e28abb3)
