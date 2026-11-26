# BeeTest 3.0.7

Released 2026-11-26 · Desktop app for macOS and Windows · Tester release

- **BeeTest found** – after every web run an AI QA Principal looks at each screen the test visited, with its own
  judgement and not only what the test case checks: confusing or repeated controls, clipped text, things that do not
  match the rest of the app, dark mode, phone width, right-to-left, wording, accessibility, visible security problems.
  Every finding points at its proof on the screen and is checked again by a second, independent AI. Findings are on
  the run page and in Needs you: **Real bug** files a Work bug with the marked picture, **Intended** is remembered and
  not raised again, **Not a bug** teaches BeeTest. A cost limit applies (tokens on a subscription, $ with an API key).
- **Pull request checks read like a principal QA, an architect and a security engineer** – Development Testing looks
  again at the changed features' screens in dark, at 390 px and right to left, and reads the pull request's code for
  design, correctness, data, compatibility, speed, missing tests and security (injection, access checks such as IDOR,
  secrets, risky dependencies). Every code finding quotes the changed lines. Critical or high security, data or
  behaviour findings block the merge check; the rest warn (`gate.findings` in beetest.yml). Findings are in the CLI,
  the report and the pull request comment.
- **Security tests on the branch environment (opt-in)** – with `review.security_probe: auto` or `on`, BeeTest sends
  harmless test requests to the branch environment only (never another host or production) and reports what it
  proves, with the request and the answer, masked. Off by default: some AI providers refuse to plan such requests.
- **Ask BeeTest looks things up itself** – when you ask about your project (a cost, a duration, a run, a test case's
  history…), it reads the data itself, read only and with your role, and answers with the numbers instead of sending
  you to a page. A question whose answer never came offers **Ask again**.
- **Development Testing picks the right tests** – from the KB Test map (core cases on every push, linked cases on a
  pull request), coverage per changed feature, what is not tested and why, user-level drafts; **Autopilot** writes,
  verifies and automates the missing cases on the branch within a per-branch cost limit; guided **set-up of pull
  request checks** for a GitHub repository (5 steps) from Ask BeeTest or Development Testing.
- **Test map in the KB** – features with their test cases, core happy paths, requirements, screens, endpoints and code.
- **Smaller things** – every step of web, mobile and API runs shows how long it took; meeting notes by topic in
  Community Teams calls; the Devices live screen has the shape of its device; a Like bee among the reactions.
- **Fixes** – one "Done" in the issue panel; the add-reaction button no longer leaves a gap once a comment has
  reactions; "1 person" instead of "1 people"; the Watch button is named for screen readers; Development Testing no
  longer reads merge commits as an intended change or a silent environment failure as intended.
- Install steps, system requirements and known limitations are the same as 3.0.0 below.

# BeeTest 3.0.6

Released 2026-11-25 · Desktop app for macOS and Windows · Tester release

- **Update in one click** – BeeTest tells you inside the app when a new version is out; "Update now" downloads it,
  checks it (size and SHA-256) and installs it, then opens the new version. Your data, keys and settings stay. If the
  website cannot be reached, the update is read from GitHub.
- **Ask BeeTest asks before it acts** – questions get a plain answer. When you ask it to do something in BeeTest
  (open a page, run tests, create a test case, file a bug…), it offers "Yes, do it" or "No, just tell me how", then
  does it on the screens while you watch and can stop it. Under the message box choose **Ask before acting**
  (default) or **Full access** (acts without asking; deletes and steps that cannot be undone still ask). Admins can
  turn Full access off per project.
- **The desktop bee** – stays on your desktop while BeeTest runs (right-click › Hide Bee to put it away). It flies,
  walks and rests near the screen edges, blinks, yawns, lounges at lunch and sleeps at night, and stays still while
  you point at it or share your screen. When work finishes while BeeTest is in the background, it pops a speech
  bubble with the result and a soft "ting" (sound and flying can be turned off).
- **Runs** – while several test cases run you see which one is running, passed or failed; the console is grouped per
  test case; errors are shown in full; a pass that needed a retry or has a failed step says so.
