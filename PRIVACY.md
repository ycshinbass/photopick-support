# Photopick Beta 개인정보처리방침 · Privacy Policy

적용 버전:2.17.4 beta / Updated:2026-11-17
프로젝트:Photopick (ycshinbass)
문의 / Contact: ycshinbass@gmail.com
지원 / Support: https://ycshinbass.github.io/photopick-support/support.html
공식 사이트 / Official site: https://photopick.tistory.com/

## 한국어

Photopick은 사용자가 로그인한 Google 포토의 중복 후보와 비슷한 장면을 기기에서 비교합니다. Google과 제휴하거나 Google이 보증하는 프로그램이 아닙니다.

- **사진 처리:** 미리보기·파일 식별자·촬영일·형식·해상도·용량 및 확인 가능한 HDR 정보를 읽습니다. HDR은 원본 메타데이터 구간을 제한적으로 읽습니다. 동영상은 컨테이너 색상 정보와 영상 내부의 HDR 표시를 읽습니다. 부분 읽기가 가능하면 압축 데이터를 건너뛰고, 지원되지 않으면 순차 읽으면서 압축 데이터는 즉시 버립니다. HDR 응답 본문 읽기 예산은 원본당 64 MiB, 작업당 1 GiB이며 중지·재개에도 누적합니다. 비교 창에서 한 그룹의 ‘사진 정보 다시 확인’을 누르면 그 그룹 확인을 새 작업으로 보고 별도 1 GiB 예산을 씁니다. 이 수치는 브라우저 자체의 선행 네트워크 버퍼를 포함한 전송량 보장은 아닙니다. 컨테이너 메타데이터는 최대 512 KiB, 샘플 위치 표는 최대 100,000개(약 1.2 MB), 개별 HDR 표시 내용은 최대 64 KiB까지 메모리에 잠시 보관합니다. 원본 파일을 디스크에 저장하지 않습니다. 영상 전체와 음성 전체의 동일성을 검증하지 않습니다.
- **AI 장면 비교:** ‘비슷한 사진’과 ‘정확 모드’를 함께 고르면 확장에 포함된 이미지 모델(DINOv2-small, Apache-2.0)이 이 기기 안에서 작은 미리보기의 특징값을 계산합니다. 모델은 내려받지 않고 확장에 들어 있으며, 사진과 특징값을 개발자나 외부 분석 서비스에 보내지 않습니다. 특징값은 브라우저 메모리에서 처리합니다.
- **추천 사진 품질 확인:** 같은 조건에서 비슷한 장면 그룹의 640px 미리보기를 Google 서버에서 읽어, 확장에 포함된 얼굴 모델(MediaPipe Face Landmarker, Apache-2.0)과 초점 계산으로 눈 감음·고개 돌림·시선·흐림 여부를 이 기기 안에서 확인합니다. 얼굴을 알아보거나 사람을 식별하지 않으며, 결과 수치는 브라우저 메모리에서 처리하며, 최종 추천 내용은 아래 임시 결과 사본에 포함될 수 있습니다. 사진과 수치를 개발자나 외부 분석 서비스에 보내지 않습니다.
- **통신:** Google 포토와 Google 이미지 서버에 기존 페이지 로그인 문맥으로 읽기 요청을 보냅니다. 필요한 페이지 세션 값은 페이지 안에서 처리하며 프로필 파일·비밀번호·쿠키를 추출하지 않습니다. 사진·사진 주소·Google 인증정보를 개발자 서버에 보내거나 다른 분석 서버에 업로드하지 않습니다.
- **정보 조회 창:** 파일 정보를 확인할 때(정확 모드나 ‘사진 정보 다시 확인’) 목록만으로 형식·해상도·용량을 알 수 없는 사진이 있으면, 포토픽이 뒤쪽에 작은 Google 포토 창을 잠시 열어 그 사진의 정보 패널을 읽습니다. Chrome의 debugger 권한은 포토픽이 직접 연 이 창에만 연결해 포커스 상태를 모사하는 데 씁니다. 사용자가 연 다른 탭·창에는 연결하지 않고, 네트워크·쿠키·저장소를 들여다보는 명령을 쓰지 않습니다. 조회가 끝나거나 중지되면 연결을 해제하고 창을 닫습니다.
- **저장:** 비교 결과와 크기/유효기간이 제한된 사진 정보 캐시는 기본적으로 현재 탭 메모리에 둡니다. 언어·테마·개인정보 처리 동의와 마지막 검색 설정(검색 종류·비교 방식·기간)은 확장 저장소에 보관합니다. 탐색 설정은 짧은 유효기간의 세션 저장소를 사용합니다. 안전한 업데이트용 임시 체크포인트(복원 유효기간 30분)와 원래 목록으로 돌아갈 때 만드는 임시 사본(복원 유효기간 2분)은 사진 주소·파일 정보·비교 및 추천 결과를 확장 전용 로컬 저장소에 보관합니다. 복원을 확인하거나 목록 복귀가 안정되면 제거합니다. 종료나 중단으로 남은 만료 자료는 다음 백그라운드 실행·브라우저 시작 때 정리하며, 만료된 자료는 복원하지 않습니다. 일반 브라우저 종료·새로고침 후 영구 복원 기능은 아닙니다.
- **무료 베타:** 현재 기능은 모두 무료이며 결제·7일 체험 제한·별도 Google/이메일 인증이 없습니다. 결제 SDK와 개발자 운영 계정/체험 서버가 없고, 광고·행동 분석을 하지 않습니다. 포함된 얼굴 모델 라이브러리(MediaPipe)에 들어 있는 사용 통계 기록은 꺼 두었으며, 확장의 통신 제한(Google 포토·Google 이미지 서버만 허용)으로도 차단합니다. 향후 별도 유료 기능이나 데이터 처리 방식이 추가되면 이용 조건과 개인정보 안내를 갱신합니다.
- **사용자 제어:** 스캔·비교를 중지하고 완료한 결과를 검토할 수 있습니다. 초기화는 사진 자체가 아니라 분석·선택 준비를 지웁니다. 실제 휴지통 이동은 선택 검토와 Google 포토의 최종 확인을 거칩니다. 복원과 보관 기한은 Google 포토 안내를 따릅니다. 확장 제거 또는 Chrome의 확장 데이터 관리로 저장 정보를 지울 수 있습니다.
- **공유:** 사용자 데이터를 판매하거나 광고 목적으로 공유하지 않습니다. 지원 요청에 개인 사진·주소·계정·인증정보를 올리지 마세요.

