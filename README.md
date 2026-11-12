# Colibre — releases

Binary releases only (no source). 다운로드: [최신 릴리스 / latest release](../../releases/latest) — 설치 파일의 SHA256은 릴리스 노트에 있습니다. 실행 전 꼭 확인하세요 / verify it before running.

[한국어](#colibre-소개-0160) · [English](#introducing-colibre-0160)

## Colibre 소개 (0.1.160)

### 한 줄 소개
**Colibre는 내 PC에 설치해 쓰는 개인 스트리밍 프로그램입니다.** 내 PC의 영상·소리·라디오·내 미디어(내 음악/영상 파일), PC 화면(원격 데스크톱), 내비게이션 화면을 차 브라우저와 폰으로 보내 줍니다. 별도의 클라우드·중계 서버 없이 내 PC의 공인 IP로 직접 연결합니다.

### 1. 미디어
- **내 미디어**: PC의 미디어 폴더에 넣어 둔 음악·영상을 폴더째 보여 주고, 폴더 안 이름 검색, 전체 재생, 반복, 셔플, 이어보기를 지원합니다. 파일은 읽기만 하며 지우거나 바꾸지 않습니다. 영상은 MP4·MKV·WebM·MOV를 열고, 기기가 못 푸는 소리는 사본으로 변환해 재생할 수 있습니다(원본은 그대로). 음악은 앨범 정보(MusicBrainz)·표지(Cover Art Archive)·가사(LRCLIB)를 찾아 보여 줍니다(곡 정보 검색어만 해당 서비스로 전달).
- **라디오**: 방송국이 공개한 채널 목록(Radio Browser)을 나라별로 받아 듣습니다. 고음질만·무손실만 걸러 보기, 이름순 정렬, 방송 찾기가 있습니다. Colibre는 목록을 모아 주는 것일 뿐 방송의 소유자나 재배포 주체가 아닙니다.
- **폰 리모컨 + 차 재생**: 폰을 리모컨으로 쓰고 차 브라우저(또는 다른 기기)를 재생 위치로 골라 보냅니다. 이전/다음, 볼륨, 재생 위치 선택, 소리 효과 켜고 끄기가 한 막대에 있습니다. 차가 켜지면 재생 위치를 차로 자동 전환하는 옵션이 있습니다.
- **소리 기능(탑재된 항목만)**: 공간 효과(Spatial), 서라운드, 곡마다 크기 맞춤, 모노 확장, 저음 강화, 5.1·7.1 저음 채널(LFE) 섞기, 레퍼런스(차 실내 저음 보정), AI 음질 복원(AI clean-up), 3D 소리 등을 켜고 끌 수 있고 기기별/전체 기본값으로 저장됩니다. 일부 항목은 (test) 표시가 붙은 시험 기능입니다. 스트림 음질은 와이파이용 32비트 무손실 / LTE·약한 신호용 FLAC 24비트 중에서 고릅니다. 모든 소리 처리는 내 PC에서 하고 차/폰은 켜고 끄기만 합니다.
- **영상 모드 / 조작 모드**: 영상 모드는 소리와 화면을 몇 초 모아 함께 내보내 끊김이 적고 입모양이 맞습니다. 조작 모드는 반응 속도를 우선합니다. 회선이 느려지면 화질이 먼저 내려가고 소리는 끝까지 유지됩니다.
- **주행 안전**: 차가 움직이면 화면에 덮개가 씌워져 터치가 막히고 소리는 계속 나옵니다. 운전자는 주행 중 화면을 보거나 조작하지 말고 소리만 들으세요.

### 2. 원격 (PC 화면 보기·조작)
- 폰 리모컨의 **Colibre** 탭을 누르면 **차 화면에 내 PC 화면**이 뜨고, **폰은 조작판(트랙패드 + 키보드)**이 됩니다. 문자 명령창(터미널)이 아니라 PC 화면 전체를 보고 조작하는 **원격 데스크톱** 방식입니다.
- 입력: 폰 트랙패드(탭·끌기·두 손가락 스크롤·확대/축소 등 노트북 터치패드와 같은 방식), 화면 키보드(천지인), 블루투스 키보드·마우스, 게임패드(PC 쪽 원격 입력 드라이버 설치 시). 게임·에뮬레이터도 쓸 수 있습니다.
- 보안: 접속은 **핀번호(등록 번호) + 비밀번호**로 기기를 등록한 뒤에만 열리고, 로그인 실패가 쌓이면 차단되며, 등록 기기 수 제한과 접속 기록 확인이 있습니다. 통신은 공인 IP용 정식 인증서(Let's Encrypt IP 인증서)로 암호화됩니다. 내 PC 1대·내 차 1대·내 폰 1대용 개인용이며, DRM 보호 영상은 우회하지 않아 검게 보일 수 있습니다.
- 주의: 반응 속도는 폰 성능과 네트워크 상태에 크게 좌우됩니다. PC에 Windows 관리자 권한 창(UAC)이 뜨면 폰 입력이 막혀 PC 앞에서 직접 눌러야 합니다. PC 화면 보기·조작은 NVIDIA GeForce 그래픽카드가 필요합니다.
- 내비게이션: 지도·내 위치·단속카메라 알림(베타, 실제와 다를 수 있음)을 보여 줍니다. 위치는 내 PC와 차 브라우저 안에서만 쓰고 개발자 서버로 보내지 않습니다.

### 3. 장점
- **내 PC + 내 공인 IP 직접 연결**: 클라우드·중계 서버를 거치지 않습니다. 설정·로그인·미디어·위치 정보는 내 PC에 남습니다.
- **개발자 서버로 나가는 정보는 최소**: 핀번호 발급, 연결 확인, 업데이트 확인, 지도 자료 확인, 이용권 확인에 필요한 정보뿐이며 전부 개인정보처리방침에 적혀 있습니다. 분석·광고·추적 도구는 쓰지 않습니다.
- **모든 소리 처리는 내 PC 엔진에서** 하므로 폰·차 브라우저가 달라도 같은 소리입니다(클라이언트는 켜고 끄기만).
- **최소화에도 소리가 이어지도록 설계**: 영상 모드에서는 차 브라우저를 최소화해도 소리가 계속 나오게 만들었습니다(조작 모드는 멈출 수 있음).
- 업데이트해도 등록한 기기는 지워지지 않습니다.

### 4. 사용 환경과 설치
- 64비트 Windows 10/11 PC(사용 중 켜 둠). PC 화면 보기·조작은 NVIDIA GeForce 그래픽카드 필요. 집 밖에서 쓰려면 공인 IP와, TCP 443을 PC로 넘길 수 있는 공유기(포트포워딩)가 필요합니다.
- 설치 파일은 **코드 서명이 없어** Windows SmartScreen 경고가 뜹니다. "추가 정보 → 실행"을 누르고, 먼저 릴리스 노트의 SHA256으로 파일을 확인하세요. 공식 다운로드는 https://github.com/sangre72/colibre-releases/releases/latest 하나뿐입니다. 자세한 설치 순서는 릴리스 노트를 보세요.

### 5. 체험·이용권
- **첫 실행일부터 10일 무료 체험**: 모든 기능을 쓸 수 있고, 끝나면 라디오를 뺀 재생이 멈춥니다.
- 체험 후에는 지원 메일로 이용권을 요청해 주세요. 요청 순서대로 보내 드리며 시간이 걸릴 수 있습니다(후원 여부와 관계없음). 아직 사업 등록·인증 전이라 이용권을 팔지 않고, 당분간 후원으로만 운영합니다(후원은 자발적 응원이며 대가가 없습니다). 이 버전에는 가격 안내가 없습니다.
- **테슬라 연동**: 개발 완료, 서비스 제공 가능 확인 및 필요한 절차 후 공개 예정, 현재 버전 미제공.

## Introducing Colibre (0.1.160)

### In one line
**Colibre is a personal streaming program you install on your own PC.** It sends your PC's video, sound, radio, your own media files, the PC screen (remote desktop) and a navigation screen to your car browser and phone. There is no cloud or relay server: devices connect straight to your PC's public IP.

### 1. Media
- **My Media**: shows the music and video in your PC's media folder, folder by folder, with in-folder name search, play all, repeat, shuffle and resume. Files are read-only; Colibre never deletes or changes them. Video opens as MP4, MKV, WebM or MOV; audio the device cannot decode can be converted to a copy (the original is untouched). For music it looks up album info (MusicBrainz), cover art (Cover Art Archive) and lyrics (LRCLIB); only the artist/title search terms go to those services.
- **Radio**: downloads the public station lists (Radio Browser) by country. Filters (high quality only, lossless only), name sort and station search. Colibre only collects public channel lists; it does not own or redistribute broadcasts.
- **Phone remote + car playback**: use the phone as a remote and pick the car browser (or another device) as the player. One bar holds previous/next, volume, player choice and effects on/off. An option switches playback to the car when the car turns on.
- **Sound features (as shipped)**: Spatial, Surround, even volume across tracks, widen mono, bass boost, mixing the 5.1/7.1 bass channel (LFE) into left/right, Reference (trims cabin-boosted bass), AI clean-up (restores highs cut by compression) and 3D sound, set per device or as a default. Some items are marked (test). Stream quality: 32-bit lossless (Wi-Fi) or FLAC 24-bit (LTE / weak signal). All sound processing runs in the engine on your PC; the phone and car only toggle it.
- **Video mode / control mode**: video mode buffers sound and picture for a few seconds and sends them together, for fewer stalls and matched lip-sync. Control mode favours responsiveness. On a slow link, picture quality drops first and sound is kept to the end.
- **Driving safety**: when the car moves, a cover blocks touch on the screen and sound keeps playing. Drivers must not watch or operate the screen while driving; listen only.

### 2. Remote (view and control your PC)
- The **Colibre** tab on the phone remote opens **your PC screen on the car screen**, and **the phone becomes the control pad (trackpad + keyboard)**. This is a full **remote desktop**, not a text terminal.
- Input: phone trackpad (tap, drag, two-finger scroll, pinch, like a laptop touchpad), on-screen keyboard, Bluetooth keyboard and mouse, and game pads (needs the remote-input driver on the PC). Games and emulators work too.
- Security: a device is opened only after registration with a **PIN (registration number) and a password**; repeated failed sign-ins are blocked; there is a device limit and an access history. Traffic is encrypted with a trusted public-IP certificate (Let's Encrypt IP certificate). It is for personal use: your own 1 PC, 1 car, 1 phone. DRM-protected video is not bypassed and may show black.
- Notes: responsiveness depends heavily on the phone and the network. If a Windows administrator (UAC) prompt appears on the PC, phone input is blocked until you click it at the PC. Viewing and controlling the PC screen needs an NVIDIA GeForce graphics card.
- Navigation: shows the map, your position and speed-camera alerts (beta; may differ from reality). Location is used only on your PC and in the car browser and is not sent to the developer's servers.

### 3. Advantages
- **Your PC, your public IP, direct connection**: no cloud or relay. Settings, sign-in details, media and location stay on your PC.
- **Minimal data leaves the PC**: only what PIN issuing, connection checks, update checks, map-data checks and the pass check need, all listed in the Privacy Policy. No analytics, ads or tracking tools.
- **All audio processing in the PC engine**, so the sound is the same on any phone or car browser.
- **Built to keep playing when minimised**: in video mode, sound continues when the car browser is minimised (control mode may go silent).
- Updating does not erase your registered devices.

### 4. Requirements and install
- 64-bit Windows 10/11 PC that stays on. An NVIDIA GeForce card for PC-screen viewing/control. For use away from home: a public IP and a router that can forward TCP 443 to the PC.
- The installer is **not code-signed**, so Windows SmartScreen warns: click **More info → Run anyway**, after checking the file against the SHA256 in the release notes. The only official download is https://github.com/sangre72/colibre-releases/releases/latest. See the release notes for the full steps.

### 5. Trial and pass
- **10-day free trial from first run**: all features work; when it ends, playback other than radio stops.
- After the trial, request a pass by email to support. Passes are sent in order and may take time (regardless of donation). Colibre is not yet business-registered/certified, so it does not sell passes and is run on donations for now (a donation is voluntary and gets nothing in return). This version states no prices.
- **Tesla link**: development is complete; it will be released after availability is confirmed and the necessary procedures are done; not provided in the current version.

- Support: support@colibre.app

## License and legal

Colibre is proprietary, commercial software, licensed (not sold) under the Colibre End-User License Agreement. It is not open source.

- [LICENSE](LICENSE) (English) · [LICENSE.ko](LICENSE.ko) (Korean, governs if the translations differ)
- [THIRD_PARTY_NOTICES.md](THIRD_PARTY_NOTICES.md): open-source components bundled in the installer and their licenses
- Terms of Use: https://colibre.app/global/legal/terms/ (Korean: https://colibre.app/legal/terms/)
- Refund Policy: https://colibre.app/global/legal/refund/ (Korean: https://colibre.app/legal/refund/)
- Privacy Policy: https://colibre.app/global/legal/privacy/ (Korean: https://colibre.app/legal/privacy/)
- Support: support@colibre.app
