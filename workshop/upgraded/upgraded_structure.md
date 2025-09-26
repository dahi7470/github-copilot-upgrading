# upgraded 디렉터리 구조 및 설명

`upgraded` 폴더는 레거시 프로젝트의 모든 주요 파일과 폴더를 최신 Python 환경에 맞게 복사 및 재구성한 디렉터리입니다.

## 최상위 파일
- `MANIFEST.in`: 패키징 시 포함할 파일 목록을 정의합니다.
- `README.rst`: 프로젝트 설명서입니다.
- `distribute_setup.py`, `distribute-0.6.10.tar.gz`: 레거시 배포 도구 관련 파일(최신 환경에서는 사용하지 않음).
- `setup.py`: 프로젝트 설치 및 패키징 스크립트(최신 환경에서는 pyproject.toml 사용 권장).

## docs (문서 폴더)
- `Makefile`: Sphinx 문서 빌드용 Makefile
- `build/`: Sphinx 빌드 결과물 저장 폴더
  - `doctrees/`, `html/`, `_sources/`, `_static/`: Sphinx 내부 빌드 구조
- `source/`: Sphinx 문서 소스
  - `changelog.rst`, `conf.py`, `example_usage.rst`, `getting_started.rst`, `index.rst`, `other_uses.rst`, `_static/`

## guachi (애플리케이션 코드)
- `__init__.py`: guachi 패키지 초기화 파일
- `config.py`: 설정 관련 모듈
- `database.py`: 데이터베이스 관련 모듈
- `tests/`: 테스트 코드
  - `test_configmapper.py`, `test_configurations.py`, `test_database.py`, `test_integration.py`

## guachi.egg-info (패키지 메타 정보)
- `PKG-INFO`: 패키지 정보
- `SOURCES.txt`: 소스 파일 목록
- `dependency_links.txt`: 의존성 링크
- `top_level.txt`: 최상위 패키지 정보

---

이 구조는 레거시 프로젝트의 모든 주요 파일을 최신 환경에서 관리하기 쉽게 복사한 것입니다. 각 폴더와 파일은 원래의 역할을 유지하며, 필요에 따라 최신 Python 문법 및 패키징 방식으로 점진적으로 업그레이드할 수 있습니다.
