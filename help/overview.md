---
title: ' [!DNL Synoptryx](으)로 AEM Managed Services 환경 모니터링'
description: Adobe에서 모니터링 [!DNL Synoptryx] Managed Services에 대한 개요 [!DNL Experience Manager] Adobe이 모니터링하는 항목, 계정 설정 방법 및 팀에 대한 액세스 방법.
feature: Operations
role: Admin
source-git-commit: e8de2213d91e09da68a8f7014b075f81bd7f07ef
workflow-type: tm+mt
source-wordcount: '618'
ht-degree: 0%

---


# [!DNL Synoptryx]&#x200B;(으)로 AEM Managed Services 환경 모니터링 {#synoptryx-monitoring}

[!DNL Synoptryx]을(를) 사용하면 별도의 모니터링 플랫폼을 설정하지 않고도 팀이 애플리케이션 성능, 인프라 상태 및 최종 사용자 환경을 파악할 수 있습니다.

>[!NOTE]
>
> 이해 당사자와 공유하거나 오프라인에서 검토하는 데 이상적인 전체 AEM Managed Services 가시성 및 모니터링 개요에 대해 [!DNL Synoptryx] 제품 개요 백서를 사용할 수 있습니다.

## 개요 {#overview}

[!DNL Synoptryx]은(는) Adobe의 차세대 가시성 플랫폼으로, 애플리케이션 성능, 인프라 상태 및 통합 모니터링에 대한 통합 가시성을 제공하도록 설계되었습니다. 통합된 단일 환경을 통해 중요한 비즈니스 서비스를 사전 예방적으로 모니터링할 수 있습니다. [!DNL Synoptryx]은(는) APM(응용 프로그램 성능 모니터링), 인프라 모니터링 및 가상 사용자 여정 모니터링을 결합하여 최종 사용자에게 영향을 미치기 전에 문제를 식별하고 해결하는 데 도움이 됩니다. 이 플랫폼은 보다 신속한 근본 원인 분석을 위해 심층적인 트랜잭션 추적, JVM 통찰력, 인프라 원격 분석 및 고급 진단을 제공합니다. 최신 가시성 기술을 기반으로 구축되어 복잡한 엔터프라이즈 환경 전반에 걸쳐 확장 가능하고 안전한 모니터링을 제공합니다. [!DNL Synoptryx]은(는) 확장된 데이터 유지, 풍부한 대시보드 및 지능형 분석을 제공하여 운영 효율성을 지원합니다. [!DNL Adobe IMS]을(를) 통한 원활한 로그인 환경을 통해 보안 액세스 및 거버넌스를 보장합니다. 이 플랫폼은 서비스 신뢰성을 향상시키고, 문제 해결을 가속화하고, 고객 경험을 향상시키도록 설계되었습니다. Adobe의 전략적 가시성 솔루션인 [!DNL Synoptryx]은(는) 관리 서비스 환경 전반에서 모니터링, 자동화 및 운영 통찰력을 제공하기 위한 미래 대비형 기반을 제공합니다.

[!DNL Synoptryx]은(는) Adobe [!DNL Experience Manager] Managed Services에 포함되어 있으므로 별도의 모니터링 플랫폼이나 라이선스가 필요하지 않습니다. Adobe은 표준 서비스의 일부로 환경의 가용성과 성능을 모니터링하며, [!DNL Synoptryx]은(는) 팀이 Adobe [!DNL Experience Manager]&#x200B;(AEM) 애플리케이션 및 지원 인프라의 작동 방식을 이해하는 데 사용할 수 있는 전용 플랫폼입니다.

이 안내서에서는 모니터링되는 항목, [!DNL Synoptryx] 계정의 설정 방법, 일상적인 분석 및 문제 해결에 사용하는 대시보드를 탐색하는 방법에 대해 설명합니다.

## 개요 {#at-a-glance}

AEM Managed Services의 일부로 다음을 받을 수 있습니다.

- **전용 [!DNL Synoptryx] 계정** — 팀에 대한 읽기 전용 액세스 권한으로 Adobe Managed Services에서 프로비저닝하고 감독합니다.
- **심층 AEM 트랜잭션 모니터링** — [!DNL Synoptryx] APM 에이전트는 의미 있는 트랜잭션을 메서드 호출(줄 번호 포함), 외부 종속성 및 저장소 작업까지 추적합니다.
- **통합 애플리케이션 및 인프라 보기** - APM과 호스트 수준 지표를 결합하여 전체적으로 성능을 최적화합니다.

## Adobe에서 [!DNL Synoptryx]&#x200B;(으)로 모니터링하는 항목 {#what-we-monitor}

Adobe은 [!DNL Synoptryx] APM Java 플러그인으로 AEM **작성자** 및 **게시** 계층을 모니터링합니다. 토폴로지의 모든 호스팅 서버는 [!DNL Synoptryx] 인프라 에이전트를 사용하여 모니터링됩니다. 사용자 지정 APM 및 인프라 모니터링은 비프로덕션 및 프로덕션 Managed Services 환경 모두에서 활성화됩니다.

![AEM 작성자, 게시 및 호스팅 서버 전체의 Synoptryx APM 및 인프라 모니터링을 보여 주는 다이어그램](assets/image6.png)

### 계정의 애플리케이션 {#applications-in-your-account}

[!DNL Synoptryx] 계정이 단일 Adobe 마스터 계정에 연결되어 있으며 다음을 포함한 여러 응용 프로그램에서 데이터를 받을 수 있습니다.

- AEM Managed Services 환경당 **작성자** 계층용 APM 응용 프로그램 1개
- AEM Managed Services 환경당 **게시** 계층에 대한 APM 응용 프로그램 1개

각 응용 프로그램에는 자체 라이선스 키가 있습니다. Managed Services 계약 보고서의 모든 토폴로지를 하나의 [!DNL Synoptryx] 계정으로 만듭니다. APM 및 인프라 지표와 이벤트는 최대 **30일** 동안 유지됩니다.

## 및 계정 액세스 {#access}

모니터링 데이터는 Adobe에서 프로비저닝하고 관리하는 [!DNL Synoptryx] 계정에 통합됩니다. 에이전트에서 수집한 모든 APM 및 인프라 지표에 대한 **전체 읽기 전용 액세스**&#x200B;를 받게 됩니다. Adobe Managed Services은 계정에 대한 소유권 및 관리 권한을 유지합니다.

>[!NOTE]
>
> **액세스:** [!DNL Synoptryx]에 액세스하려면 [!DNL Adobe IMS] 프로비전이 필요합니다. 고객 성공 엔지니어(CSE)는 조직에 대한 사용자 액세스를 프로비저닝하고 관리할 수 있습니다.

CSE가 계정을 프로비저닝하면 [synoptryx.adobecqms.net](https://synoptryx.adobecqms.net)에 로그인할 수 있습니다.

## 다음 단계 {#whats-next}

팀이 매일 사용하는 모니터링 대시보드를 계속 진행합니다.

- [APM(응용 프로그램 성능 모니터링)](application-performance-monitoring.md) - AEM 트랜잭션을 추적하고 JVM 동작을 분석하며 외부 서비스를 검사합니다.
- [인프라 모니터링](infrastructure-monitoring.md) - 호스트 수준 시스템, 네트워크, 프로세스 및 저장소 지표를 검토합니다.