- **제한적 사용:** Photopick은 Google 포토에서 얻은 정보를 안내한 사진 비교·정리 기능에만 사용하며, Chrome 웹 스토어 사용자 데이터 정책의 제한적 사용(Limited Use) 요건을 준수합니다.
- **지원 사이트와 문의:** 안내 사이트는 GitHub Pages에서 제공하며 GitHub가 보안을 위해 접속 IP 주소를 기록할 수 있습니다. 이메일 문의를 보내면 답변에 필요한 이메일 주소와 문의 내용을 지원 담당자가 처리합니다. 문의에 개인 사진이나 인증정보를 포함하지 마세요.

## English

Photopick compares candidates in the Google Photos account you use, on your device. It is not affiliated with or endorsed by Google.

- **Media:** It reads previews, file identifiers, capture dates, formats, dimensions, sizes and available HDR metadata. HDR checking reads bounded original metadata ranges. For videos, it checks container colour information and HDR signalling inside the video. Compressed payloads are skipped when range reads work, or discarded during a sequential read otherwise. HDR response-body read budgets are 64 MiB per original and 1 GiB per scan, including pause/resume. Refresh photo details for one group in the comparison window counts as a new task with its own 1 GiB budget. These counters do not guarantee total network transfer including browser prefetch buffers. Temporarily retained data is limited to 512 KiB of container metadata, 100,000 sample positions (about 1.2 MB), and 64 KiB per HDR signalling unit. No original media file is saved to disk. Full video/audio identity is not verified.
- **On-device scene model:** With *Similar photos* and *Accurate mode*, a bundled image model (DINOv2-small, Apache-2.0) computes features of small previews on this device. The model ships inside the extension; photos and features are not sent to the developer or external analysis services. Features are processed in browser memory.
- **Keeper quality check:** Under the same settings, 640px previews of similar-scene groups are read from Google servers and checked on this device for closed eyes, turned heads, gaze and blur using a bundled face model (MediaPipe Face Landmarker, Apache-2.0) and a focus measure. It does not recognize or identify people. Scores are processed in browser memory; final recommendations may be included in the temporary result copies described below. Photos and scores are not sent to the developer or external analysis services.
- **Network:** Read requests go to Google Photos and Google image servers using the current page's sign-in context. Required page-session values stay inside that page. Browser profile files, passwords and cookies are not extracted. Photos, private photo URLs and Google credentials are not sent to the developer or another analysis service.
- **Information window:** When checking file details (Accurate mode or Refresh photo details) and the list does not show a photo's format, dimensions or size, Photopick briefly opens a small Google Photos window in the background and reads that photo's info panel. The Chrome debugger permission is attached only to this window that Photopick opened, to emulate focus. It is never attached to tabs or windows you opened, and no network, cookie or storage inspection commands are used. The connection is released and the window closed when the lookup ends or is stopped.
- **Storage:** Bounded result and photo-information caches normally remain in tab memory. Language, theme, consent and the last search settings (search type, comparison method and period) use extension storage. Navigation settings use short-lived session storage. Temporary safe-update checkpoints (valid for restoration for 30 minutes) and library-return copies (valid for 2 minutes) store photo URLs, file details, comparison results and recommendations in extension-private local storage. They are removed after successful restoration or a stable return. Expired copies left after interruption are removed when the background next starts or Chrome restarts; expired copies cannot be restored. Refreshing a page or closing Chrome does not provide permanent result recovery.
- **Free beta:** All current features are free. There is no payment, seven-day trial limit, added Google/email sign-in, billing SDK or developer-operated account/trial server, and no advertising or behavioral analytics. The usage-statistics log inside the bundled face-model library (MediaPipe) is switched off and is also blocked by the extension's network restrictions (Google Photos and Google image servers only). Separate paid features may be introduced later with updated terms and privacy disclosures.
- **Control:** Stop tasks and review completed work. Reset clears analysis and prepared selections, not the photos themselves. Actual moves require selection review and final confirmation in Google Photos. Restoration follows the Google Photos retention notice. Uninstall or use Chrome's extension-data controls to remove stored data.
- **Sharing:** Data is not sold or shared for advertising. Do not include private photos, URLs, account details or authentication values in public support requests.

- **Limited Use:** Photopick uses information obtained from Google Photos only for the photo comparison and organization features described here, in compliance with the Chrome Web Store User Data Policy, including its Limited Use requirements.
- **Support site and contact:** This documentation site is hosted by GitHub Pages, which may log visitors’ IP addresses for security. If you contact support by email, your email address and message are handled to respond to your request. Do not include private photos or authentication information.