- **Smaller things** – the Overview shows the top 10 features (with "Show all") in slimmer charts; the logo is clear
  in dark mode; any profile picture is accepted and made small automatically; Community Teams messages use the full
  width with the BeeTest mark as its avatar; the privacy policy and terms say that team admins can read team
  messages for moderation.
- **Fixes** – the master key and the test engine are kept when you reinstall or update (3.0.5 test builds could fail
  to start); the run page no longer leaves a tall empty space under a long log; the Overview tooltip no longer greys
  the chart.
- Install steps, system requirements and known limitations are the same as 3.0.0 below.

# BeeTest 3.0.4

Released 2026-11-24 · Desktop app for macOS and Windows · Tester release

- **Screen sharing like Teams** – choose a whole screen or one window side by side; a light-green frame shows what
  you share (it follows a shared window), a small "You are sharing your screen · Stop sharing" bar sits at the top,
  and a compact meeting window (time, camera, microphone, back to the call, leave, a preview of what you share and who
  is speaking) floats over your other apps. None of these appear in what the others see. Your own call window no
  longer shows a mirror of your screen.
- **Calls on hold** – answering a call while you are in another one puts the first call on hold instead of leaving
  it; a bar lets you resume or hang up, and the others see "On hold".
- **Cleaner filters** – single-choice filters (test kind, question status, draft status, run result) are compact
  dropdowns with counts instead of long rows of chips.
- Fixes found by the go-live end-to-end check (two installs on one team, Pro billing, Admin console, Community Teams
  and meetings), a language review of the admin, license, call and calendar texts in 6 languages, and per-seat billing
  wording.
- Install steps, system requirements and known limitations are the same as 3.0.0 below.

---

# BeeTest 3.0.3

Released 2026-11-24 · Desktop app for macOS and Windows · Tester release

- **Development Testing Mode** – connect your repo with `beetest init`; every branch and PR gets the test cases its
  change affects (with the reason and a confidence), draft test cases from ticket criteria, and every failure sorted:
  likely bug, intended change, flaky, environment, already failing on main. One PR comment, a status and a JUnit file
  (GitHub, GitLab, Bitbucket, Azure DevOps). `beetest merge` turns approved drafts into test cases.
- **Generate beetest.yml with BeeTest AI** from your repository's folders, features, test cases and tickets.
- **The knowledge base is the project's brain** – BeeTest works on its own and asks only when it has a real concern
  (one question per topic); your answer is the approval. New tabs in AI knowledge: *Needs you*, *Knowledge*,
  *Autonomy* and *Growth* (what BeeTest did and learned, measured from real outcomes).
- **Community Teams** (Pro, formerly Chat) – a Teams-like **calendar** (day / week / month, recurring meetings,
  RSVP, reminders, join the meeting call), **reactions** with BeeTest stickers, and **background effects** for video
  calls (blur, sample backgrounds, your own picture – processed on your device).
- **Admin mode for team owners** – one console for people (invite keys, roles, block, reset codes, owner protection
  and transfer), projects (per-project access), Community Teams (channels, retention, meetings), billing, AI cost per
  person with budgets, security settings and an audit log.
- **Start or join a team** – the first sign-up creates your own team (you are its owner); others join with the secret
  key the admin sends. No seat limit: each new member is simply billed.
- **Clear Pro lifecycle** – reminders before the end, a 14-day grace period, nothing is ever deleted, and a plain
  explanation for every person when Pro ends (see docs/LICENSING.md).
- **Meetings** – chat inside the call, an AI summary of who said what and who does what (in your language), reminders
  15 minutes before, "X joined the meeting" notices, and a redesigned call window.
- **7 languages**: English, Tiếng Việt, 日本語, 中文, 한국어, العربية (right-to-left), ไทย.
- Server mode for team CI runners (`BEETEST_SERVER=1`, Docker files included).
- Install steps, system requirements and known limitations are the same as 3.0.0 below.

---

# BeeTest 3.0.2

Released 2026-11-23 · Desktop app for macOS and Windows · Tester release

