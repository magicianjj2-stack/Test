graph TD
    %% System Under Development
    SUD["::병원 진료 접수 시스템::\n(User App, Hospital S/W, Kiosk S/W)"]

    %% External Entities
    E1[("모바일 앱 사용자\n(환자/보호자)")]
    E2[("내원 환자\n(현장 방문객)")]
    E3[("의료진\n(의사/간호사)")]
    E4[("병원 관리자")]
    E5[("결제 시스템\n(PG사)")]

    %% Interactions (Multiplicity included in text below)
    E1 -- "I01: 모바일 진료 서비스 이용" --> SUD
    E2 -- "I02: 키오스크 셀프 접수 이용" --> SUD
    E3 -- "I03: 진료 및 대기열 관리 수행" --> SUD
    E4 -- "I04: 시스템 운영 및 통계 관리 수행" --> SUD
    SUD -- "I05: 결제 승인 및 처리 요청" --> E5

    classDef system fill:#f9f,stroke:#333,stroke-width:2px;
    classDef entity fill:#fff,stroke:#333,stroke-width:1px;
    class SUD system;
    class E1,E2,E3,E4,E5 entity;
