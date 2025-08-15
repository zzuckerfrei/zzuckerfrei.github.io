---
name: Skuber Management Platform
tools: [Kubernetes, ClickHouse, SigNoz, OpenTelemetry, Go]
image: 
description: Kubernetes 멀티클러스터 모니터링 및 관측성 플랫폼
---

# Skuber Management Platform

**Kubernetes 멀티클러스터 모니터링 및 관측성 플랫폼**

## 🎯 Overview

Wondermove에서 개발 중인 대규모 Kubernetes 환경을 위한 통합 모니터링 플랫폼입니다. 
멀티클러스터 환경에서 중앙 집중식 관측성과 운영 효율성을 제공합니다.

## 🏗 Architecture

**2-Tier Monitoring Structure**
- **Agent Clusters**: 각 클러스터에서 데이터 수집
- **Host Cluster**: 중앙 집중식 데이터 저장 및 시각화

## 🚀 Key Features

- **87개+ SigNoz 그래프** 완전 구현
- **5개+ 클러스터** 통합 관리
- **실시간 메트릭 수집** (20-30초 간격)
- **ClickHouse 기반** 대용량 시계열 데이터 처리

## 🔧 Tech Stack

- **Platform**: Kubernetes, Docker
- **Database**: ClickHouse (time-series data)
- **Observability**: SigNoz, OpenTelemetry
- **Language**: Go (system tools)
- **Network**: Cilium CNI

## 📊 Results

- 멀티클러스터 환경에서 **99.9%+ 가용성** 달성
- 대용량 메트릭 데이터 **실시간 처리** 구현
- **Infrastructure 모니터링** 완전 자동화

---

*지속적인 기능 개선과 확장을 통해 플랫폼 안정성을 높이고 있습니다.*