# 도커 쿠버네티스 워크샵

## Contents

### Day 01

1. [도커 실행](01/01.md)
2. [도커 레지스트리](01/02.md)
3. [Dockerfile 작성 및 빌드](01/03.md)
4. [도커 고급실행](01/04.md)
5. [docker-compose](01/05.md)

### Day 02

1. [kubectl 살펴보기](02/01.md)
2. [Pod #1 라벨링](02/02.md)
3. [Pod #2 볼륨](02/02.md#volume-연결)
4. [Pod #2 Config](02/02.md#정보전달)

### Day 03

1. [네트워킹 #1 ClusterIP](03/01.md)
2. [네트워킹 #2 NodePort](03/01.md#nodeport)
3. [네트워킹 #3 LoadBalancer](03/01.md#loadbalancer)
4. [네트워킹 #4 ExternalName](03/01.md#externalname)

### Day 04

1. [ReplicaSet](04/01.md)
2. [Deployment](04/01.md#deployment)
3. [DaemonSet](04/01.md#daemonset)
3. [Job & CronJob](04/01.md#job--cronjob)

### Day 05

1. [helm 패키지 매니저](05/01.md)
2. [원격 레포지토리](05/01.md#원격-레포지토리)
3. [Ingress 라우팅](05/02.md)

### 프로젝트 (Optional)

1. [Wordpress 서비스 만들기](project/01.md)
2. [ML 모델 학습 시키기](project/02.md)


## 실습환경

- OS: ubuntu 18.04
- root user (sudo)
- CPU 2 core / MEM 4G / Disk 50G
- Public IP 권장 (EC2 / GCE / Azure VM)

## 사전지식

- 리눅스 기본 지식이 필요합니다. (ssh, vim, apt, curl 등)
- 간단한 프로그래밍 지식을 요구합니다. 언어는 무관하지만 이 책에서는 파이썬을 주로 다룹니다. 파이썬을 모르시더라도 전반적인 프로그래밍 지식만으로도 충분히 이해할 수 있습니다.
- 간단한 클라우드 지식이 필요합니다.
- `tmux`, `screen`과 같은 터미널 멀티플랙서를 사용하면 편리합니다.

## 클라우드 계정 만들기

준비한 서버가 없다면 다음 클라우드 플랫폼을 이용하여 무료로 서버를 생성하시기 바랍니다.

- `GCP`: https://cloud.google.com/free/
- `AWS`: https://aws.amazon.com/ko/s/dm/landing-page/start-your-free-trial/
- `Azure`: https://azure.microsoft.com/ko-kr/free

## MobaXterm 설치

---

**![참고](02.png) 참고** 윈도우 운영체제 사용자에 한해서 설치합니다. 리눅스나 맥 운영체제를 사용하시는 경우 MobaXterm을 설치할 필요 없이 바로 각 운영체제에서 지원하는 터미널 프로그램을 사용하면 됩니다.

---

리눅스 서버로 접속할 터미널을 윈도우 서버에 설치합니다. `putty` ([https://www.putty.org](https://www.putty.org/)) 등 선호하는 터미널을 사용해도 무방합니다.

1. MobaXterm 다운로드: [https://mobaxterm.mobatek.net/download.html](https://mobaxterm.mobatek.net/download.html)
2. `Home Edition` > `Download now` 클릭
3. `MobaXterm Home Edition (Portable edition)` 다운로드
4. 다운로드 완료된 파일 압축 해제
5. `Session` 버튼 > `SSH` 버튼 클릭
6. Remote host / User 입력
7. (Optional) Advanced SSH settings > Use private key (체크) > PEM키 등록

![[그림 3-3] MobaXterm](01.png)

---

**![참고](02.png) 참고** Remote host와 User는 각각 준비한 서버 정보를 입력합니다.


# 참고자료

### Demo 클러스터
- [Play with k8s](https://labs.play-with-k8s.com/)
- [Playground](https://www.katacoda.com/courses/kubernetes/playground)

### Examples & Tutorials
- [쿠버네티스 공식 튜토리얼](https://kubernetes.io/docs/tutorials/)
- [쿠버네티스 example](https://kubernetesbyexample.com/)

### Books
- [The Kubernetes Book](https://www.amazon.com/Kubernetes-Book-Version-January-2018-ebook/dp/B072TS9ZQZ/ref=sr_1_3?ie=UTF8&qid=1528625195&sr=8-3&keywords=kubernetes&dpID=41SyKBO3UcL&preST=_SX342_QL70_&dpSrc=srch)
- [Designing Distributed System](https://azure.microsoft.com/en-us/resources/designing-distributed-systems/en-us/)

### 읽을거리
- [쿠버네티스란 무엇인가](https://subicura.com/2019/05/19/kubernetes-basic-1.html)
