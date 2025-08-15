---
name: Skuber Management Platform
tools: [Kubernetes, ClickHouse, SigNoz, OpenTelemetry, Go]
image: 
description: Kubernetes 모니터링 및 운영 통합 플랫폼
---

# Skuber Management Platform

**Kubernetes 모니터링 및 운영 통합 플랫폼**

## 📋 프로젝트 개요

Wondermove에서 개발 중인 대규모 Kubernetes 클러스터 모니터링 및 관리 플랫폼입니다. 
멀티클러스터 환경에서의 통합 관측성과 운영 효율성을 제공합니다.

## 🏗 아키텍처

### 2-Tier 모니터링 구조
- **Agent 클러스터**: 데이터 수집 (flash-cluster-1)
- **Host 클러스터**: 데이터 저장 및 시각화 (common-cluster)

### 핵심 컴포넌트
- **SigNoz**: 통합 관측성 대시보드 (87개+ 그래프)
- **ClickHouse**: 시계열 데이터 저장소
- **OpenTelemetry Collector**: 메트릭/로그/트레이스 수집
- **Grafana**: 커스텀 대시보드

## 🚀 주요 기능

### Infrastructure 모니터링
- **Kubernetes**: 76개 그래프 (Pods, Nodes, Deployments 등)
- **Hosts**: 12개 그래프 (시스템 메트릭)
- **Services**: 11개 그래프 (APM 서비스 모니터링)

### 멀티클러스터 관리
- 5개+ 클러스터 통합 모니터링
- 클러스터별 독립적 데이터 수집
- 중앙 집중식 데이터 저장

## 💡 기술적 성과

### 성능 최적화
- OTel Collector 메모리 사용량 최적화
- 메트릭 수집 파이프라인 처리 성능 개선
- ClickHouse 쿼리 튜닝

### 완전성 달성
- SigNoz UI 87개+ 그래프 100% 데이터 표시
- Infrastructure 모니터링 완전 구현
- 실시간 메트릭 수집 (20-30초 간격)

## 🔧 기술 스택

- **Orchestration**: Kubernetes
- **Database**: ClickHouse (시계열 데이터)
- **Observability**: SigNoz, OpenTelemetry
- **Monitoring**: Grafana, Prometheus
- **Language**: Go (시스템 도구)
- **Networking**: Cilium CNI

## 📊 성과 지표

- **클러스터 수**: 5개+ 통합 관리
- **메트릭 그래프**: 87개+ 완전 구현
- **데이터 수집 주기**: 20-30초 실시간
- **시스템 가용성**: 99.9%+ 목표

---

*현재 진행 중인 프로젝트로, 지속적인 기능 개선과 확장이 이루어지고 있습니다.*