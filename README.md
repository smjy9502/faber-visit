# FABER LINKS

회사 소개와 공식 채널 4개를 안내하는 독립적인 정적 1페이지입니다. HTML/CSS, 제공된 원본 PNG, 로컬 SVG 아이콘을 사용합니다. JavaScript, 외부 폰트, CDN, 분석 도구, npm 패키지, 빌드 과정은 없습니다.

## 로컬 실행

현재 macOS 기본 Python 실행기는 Xcode 라이브러리 오류가 있어, 설치되어 있는 Python 3.12.14를 사용합니다. 추가 설치나 시스템 변경은 필요하지 않습니다.

```sh
cd /Users/smkim/dev/faber-links
/Users/smkim/.cache/codex-runtimes/codex-primary-runtime/dependencies/python/bin/python3 -m http.server 8765 --bind 127.0.0.1 --directory public
```

접속 URL: http://127.0.0.1:8765/

이미 사용 중인 포트라면 다른 빈 포트를 지정하고 URL도 변경하세요. 기존 프로세스를 종료하지 마세요. 서버 종료는 실행 터미널에서 Ctrl+C입니다. 정상 동작하는 Python 3가 있다면 실행 파일 경로를 해당 경로로 바꿀 수 있습니다.

## 구성

- `public/index.html`: 소개, 로고, 공식 채널 링크, 접근성 정보
- `public/styles.css`: 모바일 우선 레이아웃, 버튼, 키보드 포커스
- `public/assets/faber-logo.png`: 제공된 1264×304 투명 PNG의 수정 없는 복사본

링크는 새 탭으로 열리며 보조기술에도 이를 안내합니다. 배경 흐림 미지원 시에도 밝은 배경을 제공합니다. 애니메이션은 사용하지 않습니다.

## 작업 범위

정적 페이지 완성본은 https://github.com/smjy9502/faber-visit 의 main 브랜치에 기록합니다. 원격의 기존 LICENSE와 초기 커밋 이력을 보존합니다. Firebase 현황은 읽기 전용으로 확인하며 사이트 생성·설정 파일 생성·target 연결·배포는 별도 승인 후 진행합니다. 기존 faber-home 및 faber-sam-server 저장소와 운영 서비스는 작업 대상이 아닙니다.

## 아이콘 출처와 사용 지침 (2026-10-24 확인)

- Instagram: [Meta 공식 브랜드 자료 및 지침](https://www.meta.com/brand/resources/instagram/instagram-brand/). 공식 `IG_brand_asset_pack_2023.zip` → `01 Static Glyph/03 Black Glyph/Instagram_Glyph_Black.svg`를 `public/assets/instagram.svg`에 바이트 변경 없이 복사했습니다. 공식 검정 단색을 유지하며 재색상·변형·필터를 적용하지 않습니다. FABER보다 두드러지게 표시하거나 제휴·보증을 암시하지 않습니다. 공식 페이지에서 연결된 [상세 Brand Elements 링크](https://www.facebook.com/brand/resources/instagram/icons)는 확인 시 빈 화면/실패하여 상세 페이지의 별도 크기 규칙을 검증하지 못했습니다.
- Threads: [Meta 공식 브랜드 자료 및 지침](https://www.meta.com/brand/resources/threads/). 공식 `Threads-Brand-Resource-Center.zip` → `02 Black/Logo/threads-logo-black.svg`를 `public/assets/threads.svg`에 바이트 변경 없이 복사했습니다. 공식 검정 단색과 원본 비율을 유지합니다. 아이콘 폭의 1/4 이상 여백을 확보합니다(표시 영역 20px, 이름과 간격 10px). 워드마크 조합은 사용하지 않습니다.
- Homepage / Store: 이 페이지용으로 작성한 단순 선 SVG. `viewBox="0 0 24 24"`, 동일한 1.65 선 굵기와 둥근 모서리를 사용합니다. 브랜드 로고가 아닙니다.
- 모든 SVG를 XML로 점검하여 script, 이벤트 속성, foreignObject, 외부 이미지·참조 및 URL 참조가 없음을 확인했습니다. 장식 이미지는 빈 alt와 aria-hidden으로 링크 이름에 중복 낭독되지 않게 했습니다.
- 공식 검정 로고는 웜블랙 텍스트와 가까운 톤이지만 정확한 원본 검정색을 우선합니다. 로고 파일은 런타임에 외부 서버를 요청하지 않습니다.

## 유리 버튼

변경 전 Chrome 계산 스타일은 흰색 불투명도 65%, backdrop-filter blur(12px)였습니다. 배경 변화가 작아 화면에서는 흰 카드에 가까웠습니다. 흰색 기본 레이어를 28%로 낮추고 약한 표면 그라데이션, 밝은 테두리·내부 하이라이트, 버튼 뒤의 작은 오렌지·웜그레이 명암 차이를 적용했습니다. blur는 버튼 4개에만 적용하고 Safari용 -webkit-backdrop-filter를 유지합니다. 미지원 환경의 기본 배경은 #fcfaf7입니다. 중첩 blur나 애니메이션은 없습니다.

## 저장소와 자산

원격 저장소는 public이므로 추적된 코드·자산이 공개됩니다. 기존 Apache-2.0 LICENSE를 그대로 보존하며, Faber 및 Meta 브랜드 자산의 상표·사용 조건은 각 권리자의 지침을 따릅니다. 환경 변수, 인증 파일, 로그·캐시 및 임시 검증 산출물은 기록하지 않습니다.
