---
title: 온라인 호스팅 지침
permalink: index.html
layout: home
---

# Azure Machine Learning 연습

이 리포지토리에는 Microsoft 과정 [DP-100 *Azure의 데이터 과학 솔루션 디자인 및 구현*](https://docs.microsoft.com/learn/certifications/courses/dp-100t01) 및 이 과정에 해당하는 [Microsoft Learn의 자기 주도적 모듈](https://docs.microsoft.com/learn/paths/build-ai-solutions-with-azure-ml-service/)용 실습 랩 연습이 포함되어 있습니다. 학습 자료와 함께 제공되는 이러한 연습에서는 학습 자료에 설명되어 있는 기술을 사용하여 연습을 진행할 수 있습니다.

이러한 연습을 완료하려면 Microsoft Azure 구독이 필요합니다. 강사가 구독을 제공하지 않은 경우 [https://azure.microsoft.com](https://azure.microsoft.com)에서 등록을 하면 무료 평가판을 받을 수 있습니다.

{% assign labs = site.pages | where_exp:"page", "page.url contains '/Instructions'" %}
| 연습 |
| ------- | 
{% for activity in labs  %}| [{{ activity.lab.title }}]({{ site.github.url }}{{ activity.url }}) |
{% endfor %}
