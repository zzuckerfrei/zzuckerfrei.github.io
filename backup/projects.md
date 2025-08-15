---
layout: page
permalink: /projects/
title: 프로젝트
---

# 프로젝트

## 🚀 주요 프로젝트

### **Skuber Management Platform**

*Kubernetes 모니터링 및 운영 통합 플랫폼*

#### 📋 프로젝트 개요

**Wondermove**에서 개발 중인 엔터프라이즈급 Kubernetes 모니터링 및 운영 플랫폼입니다. 복잡한 멀티클러스터 환경에서 일관된 관측성과 운영 효율성을 제공합니다.

#### 🏗 아키텍처 특징

- **2-Tier 모니터링 구조**
   - **Agent 클러스터**: 각 운영 클러스터에서 데이터 수집
   - **Host 클러스터**: 중앙집중식 데이터 저장소 및 분석
   - **확장성**: 추가 클러스터 연결 시 Agent만 추가하는 구조

#### 🛠 기술 스택

- **수집**: OpenTelemetry Collector (DaemonSet + Deployment)
- **저장**: ClickHouse (시계열 데이터)
- **시각화**: SigNoz, Grafana
- **오케스트레이션**: Kubernetes, Helm
- **네트워킹**: OTLP (4317 포트)

#### 🎯 핵심 기능

##### **완전한 관측성**

- **Infrastructure 모니터링**: 87개+ SigNoz 그래프 지원
   - Kubernetes: 76개 그래프 (Pods, Nodes, Deployments, etc.)
   - Hosts: 12개 그래프 (시스템 메트릭)
   - Services: 11개 그래프 (APM)

- **실시간 메트릭 수집**: kubeletstats, hostmetrics, kube-state-metrics
- **로그 집중화**: 모든 파드 로그 수집 및 분석
- **분산 트레이싱**: Beyla eBPF 기반 자동 트레이스

##### **성능 최적화**

- **쿼리 성능**: ClickHouse 쿼리 튜닝 및 최적화
- **메모리 효율성**: OTel Collector 메모리 사용량 최적화
- **처리량**: 메트릭 수집 파이프라인 성능 개선
- **네트워크 효율성**: 배치 처리 및 압축을 통한 전송 최적화

##### **운영 자동화**

- **자동 배포**: Helm Charts 기반 원클릭 배포
- **헬스체크**: 자동 장애 감지 및 복구
- **스케일링**: 부하에 따른 자동 확장/축소
- **백업**: ClickHouse 데이터 자동 백업

#### 📊 성과 지표

- **모니터링 대상**: 5개+ 클러스터 통합 관리
- **메트릭 처리량**: 대용량 시계열 데이터 실시간 처리
- **대시보드 응답성**: 빠른 쿼리 응답 및 시각화
- **시스템 안정성**: 높은 가용성과 안정적 운영

#### 🔧 기술적 도전과 해결

##### **Challenge 1: 네임스페이스 필터링**

**문제**: SigNoz Infrastructure 메뉴에서 네임스페이스 필터가 작동하지 않는 이슈
**해결**:

- OTel Collector 설정 최적화로 메트릭 라벨링 개선
- ClickHouse 쿼리 최적화를 통한 정확한 필터링 구현
- 메트릭 파이프라인 보완으로 데이터 정제

##### **Challenge 2: 대용량 데이터 처리**

**문제**: TB 단위 시계열 데이터의 실시간 처리 및 효율적 저장
**해결**:

- ClickHouse 테이블 구조 최적화 (파티셔닝, 압축)
- 집계 함수 활용 (`sumMerge`, `avgMerge` 등)
- 인덱싱 전략 및 쿼리 패턴 개선

##### **Challenge 3: 멀티클러스터 네트워크**

**문제**: 클러스터 간 네트워크 연결 및 보안
**해결**:

- LoadBalancer를 통한 안전한 OTLP 엔드포인트 노출
- VPN 기반 클러스터 간 통신
- 인증서 기반 보안 연결

#### 🌐 데모 & 링크

- **라이브 데모**: [https://skuber.wondermove.net/](https://skuber.wondermove.net/)
- **회사 정보**: [Wondermove](https://wondermove.com)

---

## 🔨 기술 실험 및 오픈소스

- ??

---

## 📈 향후 계획

### **단기 목표 (3-6개월)**

- ???

### **장기 비전 (1-2년)**

- ???

---

*프로젝트에 대해 더 자세히 알고 싶으시거나 협업을 원하신다면 언제든 [연락](/contact/)해주세요!* 📧