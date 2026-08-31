# Software-IoT-based-IDS-Project (IoT-Fender)

> 라즈베리파이 기반 IoT 전용 경량 Flooding 공격 탐지 IDS 소프트웨어

1. 프로젝트 개요
자원이 제한적인 IoT 기기를 보호하기 위해, 네트워크 길목(라즈베리파이 Gateway)에서 ICMP 및 TCP SYN Flooding 공격을 실시간으로 감지하고 대응하는 경량 침입 탐지 시스템(IDS)입니다.

2. 주요 기능
- Packet Parser: 3~4계층 패킷 헤더(IP, ICMP, TCP SYN) 실시간 파싱
- Flooding Detector: 단위 시간당 패킷 수 초과 기반 탐지 로직
- Dashboard: 실시간 트래픽 및 공격 알림 시각화

3. 간단 소프트웨어 문맥 다이어그램

공격자 -> IoT 기기 (수많은 패킷 퍼부음) -> 라즈베리파이 IDS가 패킷 캡쳐 후 검문 -> 차단

외부 엔티티: 공격자, 가상 IoT기기, 관리자
입출력 데이터: ICMP/IP 패킷, 경고 알람 메시지, IP 차단 명령
