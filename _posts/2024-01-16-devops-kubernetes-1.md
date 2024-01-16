---
title: '[Kubernetes] 쿠버네티스 공부 #1'
excerpt: ''

categories:
  - devops
tags:
  - [devops]
  - [kubernetes]

permalink: /devops/kubernetes/

toc: true
toc_sticky: true

date: 2024-01-16
last_modified_at: 2024-01-16
---

## 가상머신과 컨테이너차이

컨테이너는 호스트 운영 체제에서 애플리케이션을 실행하기 위해 격리된 경량 사일로이다.
컨테이너는 마치 호스트 운영체제에 매립된 배관처럼 호스트 운영 체제의 커널 위에 빌드된다.

컨테이너와 달리, VM은 자체 커널을 포함한 완전한 운영체제를 실행한다.

참고 - https://learn.microsoft.com/ko-kr/virtualization/windowscontainers/about/containers-vs-vm

## 쿠버네티스가 필요한 이유

컨테이너 개발 시대 : 컨테이너는 VM과 유사하지만 격리 속성을 완화하여 애플리케이션 간에 운영체제(OS)를 공유한다.
그러므로 컨테이너는 가볍다고 여겨진다. VM과 마찬가지로 컨테이너에는 자체 파일시스템, CPU 점유율, 메모리, 프로세스 공간 등이 있다.
기본 인프라와의 종속성을 끊었기 때문에, 클라우드나 OS 배포본에 모두 이식할 수 있다.

컨테이너는 애플리케이션을 포장하고 실행하는 좋은 방법이다. 프로덕션 환경에서는 애플리케이션을 실행하는 컨테이너를 관리하고
가동중지 시간이 없는지 확인해야 한다. 예를 들어 컨테이너가 다운되면 다른 컨테이너를 다시 시작해야 한다.
이러한 문제들을 시스템을 통해 처리 한다면 더 쉽게 처리 할 수 있을 것이다.

참고 - https://kubernetes.io/ko/docs/concepts/overview/
