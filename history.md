# AICP Revivo 개발·연구 히스토리

차량 파손 분석을 위한 데이터 수집 도구, AI 학습·추론 코드, 웹 화면, 연구 산출물을 날짜와 분야별로 정리한 기록이다. 개발 날짜를 확인할 수 없는 소스는 현재 구현 현황으로 별도 정리했다.

## 1. 기록 기준

- **기록일:** 소스 변경 이력에 남은 날짜
- **문서 기재 기간:** 기존 산출물에 적힌 수행기간·기준일이며, 기록일과 별도로 정리
- **날짜 미확정:** 기능과 현재 상태만 기록
- **확인 범위:** 소스와 문서를 검토

## 2. 날짜별 주요 변경 이력

연관된 변경은 하나의 작업으로 묶어 정리했다.

### 2025년 12월 — RGB-D 수집 및 카메라 설정 도구

| 날짜 | 분야 | 프로젝트 | 간략 내용 |
| --- | --- | --- | --- |
| 2025-12-10 | 연구·문서 / Data | aicp_depth_info | 저장소를 만들고 RealSense 깊이 카메라 정보 확인 도구의 목적과 기능을 README에 정리했다. |
| 2025-12-10 | Data / 하드웨어 | aicp_depth_info | D455의 센서 설정 옵션과 스트림 프로파일을 조회해 Markdown으로 내보내는 `depth_config_list.py`와 설정 목록 `config.md`를 등록했다. |
| 2025-12-17 | Data / 웹 API | aicp_depth_data_tool | FastAPI 기반 녹화 시작·중단·상태 조회 서비스를 최초 등록했다. Depth를 Color 좌표계에 정렬하고 RGB·Depth NPY·세션 메타데이터를 저장하는 코드를 포함한다. |
| 2025-12-18 | 연구·문서 / Data | aicp_depth_data_tool | README의 녹화 프레임레이트 설명을 90 FPS에서 60 FPS로 수정했다. |
| 2025-12-18 | Data / 보정 정보 | aicp_depth_info | 설정 내보내기 코드에 영상·모션 내부 파라미터, 스트림 간 외부 파라미터와 depth scale 수집을 추가했다. |
| 2025-12-18 | 웹/UI / AI·Depth | aicp_depth_info | Streamlit RGB·Depth 미리보기와 시작·중단 제어를 추가했다. 입력한 Depth 픽셀의 거리를 XYZ 좌표로 변환해 표시하는 UI를 포함한다. |
| 2025-12-18 | Data / 보정 정보 | aicp_depth_data_tool | 카메라 촬영 설정을 조정하고 세션 메타데이터에 내부·외부 파라미터를 저장하는 코드를 추가했다. |
| 2025-12-18 | 운영·문서 | aicp_depth_data_tool | MIT 라이선스를 독점 소프트웨어 사용 조건으로 교체하고 README 설명을 갱신했다. |

수집 도구의 과거 개선 사항 일부는 현재 작업 폴더의 코드에 반영되어 있지 않다.

### 2026년 4~5월 — 연구 근거와 설계 산출물 정리

| 날짜 | 분야 | 프로젝트 | 간략 내용 |
| --- | --- | --- | --- |
| 2026-04-13 | AI / 연구·문서 | AICP_Research | `RU-46 Defect_Norm_Research/PAPER.md`에 D455·L515 관련 전처리 방법의 문헌 조사표를 등록하고 정리했다. |
| 2026-04-27 | 연구·문서 | AICP_Research | LED 연구 PoC 산출물 6개의 파일 틀을 등록했다. 이 시점의 파일은 내용이 없는 골격이며 본문은 4월 29일에 추가됐다. |
| 2026-04-29 | 하드웨어 / 연구·문서 | AICP_Research | LED 광원 실험 결과서와 PoC 연구보고서에 광원 후보 비교, 촬영 환경, 적용 판단을 정리했다. |
| 2026-04-29 | 웹·시스템 / 연구·문서 | AICP_Research | PoC 기술문서와 데모 산출물에 ANPR/NVR, 차량 세션, 영상 수집, 분석 결과 조회·보고 흐름을 문서화했다. 코드 배포 이력과는 구분한다. |
| 2026-04-29 | AI / Data / 연구·문서 | AICP_Research | 데이터셋·라벨링 산출물과 파손 검출 PoC 성능평가서의 본문을 등록했다. 이번 조사에서는 문서의 성능 수치를 재검증하지 않았다. |
| 2026-04-30 | 하드웨어 | AICP_Research | LED 구조광 타워, 6채널 동기화 카메라, 조립·초기 구동, 하드웨어 결과를 다룬 문서 4개를 등록했다. |
| 2026-04-30 | Data / 수집 환경 | AICP_Research | 수집 장비·현장·차량 세션·저장 규칙·예외 처리 기준을 데이터 수집 계획서에 정리했다. |
| 2026-04-30 | Data / 원시 데이터 | AICP_Research | 원시 영상의 정의, 구축 현황, 품질 검수, 후속 활용 내용을 원시 데이터 구축 결과서에 정리했다. |
| 2026-04-30 | Data / 라벨링 | AICP_Research | 덴트·스크래치의 구분, 바운딩 박스 작성, 제외 대상과 검수 절차를 라벨링 지침서로 등록했다. |
| 2026-04-30 | Data / AI | AICP_Research | 학습·검증 데이터셋의 클래스 구성, 데이터 분할, 라벨 포맷과 품질 관리 현황을 문서화했다. |
| 2026-04-30 | 운영·환경 | AICP_Research | 작업 지침·일정표·연구용 자료의 저장소 관리 규칙을 정리했다. |
| 2026-05-02 | 웹/UI / 환경 | depth_visualizer | Python 프로젝트의 초기 골격을 등록했다. 대시보드 화면 시안의 구현 날짜는 별도 확인이 필요하다. |
| 2026-05-20 | AI / 모델 설계 | AICP_Research | 광원 왜곡 패턴 검출 모델의 대상, RF-DETR·YOLO 비교 계획, 전처리, 학습·검증 절차를 설계서로 등록했다. |
| 2026-05-20 | AI / 모델 설계 | AICP_Research | 미세 스크래치 검출을 위한 ROI·타일링, 라벨 좌표 처리, 학습·평가 기준을 설계서로 등록했다. 모델 성능표는 검증 후 채우는 구조이다. |

