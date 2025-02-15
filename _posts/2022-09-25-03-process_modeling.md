---
layout: post
title: "[IT] 프로세스 모델링 이해 03 - 분석 개요"
categories: [Study, IT]
tags: [IT, Process Modeling]
fullview: false
comments: false
---

본 포스팅은 **"프로세스 모델링 이해"** 온라인 강의를 바탕으로 공부한 내용을 정리한 것입니다.

![image](https://user-images.githubusercontent.com/84369912/192108474-596a2b19-9169-4f3a-9249-6c50b5857b8f.png)

---

## 시스템 개발 단계의 스텝

시스템 개발 진행 시
: 분석 -> 기본설계 -> 상세설계 -> 개발 -> 테스트 -> 전개 등의 단계로 진행

---

시스템 개발 단계별 산출물 연관관계도 - 분석

현행 시스템 분석, 요구사항 정의

분석
: 구축 대상 업무 및 시스템에 대해 철저히 분석/이해하여 핵심업무를 선정하는 단계

현행업무 흐름도, 현행프로그램목록, 현행테이블 정의서 등의 산출물

현행시스템 분석 완료 후 요구사항 정의작업

현행시스템의 문제점, 개선사항을 고객 인터뷰나 설문을 통해 수집한 후, 요구사항 정의서에 반영

비즈니스 업무기능에 관한 요구사항은 To-be프로세스 분석 단계에

사용자 인터페이스에 관한 요구사항은 화면정의 단계에

데이터 관련 업무기능에 관한 요구사항은 데이터 분석 단계에

내부/외부 시스템 연계에 대한 요구사항은 인터페이스 정의 단계에 사용

To-Be 프로세스 분석
: 현행시스템을 분석한 내용을 바탕으로 정의된 요구사항을 반영, 개선된 프로세스를 업무기느분해도, 업무흐름도를 통해 기술하는 작업

산출물 업무배경도, 업무기능분해도, 업무흐름도, 통합업무흐름도

화면 정의
: 주요한 화면의 레이아웃 및 입/출력을 정의하여, 고객과의 협의를 통해 요구사항을 구체적으로 확정하는 활동
: 산출물 화면정의서, 메뉴구조도 등

데이터 분석
: 현행시스템에서 분석한 용어/도메인을 조사

데이터 관련 업무기능에 관한 요구사항을 반영하여 엔터티 도출

속성/식별자/관계를 정의하는 활동

산출물 논리ERD, 엔터티 정의서 등

인터페이스 정의
: 요구사항에서 정의된 내부/외부 연계 요구사항과

To-Be 프로세스 분석 단계에서 도출된 업무간 내부/외부 연계를 반영하여

내부 인터페이스 명세서와 외부 인터페이스 명세서를 작성

단계말 검토
: 검토내용을 반영하여 검토결과서 작성, 검토 내용중 발생된 변경사항은 분석 산출물에 재반영

요구사항추적 매트릭스는 요구사항을 추적할 수 있도록 해 주는 문서

분석 시 도출된 요구사항이 설계 단계를 거쳐 구축단계에 어떻게 반영되었는지를 확인 해 주는 지표로 사용

요구사항을 추적하는 ID로는 요구사항ID, 업무기능 ID, 화면 ID 등이 사용

---

# 참고