- **Hardening:** the app is now shipped minified with its code comments removed, and with Electron security fuses set
  (the debugger and `NODE_OPTIONS` are disabled, and the app only loads from its signed archive). This raises the cost
  of reverse-engineering; the "Created by BeeTest" attribution is kept intact.
- No feature or behaviour changes from 3.0.1.
- Install steps, system requirements and known limitations are the same as 3.0.0 below.

---

# BeeTest 3.0.1

Released 2026-11-23 · Desktop app for macOS and Windows · Tester release

- **Issue history is easier to read**: the person and the field are in bold, a status shows as its coloured lozenge
  (like on the board), the old value is muted and struck through, the new value is highlighted.
- The "External link" field (a Jira / Linear link added by sync) has a readable name in the history.
- Install steps, system requirements and known limitations are the same as 3.0.0 below.

---

# BeeTest 3.0.0

Released 2026-11-23 · Desktop app for macOS and Windows · Tester release

- [Tiếng Việt](#tiếng-việt)
- [English](#english)

---

## Tiếng Việt

### Điểm mới so với 2.x

**Công việc (Work) và trình soạn thảo**
- Mục Công việc trong mỗi dự án: danh sách issue (bug, task, story), bảng Kanban kéo thả, Backlog và sprint, trang
  tài liệu (kế hoạch test, ghi chú phát hành, biên bản họp) với trình soạn thảo đầy đủ.
- Đồng bộ ticket hai chiều với **Jira** và **Linear**: sprint / cycle, xung đột được hiện rõ, các test cần chạy lại.

**Pro: làm việc nhóm**
- Chat nhóm kiểu Slack: kênh công khai / riêng tư, #general, tin nhắn trực tiếp, gắn sao, tìm kiếm, trả lời, sửa.
- Gọi thoại và video, chia sẻ màn hình, **phụ đề trực tiếp** (có dịch), ghi âm và **tóm tắt cuộc họp** kèm việc cần làm.
- Sticker và biểu cảm **Bee** trong chat và bình luận.
- **Thanh toán** Pro ngay trong app (Hồ sơ › Gói), quản lý số ghế và chu kỳ thanh toán.

**Hỗ trợ và tài khoản**
- **Báo lỗi** ngay trong app (mục Báo lỗi ở thanh bên): chụp màn hình, xem trước những gì được gửi, danh sách báo cáo của tôi.
- Trang **Hồ sơ**: tên, ảnh, giao diện sáng / tối, ngôn ngữ, gói.
- Màn hình đăng nhập mới, biểu tượng ứng dụng BeeTest.

**Kiểm thử**
- **Bản đồ tri thức 3D** của dự án.
- Loại test **Flow** (luồng nhiều bước, web + mobile, iframe, chờ nội dung trang), tạo bug từ flow chạy lỗi.
- **Phiên bản mobile** của test web (`*.mobile.spec.ts`) chạy trên điện thoại / máy tính bảng; preset thiết bị mới
  (iPhone SE hiện tại, Galaxy S24...).
- Nhập OpenAPI, kiểm tra contract, kiểm thử tải kiểu k6, ngân sách hiệu năng Lighthouse.
- AI chạy song song nhiều việc hơn, tự tiếp tục khi bị treo, hỏi "Ask BeeTest" cách dùng BeeTest.

**Sửa lỗi**: rất nhiều sửa lỗi về chat, cuộc gọi, giao diện điện thoại (390 px), chế độ tối, kết nối cơ sở dữ liệu cloud
(TLS), tạo dự án trên MySQL cục bộ, cài đặt tự động các mục còn thiếu trong Kiểm tra hệ thống.

### Yêu cầu hệ thống

| | macOS | Windows |
|---|---|---|
| Hệ điều hành | macOS 12 Monterey trở lên | Windows 10 / 11, 64-bit |
| Bộ xử lý | Apple silicon (M1 trở lên) hoặc Intel | x64 |
| RAM | 8 GB (khuyến nghị 16 GB) | 8 GB (khuyến nghị 16 GB) |
| Ổ đĩa trống | 5 GB (app, MySQL cục bộ, trình duyệt test) | 5 GB |
| Mạng | Cần Internet ở lần chạy đầu (tải Node.js, MySQL, Playwright) | như macOS |

### Cài đặt trên macOS

1. Tải đúng bản: **BeeTest-3.0.0-mac-arm64.dmg** (Apple silicon) hoặc **BeeTest-3.0.0-mac-x64.dmg** (Intel).
   Không biết máy loại nào: menu Apple › Giới thiệu về máy Mac, dòng "Chip" (Apple M…) là arm64.
2. Mở file .dmg, kéo **BeeTest** vào **Applications**.
3. **App chưa được Apple ký / công chứng (notarize)** nên lần đầu macOS sẽ chặn:
   - Trong Finder, mở Applications, **chuột phải (hoặc Control + bấm) vào BeeTest › Mở › Mở**. Chỉ cần làm một lần.
   - Trên macOS 15 trở lên, nếu không có nút Mở: Cài đặt hệ thống › Quyền riêng tư & Bảo mật, kéo xuống, bấm
     **Vẫn mở (Open Anyway)** cho BeeTest, rồi mở lại.
   - Hoặc trong Terminal: `xattr -dr com.apple.quarantine /Applications/BeeTest.app`
4. Lần đầu: tạo tài khoản, rồi chọn nơi lưu dữ liệu (một bấm cài MySQL cục bộ, hoặc cơ sở dữ liệu cloud).

### Cài đặt trên Windows

1. Tải **BeeTest-Setup-3.0.0-win-x64.exe** và mở nó.
2. App chưa được ký số nên **SmartScreen** có thể hiện "Windows đã bảo vệ máy tính của bạn": bấm **Thông tin thêm
   (More info) › Vẫn chạy (Run anyway)**.
3. Làm theo trình cài đặt, rồi mở BeeTest từ menu Start.
4. Không cài được: dùng bản **BeeTest-3.0.0-win-x64-portable.zip**, giải nén và chạy `BeeTest.exe`.

Kiểm tra file tải về: so mã SHA-256 với `SHA256SUMS.txt` (macOS: `shasum -a 256 <file>`, Windows:
`certutil -hashfile <file> SHA256`).

### Báo lỗi

Trong app: mục **Báo lỗi** ở thanh bên trái. Viết điều bạn đã làm, điều mong đợi và điều xảy ra; có thể
đính kèm ảnh chụp màn hình. Báo cáo được gửi tới kênh Discord của nhóm BeeTest; bạn xem trước chính xác những gì được gửi.
Nhật ký: menu Help › Open the log.

### Giới hạn đã biết

- **Mua Pro** cần máy chủ thanh toán của BeeTest đang hoạt động; nếu chưa mở, hộp thoại Nâng cấp sẽ báo rõ là không kết
  nối được dịch vụ thanh toán. Người thử nghiệm cần Pro có thể xin **khóa thử** từ chủ sở hữu và nhập ở Hệ thống ›
  Giấy phép.
- Pro (chat, cuộc gọi, không gian nhóm) cần **cơ sở dữ liệu cloud**; MySQL cục bộ chỉ dùng cho bản Free một người.
- App chưa được ký số (macOS chưa notarize, Windows chưa có chứng chỉ): cảnh báo khi mở lần đầu là bình thường.
- Chưa có cập nhật tự động: bản mới cần tải và cài lại (dữ liệu được giữ).
- Lần chạy đầu tải Node.js, MySQL và trình duyệt Playwright nên cần Internet và vài phút.
- MySQL cục bộ vẫn chạy nền sau khi thoát BeeTest (để lần mở sau nhanh hơn).

---

## English

### What's new since 2.x

**Work and the editor**
- A Work area in every project: issues (bugs, tasks, stories), a drag-and-drop board, backlog and sprints, and pages
  (test plans, release notes, meeting notes) with a full editor.
- Two-way ticket sync with **Jira** and **Linear**: sprints / cycles, visible conflicts, tests to run again.

**Pro: teamwork**
- Slack-like team chat: public / private channels, #general, direct messages, starred, search, reply, edit.
- Voice and video calls, screen sharing, **live captions** (with translation), recording and **meeting summaries** with
  action items.
- **Bee** stickers and expressions in chat and comments.
- **Billing** for Pro inside the app (Profile › Plan): seats and monthly / yearly billing.

**Support and account**
- **Report issue** inside the app (Report issue in the sidebar): screenshots, a preview of exactly what is sent, My reports.
- **Profile** page: name, picture, light / dark theme, language, plan.
- New sign-in screen and the BeeTest app icon.

**Testing**
- **3D knowledge map** of a project.
- **Flow** test kind (multi-step journeys, web + mobile, iframes, wait for page text); a bug from a failed flow run.
- **Mobile versions** of web cases (`*.mobile.spec.ts`) that run on phones / tablets; new device presets (current
  iPhone SE, Galaxy S24, ...).
- OpenAPI import, contract checks, k6-style load tests, Lighthouse performance budgets.
- More AI work in parallel, automatic resume of a stalled job, "Ask BeeTest" answers how to use BeeTest.

**Fixes**: many fixes in chat, calls, phone layouts (390 px), dark mode, cloud database connections (TLS), project
creation on a local MySQL, and the System check now installs every missing item by itself.

### System requirements

| | macOS | Windows |
|---|---|---|
| OS | macOS 12 Monterey or later | Windows 10 / 11, 64-bit |
| CPU | Apple silicon (M1 or later) or Intel | x64 |
| Memory | 8 GB (16 GB recommended) | 8 GB (16 GB recommended) |
| Free disk | 5 GB (app, local MySQL, test browsers) | 5 GB |
| Network | Internet on the first launch (Node.js, MySQL, Playwright downloads) | same |

### Install on macOS

1. Pick the right file: **BeeTest-3.0.0-mac-arm64.dmg** (Apple silicon) or **BeeTest-3.0.0-mac-x64.dmg** (Intel).
   Not sure? Apple menu › About This Mac: "Chip Apple M…" means arm64.
2. Open the .dmg and drag **BeeTest** to **Applications**.
3. **The app is not signed or notarized by Apple yet**, so macOS blocks the first launch:
   - In Finder › Applications, **right-click (or Control-click) BeeTest › Open › Open**. Only needed once.
   - On macOS 15 or later, if there is no Open button: System Settings › Privacy & Security, scroll down, click
     **Open Anyway** for BeeTest, then open it again.
   - Or in Terminal: `xattr -dr com.apple.quarantine /Applications/BeeTest.app`
4. First launch: create your account, then choose where BeeTest keeps its data (one-click local MySQL, or a cloud
   database).

### Install on Windows

1. Download **BeeTest-Setup-3.0.0-win-x64.exe** and open it.
2. The app is not code-signed yet, so **SmartScreen** may say "Windows protected your PC": click **More info › Run
   anyway**.
3. Follow the installer, then start BeeTest from the Start menu.
4. If the installer cannot be used: take **BeeTest-3.0.0-win-x64-portable.zip**, unzip it and run `BeeTest.exe`.

Check a download: compare its SHA-256 with `SHA256SUMS.txt` (macOS: `shasum -a 256 <file>`, Windows:
`certutil -hashfile <file> SHA256`).

### Reporting issues

In the app: **Report issue** in the left sidebar. Describe what you did, what you expected and what happened; screenshots can be
attached. The report goes to the BeeTest team's Discord channel, and you see a preview of exactly what is sent. The log:
Help › Open the log.

### Known limitations

- **Buying Pro** needs the BeeTest billing server to be online; until it is, the Upgrade dialog says clearly that the
  billing service cannot be reached. Testers who need Pro can get a **test key** from the owner and enter it in
  System › License.
- Pro (chat, calls, team space) needs a **cloud database**; a local MySQL is for the one-person Free plan.
- The app is not code-signed (macOS not notarized, Windows without a certificate): the first-launch warning is expected.
- No automatic updates yet: install a new version over the old one (your data is kept).
- The first launch downloads Node.js, MySQL and the Playwright browsers, so it needs the Internet and a few minutes.
- The local MySQL keeps running in the background after BeeTest quits (so the next start is quick).
