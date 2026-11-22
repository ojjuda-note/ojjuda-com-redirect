# 오쭈다 아지트 접속 주소

- `https://ojjuda.kr/`은 오락실, `https://ojjuda.com/`과 `https://www.ojjuda.com/`은 공원으로 연결합니다.
- 공원은 `https://ojjuda.kr/world.html?place=park`에서 열립니다. 같은 서비스에서 계정·친구·쪽지·ZU를 함께 씁니다.
- 처음 방문하면 둘러보기로 시작하고, 기존 로그인은 유지합니다. 카드 작성과 게임 한 판 이후의 회원가입 연결은 운영 사이트에서 처리합니다.
- 검색 매개변수와 해시를 보존합니다. 명시한 메뉴와 기존 하위 주소는 그대로 연결하며, 로그인·가입·계정 확인은 공식 계정 화면을 거칩니다.
- JavaScript를 쓸 수 없는 경우에도 새로고침 메타 태그와 바로가기 링크로 공원에 연결합니다.

## 기존 Android 앱 시작 대문 교체 (2026-11-22)

앱 v1의 시작 URL은 설치 시 기록되어 있으며, 오쭈다.kr 웹 서비스 배포만으로 바뀌지 않습니다. `/agit/`, `/park/`, `/pajang/`에 별도 HTML 입장 화면을 두지 않고 각 서비스로 즉시 이동시키는 호환 경로를 제공합니다.

- `https://ojjuda.com/agit/` → `https://ojjuda.kr/world.html?tab=hub`
- `https://ojjuda.com/park/` → `https://ojjuda.kr/world.html?place=park`
- `https://ojjuda.com/pajang/` → `https://ojjuda.kr/features/pajang/`
- 기존 `https://ojjuda.com/`의 공원 자동 이동은 그대로 둡니다.

리다이렉트는 임의 목적지·인증 토큰을 전달하지 않으며 유효한 추천인 UUID만 보존합니다. 비로그인은 도착한 실제 웹 서비스의 로그인 및 이용 권한 규칙을 따릅니다.

이는 도메인이 **이 Pages 저장소를 제공하고 새 파일이 실제로 응답하는 경우에만** 기존 설치 앱의 화면을 변경합니다. 이 경로가 다른 호스팅이나 앱 내 오프라인 자료에서 제공되는 경우 해당 출처를 따로 수정해야 합니다. 신규 Android 앱 버전의 기본 시작 주소 변경은 `ojjuda-note.github.io/ops/android-apps/`에서 별도 관리하며, 서명·Play 업데이트 없이 휴대폰에 적용됐다고 말하지 않습니다.