### 2026년 10월 — 통합 소개 문서 정리

| 날짜 | 분야 | 프로젝트 | 간략 내용 |
| --- | --- | --- | --- |
| 2026-10-15 | 웹 프로젝트 / 문서 | AICP_Revivo_Web | 저장소와 README를 생성하고 AICP Revivo의 소개 문구를 등록했다. |
| 2026-10-19 | 연구·문서 | AICP_Revivo_Web | Scratch·Depth·Tracking 소개, 실행 방법, API, 배포 안내, 제약과 라이선스를 통합 README에 정리했다. |

이 저장소의 통합 README는 프로젝트 설명 자료이며, 설명에 해당하는 실행 소스와 배포 구성은 현재 폴더에 포함되어 있지 않다.

## 3. 기존 문서·산출물에 남아 있는 날짜

### 문서의 수행기간과 조사 기준일

아래 기간은 **기존 문서에 기재된 날짜**이다. 해당 기간 전체의 실제 수행·완료 여부를 이번 조사에서 재검증하지 않았으며, 변경 기록일은 2절에 별도로 정리했다.

| 문서 기재 기간·기준일 | 분야 | 기록된 작업 범위 | 관련 문서 |
| --- | --- | --- | --- |
| 2025-12-01 ~ 2025-12-20 | 하드웨어 | LED 구조광 타워형 모듈과 6채널 동기화 카메라 시스템 설계 | `Source/AICP_Research/AICP-1 Structured_LED_HW/`의 설계서 2개 |
| 2026-01-01 ~ 2026-01-20 | 하드웨어 | 조립 대상, 광원 구성, 초기 구동 테스트 항목 정리 | 같은 폴더의 `하드웨어 조립 및 초기 구동 테스트 보고서.md` |
| 2026-01-15 ~ 2026-01-31 | 하드웨어 | 구조광·카메라·ANPR/NVR 구성 결과 정리 | 같은 폴더의 `하드웨어 개발 결과서.md` |
| 2026-02-01 ~ 2026-02-28 | Data / 수집 | 현장·장비·저장 규칙과 수집 운영 기준 수립 범위 | `Source/AICP_Research/AICP-2 Acquire_Data/데이터 수집 계획서 및 환경 구축 보고서.md` |
| 2026-03-01 ~ 2026-05-31 | Data / 원시 데이터 | 원시 데이터 구축 범위. 본문 집계 기준일은 2026-04-30이며 이후 누적 갱신을 예정함 | 같은 폴더의 `차량 외관 파손 원시 데이터 구축 결과서.md` |
| 2026-03-01 ~ 2026-03-15 | Data / 라벨링 | 덴트·스크래치 분류와 바운딩 박스 작성 지침 | `Source/AICP_Research/AICP-3 Data_Labeling/손상 유형별 데이터 라벨링 지침서.md` |
| 2026-03-16 ~ 2026-06-30 | Data / AI | 학습·검증 라벨링 데이터셋 구축 범위. 본문 집계 기준일은 2026-04-30 | 같은 폴더의 `AI 학습용 및 검증용 라벨링 데이터셋 구축 결과서.md` |
| 2026-05-01 ~ 2026-06-30 | AI / 모델 설계 | 광원 왜곡·미세 스크래치 모델 설계 범위. 두 문서 기준일은 2026-05-20 | `Source/AICP_Research/AICP-4 Scratch_Detection/` |
| 2026-06-25 기준 | 연구·문서 | 개발·인공지능·산출물의 주간 연구사항 정리본 | `Source/AICP_Research/업로드용/` · 미추적 로컬 문서 |
| 2026-07-14 조사 기준 | AI / 개발환경 | RF-DETR 1.8.3, 학습 API, 평가·예측 구성에 관한 라이브러리 조사 기록 | `10.Detect_Damage/docs/library_research.md` · 미커밋 문서; 구현 완료일은 미확정 |

