---
lab:
  title: 모델 학습
ms.openlocfilehash: dffa9edda34c599dfbd372fe898ddcf955f6f200
ms.sourcegitcommit: 66d8872bc3d24c2121e225be132b56f4df7920ac
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/12/2022
ms.locfileid: "138597264"
---
# <a name="train-models"></a>모델 학습

기계 학습에서는 주로 애플리케이션에 예측 서비스를 제공하는 데 사용할 수 있는 모델의 학습을 수행합니다. 이 연습에서는 Azure Machine Learning 실험을 사용하여 학습 스크립트를 실행하는 방법과 학습된 모델을 등록하는 방법을 살펴보겠습니다.

## <a name="before-you-start"></a>시작하기 전 주의 사항

*[Azure Machine Learning 작업 영역 만들기](01-create-a-workspace.md)* 연습을 아직 완료하지 않았으면 해당 연습을 완료하여 Azure Machine Learning 작업 영역과 컴퓨팅 인스턴스를 만들고 이 연습에 필요한 Notebook을 복제합니다.

## <a name="open-jupyter"></a>Jupyter 열기

Azure Machine Learning Studio의 **Notebooks** 페이지를 통해 Notebook을 실행할 수도 있지만, *Jupyter* 등의 모든 기능을 갖춘 Notebook 개발 환경을 사용하면 생산성을 더욱 높일 수 있는 경우가 많습니다.

1. [Azure Machine Learning Studio](https://ml.azure.com)에서 작업 영역의 **컴퓨팅** 페이지를 표시하고 **컴퓨팅 인스턴스** 탭에서 컴퓨팅 인스턴스가 아직 실행되고 있지 않으면 인스턴스를 시작합니다.
2. 컴퓨팅 인스턴스가 실행되고 있으면 **Jupyter** 링크를 클릭하여 새 브라우저 탭에서 Jupyter 홈 페이지를 엽니다.

> **팁**: Python을 새로 사용하시겠습니까? [Python 치트 시트](cheat-sheets/dp100-cheat-sheet-python.pdf)를 사용하여 코드를 파악합니다. 기계 학습을 새로운 기능으로 사용하시겠습니까? [기계 학습 개요](cheat-sheets/dp100-cheat-sheet-machine-learning.pdf)를 사용하여 Azure Machine Learning 기계 학습 프로세스 개요의 간소화된 개요를 확인합니다.

## <a name="train-models-using-the-azure-machine-learning-sdk"></a>Azure Machine Learning SDK를 사용하여 모델 학습시키기

이 연습에서는 모델을 학습시키기 위한 코드가 Notebook에서 제공됩니다.

1. Jupyter 홈페이지에서 Notebook 리포지토리를 복제한 **/users/*your-user-name*/mslearn-dp100** 폴더로 이동하고 **모델 학습** Notebook을 엽니다.
2. 그런 다음 각 코드 셀을 차례로 실행하여 Notebook의 메모를 읽습니다.
3. Notebook에서 코드 실행이 완료되면 **파일** 메뉴에서 **닫기 및 중지** 를 클릭하여 Notebook을 닫고 Python 커널을 종료합니다. 그런 후에 모든 Jupyter 브라우저 탭을 닫습니다.

## <a name="clean-up"></a>정리

Azure Machine Learning에서 이 랩을 위한 작업이 완료되었으면 Azure Machine Learning의 **컴퓨팅** 페이지 **컴퓨팅 인스턴스** 탭에서 컴퓨팅 인스턴스를 선택한 다음 **중지** 를 클릭하여 종료합니다. 완료되지 않았다면 다음 랩을 위해 실행 상태로 둡니다.

> **참고**: 컴퓨팅을 중지하면 컴퓨팅 리소스에 대한 구독 요금이 청구되지 않습니다. 그러나 구독에 Azure Machine Learning 작업 영역이 존재하는 동안에는 약간의 데이터 스토리지 요금이 청구됩니다. Azure Machine Learning 탐색을 완료했으면 Azure Machine Learning 작업 영역 및 관련 리소스를 삭제할 수 있습니다. 그러나 이 시리즈의 다른 랩을 완료할 계획인 경우, 먼저 *[Azure Machine Learning 작업 영역 만들기](01-create-a-workspace.md)* 연습을 반복하여 작업 영역을 만들고 환경을 준비해야 하므로 신중히 생각한 후 삭제하는 것이 좋습니다.