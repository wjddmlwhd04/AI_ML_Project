# 실제 Colab GPU 실행 화면 5장

2026-11-16 사용자 허용 후 학생용 DB를 Colab 런타임에 업로드했습니다. 실제 Tesla T4에서 전체 실습을 실행하고 화면 5장을 수집했습니다. Random Forest는 CPU, MLP는 CUDA에서 실행했습니다. 도구 보조로 실행했으며 본인 담당 범위와 해석은 학생이 검토해야 합니다.

- [GPU 실행 화면](01_gpu_runtime.png)
- [실제 Colab에서 내려받은 부분 실행 노트북](GPU_runtime_only.ipynb): 설치·함수 정의·GPU 점검까지 실행됐으며 DB 업로드 이후 학습 셀은 미실행입니다.
- [전체 실행 출력 포함 노트북](MAI_SMA_DuckDB_ML_DL_GPU_executed.ipynb): 전체 코드 셀 10개 실행, 오류 0건입니다. 위 부분 실행본 이후 완료한 최종 결과입니다.
- [실제 실행 환경 메타데이터](../../results/colab_gpu/runtime.json): 위 노트북의 실제 출력에서 추출했습니다.
- [Colab 작업 링크](https://colab.research.google.com/drive/1JsHr9P2ydsc4MpW1IKtc8y9HGnyVryno): 공개 공유 여부는 검증 전입니다.

| 파일명 | 캡처할 실제 화면 |
|---|---|
| [01_gpu_runtime.png](01_gpu_runtime.png) | Colab 주소, 런타임 GPU 정보, CUDA 텐서 연산 출력 |
| [02_duckdb_distribution.png](02_duckdb_distribution.png) | DuckDB 조회 건수·라벨 분포 코드와 그래프 |
| [03_ml_confusion_roc.png](03_ml_confusion_roc.png) | Random Forest 코드·지표·confusion matrix·ROC |
| [04_dl_learning_curves.png](04_dl_learning_curves.png) | MLP CUDA device·epoch 로그·학습 곡선 |
| [05_comparison.png](05_comparison.png) | ML/DL 성능표·비교 그래프·해석 |

노트북: [GPU 실습 노트북](../../notebooks/MAI_SMA_DuckDB_ML_DL_GPU.ipynb)

Colab에서 **Runtime → Change runtime type → GPU** 선택 후 전체 실행합니다. 첫 CAPTURE 셀은 GPU가 없으면 중단합니다. 실행한 노트북은 출력이 남아 있는 `.ipynb`로 내려받아 함께 보관하고, 결과 ZIP의 `runtime.json`, `metrics.json`, `training_history.json`, 그래프도 보관합니다. GPU 제공 여부와 유형은 계정·할당 상태에 따라 달라집니다. [Colab 공식 FAQ](https://research.google.com/colaboratory/faq.html)