`Source/AICP_Research/TimeLine.md`는 일정표이며 Git 제외 대상이다. 일정표의 예정일을 완료 실적 날짜로 사용하지 않았다.

### 산출물 내부 기록

소스 커밋이 없어도 결과 파일에 처리 시각이 남아 있는 경우가 있다. 다음 날짜는 파일 내부 값이며, 해당 소스의 작성일이나 현재 재현 성공을 의미하지 않는다.

| 파일 내부 날짜 | 분야 | 확인된 기록 | 근거·범위 |
| --- | --- | --- | --- |
| 2025-12-09 | AI / Depth | 외장 부위·덴트 검출 JSON 8,240건이 남아 있으며, 이 중 6,057건에 null이 아닌 3D 값이 기록되어 있다. | `Source/revivo_depth/result/detections.json` · 시각에 시간대 표기 없음. 파손 고유 개수·정확도 또는 정밀 깊이 검증 수치가 아님 |
| 2026-07-28 | Data / 추출 | BAG 추출 manifest 12개에 처리 완료 상태와 Color·Depth·IR1·IR2 저장 기록이 남아 있다. | `20.Depth_Data/extract/*/*/manifest.json` · 기록된 PNG 참조 12,346개 중 현재 파일은 12,345개로, 참조 파일 1개 누락 |

## 4. 분야별 소스 현황 — 구현 날짜 미확정

다음 항목은 확인일 현재 파일 내용으로 파악한 기능이다. 미커밋 소스 또는 초기 골격 이후의 로컬 파일에 해당하므로 개발·완료 날짜를 부여하지 않았다. 전체 경로는 `40.개발_소스/`를 기준으로 한다. 앞에서 프로젝트·패키지 경로를 명시한 뒤 나열한 파일명은 해당 프로젝트·패키지 기준의 축약 경로이다.

### 웹/UI·백엔드

| 프로젝트 | 간략 내용 | 현재 상태·범위 | 주요 소스 |
| --- | --- | --- | --- |
| Web-Dashboard | 차량번호 입력, 공백·하이픈 정규화, 형식 검증, 대시보드 이동 | FastAPI·Jinja2 소스 확인. 파손 결과 영역은 AI 연동 전 자리표시자 | `Source/Web-Dashboard/main.py`, `templates/vehicle_form.html`, `templates/main.html` |
| NexVi-Dashboard | 로그인·회원가입·대시보드·데이터 탐색·관리자 화면과 보호 라우팅 | React 화면 및 FastAPI 연동 코드 확인. 라이브 영상은 연결 전 시안 | `Source/NexVi-Dashboard/NexVi Dashboard/frontend/src/` |
| NexVi-Dashboard | Supabase 가입·로그인·세션 갱신·프로필 조회와 관리자 확인 | 인증·권한 확인 코드 존재. 외부 인증 서비스 연결과 운영 상태는 미검증 | 같은 프로젝트의 `app/routers/auth.py`, `app/routers/admin.py`, `app/deps.py` |
| NexVi-Dashboard | 디바이스 heartbeat, 카메라·수집 상태·로그 조회 | 디바이스 토큰 검사와 메모리 저장소 코드 존재. 실제 장비 연결 이력은 미확인 | 같은 프로젝트의 `app/routers/device.py`, `app/store.py` |
| NexVi-Dashboard | 시스템 자원 모니터링과 세션 검색·통계 화면 | 시스템 자원은 선택적으로 실측. 세션 목록 전체는 고정 시드 4개이며 추이·수집량·용량 KPI도 시드·임시 값 | 같은 프로젝트의 `app/system_metrics.py`, `app/routers/data.py`, `frontend/src/lib/dashboard.js` |
| NexVi-Dashboard | 선택 세션 파일의 Google Drive 업로드와 진행 상태 조회 | 백그라운드 업로드·상태 조회 코드 확인. 실제 업로드 성공은 미검증 | 같은 프로젝트의 `app/gdrive.py`, `app/routers/data.py` |
| depth_visualizer | DepthStation의 스트림·깊이 렌더링·설정 패널 화면 시안 | `claude_design/`의 미추적 React 시안. 커밋된 초기 Python 골격과 별도 | `Source/depth_visualizer/claude_design/` |

