---
title: 온라인 호스팅 지침
permalink: index.html
layout: home
ms.openlocfilehash: a2eb157b1d188655f4cfbcc575befec4a2e9c623
ms.sourcegitcommit: 18f734eeb1031a9cb69c3b294632efd2e69324ac
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/17/2021
ms.locfileid: "137894587"
---
# <a name="azure-machine-learning-exercises"></a>Azure Machine Learning 연습

이 리포지토리에는 Microsoft 과정 [DP-100 Azure의 데이터 과학 솔루션 디자인 및 구현](https://docs.microsoft.com/learn/certifications/courses/dp-100t01) 및 이 과정에 해당하는 [Microsoft Learn의 자기 주도적 모듈](https://docs.microsoft.com/learn/paths/build-ai-solutions-with-azure-ml-service/)용 실습 랩 연습이 포함되어 있습니다. 연습은 학습 자료와 함께 진행할 수 있으며, 설명되어 있는 기술을 사용하여 연습할 수 있게 도와줍니다.

이러한 연습을 완료하려면 Microsoft Azure 구독이 필요합니다. 강사가 Microsoft Azure 구독을 제공하지 않은 경우 [https://azure.microsoft.com](https://azure.microsoft.com)에서 무료 평가판에 등록할 수 있습니다.

{% assign labs = site.pages | where_exp:"page", "page.url contains '/instructions'" %}
| 연습 |
| ------- | 
{% for activity in labs  %}| [{{ activity.lab.title }}]({{ site.github.url }}{{ activity.url }}) |
{% endfor %}
