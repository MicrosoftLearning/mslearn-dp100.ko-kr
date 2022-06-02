---
lab:
  title: 모델 해석
ms.openlocfilehash: 67c49bac773fe3da774f583729a0f9a9de1b3b44
ms.sourcegitcommit: 18f734eeb1031a9cb69c3b294632efd2e69324ac
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 11/17/2021
ms.locfileid: "137894524"
---
# <a name="interpret-models"></a>모델 해석

기계 학습이 건강, 안전, 경제적 복지 그리고 사람들의 삶의 다른 측면에 영향을 주는 결정에 점점 더 중요해짐에 따라 모델이 예측을 수행하는 방식을 이해할 수 있고 기계 학습 기반 결정의 근거를 설명할 수 있는 것이 중요합니다.

## <a name="before-you-start"></a>시작하기 전 주의 사항

*[Azure Machine Learning 작업 영역 만들기](01-create-a-workspace.md)* 연습을 아직 완료하지 않았으면 해당 연습을 완료하여 Azure Machine Learning 작업 영역과 컴퓨팅 인스턴스를 만들고 이 연습에 필요한 Notebook을 복제합니다.

## <a name="open-jupyter"></a>Jupyter 열기

Azure Machine Learning Studio의 **Notebooks** 페이지를 통해 Notebook을 실행할 수도 있지만, *Jupyter* 등의 모든 기능을 갖춘 Notebook 개발 환경을 사용하면 생산성을 더욱 높일 수 있는 경우가 많습니다.

1. [Azure Machine Learning Studio](https://ml.azure.com)에서 작업 영역의 **컴퓨팅** 페이지를 표시하고 **컴퓨팅 인스턴스** 탭에서 컴퓨팅 인스턴스가 아직 실행되고 있지 않으면 인스턴스를 시작합니다.
2. 컴퓨팅 인스턴스가 실행되고 있으면 **Jupyter** 링크를 클릭하여 새 브라우저 탭에서 Jupyter 홈 페이지를 엽니다.

## <a name="use-the-sdk-to-interpret-models"></a>SDK를 사용하여 모델 해석

이 연습에서는 모델 해석을 위한 코드가 Notebook에서 제공됩니다.

1. Jupyter 홈페이지에서 Notebook 리포지토리를 복제한 **/users/*your-user-name*/mslearn-dp100** 폴더로 이동하여 **Interpret Models** Notebook을 엽니다.
2. 그런 다음 각 코드 셀을 차례로 실행하여 Notebook의 메모를 읽습니다.
3. Notebook에서 코드 실행이 완료되면 **파일** 메뉴에서 **닫기 및 중지** 를 클릭하여 Notebook을 닫고 Python 커널을 종료합니다. 그런 후에 모든 Jupyter 브라우저 탭을 닫습니다.

## <a name="clean-up"></a>정리

Azure Machine Learning에서 이 랩을 위한 작업이 완료되었으면 Azure Machine Learning의 **컴퓨팅** 페이지 **컴퓨팅 인스턴스** 탭에서 컴퓨팅 인스턴스를 선택한 다음 **중지** 를 클릭하여 종료합니다. 완료되지 않았다면 다음 랩을 위해 실행 상태로 둡니다.

> **참고**: 컴퓨팅을 중지하면 컴퓨팅 리소스에 대한 구독 요금이 청구되지 않습니다. 그러나 구독에 Azure Machine Learning 작업 영역이 존재하는 동안에는 약간의 데이터 스토리지 요금이 청구됩니다. Azure Machine Learning 탐색을 완료했으면 Azure Machine Learning 작업 영역 및 관련 리소스를 삭제할 수 있습니다. 그러나 이 시리즈의 다른 랩을 완료할 계획인 경우, 먼저 *[Azure Machine Learning 작업 영역 만들기](01-create-a-workspace.md)* 연습을 반복하여 작업 영역을 만들고 환경을 준비해야 하므로 신중히 생각한 후 삭제하는 것이 좋습니다.