### AI·검출

| 프로젝트 | 간략 내용 | 현재 상태·범위 | 주요 소스 |
| --- | --- | --- | --- |
| Detect_Damage | RF-DETR 검출·인스턴스 분할의 학습·평가·단일 이미지 예측 CLI | 전용 응용 코드 존재. 실제 데이터 전체 학습·GPU 실행 결과는 이번 조사 범위 밖 | `10.Detect_Damage/src/detect_damage/train.py`, `evaluate.py`, `predict.py` |
| Detect_Damage | TOML 설정 검증, 클래스·모드 정합성 검사, COCO·YOLO 데이터셋 사전 검사 | 학습 입력 오류를 확인하는 코드와 테스트 소스 존재 | 같은 패키지의 `config.py`, `train.py`, `10.Detect_Damage/tests/` |
| Detect_Damage | bbox·mask COCO 지표와 F1 계산, JSON·CSV 평가 보고서, 예측 이미지 저장 | 평가·예측 결과 생성 코드 확인. 실제 성능 수치는 별도 실험 근거가 필요 | 같은 패키지의 `evaluate.py`, `predict.py` |
| Detect_Damage | 평가·예측의 공용 추론 설정과 해상도 변경 시 위치 인코딩 설정 유지 | 공용 추론 코드와 관련 테스트 소스 확인 | 같은 패키지의 `inference.py`, `10.Detect_Damage/tests/test_inference.py` |
| revivo_depth | RealSense 스트림과 외장 부위·덴트·스크래치 RF-DETR 모델을 연결하는 Streamlit 코드 | 3개 모델 설정·검출 결과 구조가 존재하는 미커밋 소스. 실시간 성능·가중치 구동은 미검증 | `Source/revivo_depth/main.py` |
| revivo_depth | 덴트 박스의 중심·모서리를 역투영해 치수와 깊이 차이를 근사 계산 | 시제품 계산 코드. RGB·Depth 정합과 비동기 결과의 프레임 대응 한계가 있어 정밀 함몰 깊이 측정으로 확정하지 않음 | `Source/revivo_depth/main.py`의 `calculate_3d_bbox` |

### Data·연구지원·운영

| 프로젝트 | 간략 내용 | 현재 상태·범위 | 주요 소스 |
| --- | --- | --- | --- |
| Depth_Data | BAG의 장치·스트림·해상도·프레임레이트 정보를 조회 | 미커밋 CLI 소스 | `20.Depth_Data/bag_info.py` |
| Depth_Data | Color·Depth·IR 원본 PNG 추출, 프레임 시각·보정 정보·중복·누락 집계를 manifest로 저장 | 원본 데이터 추출 코드. 정렬·깊이 필터링 단계와 구분 | `20.Depth_Data/bag_extract.py` |
| Depth_Data | BAG 일괄 추출, 완료 세션 건너뛰기, 실패 목록 수집 | 단일 BAG 추출 함수를 재사용하는 일괄 처리 코드 | `20.Depth_Data/bag_extract_all.py` |
| Depth_Data | 추출 세션의 RGB·Depth 탐색과 픽셀 깊이값 조회 | FastAPI 시각화 코드. 저장 순번의 프레임 대응이 시간 기반 정합을 보장하지는 않음 | `20.Depth_Data/bag_visualizer.py` |
| Depth_Data | D455 설정·내외부 파라미터·보정 정보 JSON 수집과 macOS 실행환경 구성 | 조회·저장 코드 및 로컬 SDK wheel·설치 안내 존재. 실기 구동은 미검증 | `20.Depth_Data/d455_parameters.py`, `pyproject.toml`, `HOWTOUSE.md`, `vendor/` |
| ResearchNote | Markdown 파일·폴더를 HTML을 거쳐 A4 PDF로 변환하는 CLI | 표·코드 블록, 상대 리소스 경로, 파일별 실패 처리를 포함한 코드 확인 | `Source/ResearchNote/main.py`, `pyproject.toml` |
| NexVi-Dashboard | Supabase 초기 구성 안내와 의존성 보안 감사 워크플로 | 설정·워크플로 파일 존재. Git 원격이 없어 CI 실행·배포 이력은 미확인 | `Source/NexVi-Dashboard/NexVi Dashboard/README.md`, `.github/workflows/security-audit.yml` |
| AICP_Research | 데이터셋 정의·어노테이션 문서 및 주간 연구사항 보관 | `RU-15`는 Git 제외 대상, `업로드용/`은 미추적 상태로 확인 | `Source/AICP_Research/RU-15 Vehicle_Damage_Dataset/`, `Source/AICP_Research/업로드용/` |
