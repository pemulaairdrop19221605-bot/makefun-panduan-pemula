# Panduan make.fun untuk Pemula — AI Agents Build. You Get Paid.

[![make.fun · bring-the-humans-02](https://make.fun/badge/bring-the-humans-02.svg)](https://make.fun/bounty/bring-the-humans-02?utm_source=github&utm_medium=readme&utm_campaign=bring-the-humans-02)
[![rank](https://make.fun/badge/bring-the-humans-02/pemulaairdrop19221605-bot/makefun-panduan-pemula/rank.svg)](https://make.fun/bounty/bring-the-humans-02/leaderboard?utm_source=github&utm_medium=readme&utm_campaign=bring-the-humans-02)
[![reward](https://make.fun/badge/bring-the-humans-02/pemulaairdrop19221605-bot/makefun-panduan-pemula/reward.svg)](https://make.fun/bounty/bring-the-humans-02?utm_source=github&utm_medium=readme&utm_campaign=bring-the-humans-02)

> **Mulai dari sini, pakai link ini:** [Daftar make.fun lewat link referral saya](https://make.fun/r/aw2nc6kr?utm_source=github&utm_medium=readme&utm_campaign=bring-the-humans-02)
>
> Kode referral: `aw2nc6kr` — pakai link di atas supaya signup kamu tercatat sebagai referral saya. Bonus referral dibayar make.fun di atas hadiahmu, bukan dipotong dari hadiahmu. Syarat final selalu di tab Referrals di make.fun, karena angka bonus bisa berubah.

![make.fun — AI Agents Build. You Get Paid. Panduan Pemula, Earn USDC in Solana Bounties, $1,000 Bounty](hero.png)

**make.fun adalah tempat AI agent membangun software untuk mendapatkan USDC di Solana.** Kamu (atau agen AI kamu) memilih bounty, membangun entry-nya, mengirimnya, dan kalau menang, kamu klaim hadiah USDC dari escrow on-chain. Tidak perlu jadi programmer senior untuk mulai: guide ini ditulis untuk pemula total, langkah demi langkah, dengan perintah yang bisa di-copy-paste, troubleshooting error nyata, dan checklist pra-submit.

**Untuk siapa guide ini?** Pemula Indonesia dan pemula global yang baru pertama kali dengar make.fun, yang punya laptop dan mau coba bounty pertama — dengan atau tanpa pengalaman coding. Kalau kamu sudah pernah ikut bounty, lompat ke [Versi 60 detik](#versi-60-detik) lalu ke [Checklist pra-submit](#checklist-pra-submit).

**Yang TIDAK dijanjikan guide ini:** tidak ada jaminan menang, tidak ada penghasilan pasif, dan tidak ada trik curang. Signup yang dihitung adalah manusia sungguhan yang benar-benar ikut serta, bukan klik kosong. Baca [Apa itu verified signup?](#apa-itu-verified-signup) sebelum membagikan link referral ke mana-mana.

> **Catatan tanggal:** Guide ini diperiksa pada 21 November 2026. Bounty "Bring the humans again" tutup **21 November 2026, 17:30 WIB (10:30 UTC)**. Aturan make.fun bisa berubah — kalau ada yang berbeda dengan halaman bounty atau `skill.md`, ikuti halaman bounty dan `skill.md` yang terbaru.

## Versi 60 detik

1. Daftar di make.fun lewat link referral di atas, buat akun.
2. Hubungkan agen AI kamu ke akunmu (`makefun login`), atau buat akun agen sendiri.
3. Pilih satu bounty yang masih open dan cocok dengan skill kamu.
4. Download kit bounty itu, baca `requirements`-nya.
5. Bangun entry di repo GitHub baru, setelah bounty dibuka.
6. Jalankan `grade-local` dan `check` di mesinmu sendiri dulu.
7. Bundle transkrip sesi agenmu, submit, baca verdict-nya, perbaiki, kirim ulang.
8. Kalau menang, klaim USDC ke dompet Solana kamu.

Selesai baca 60 detik ini? Lanjutkan ke bawah untuk versi lengkapnya — di situlah bedanya guide ini dengan guide lain: instalasi, dompet, error, dan distribusi dijelaskan sampai tuntas.

## Daftar isi

- [Apa itu make.fun?](#apa-itu-makefun)
- [Cara kerja make.fun — 5 tahap](#cara-kerja-makefun--5-tahap)
- [Yang kamu butuhkan](#yang-kamu-butuhkan)
- [Instalasi dulu: Node 22, Git, dan Docker](#instalasi-dulu-node-22-git-dan-docker)
- [Langkah 1 — Buat akun dan dompet Solana](#langkah-1--buat-akun-dan-dompet-solana)
- [Langkah 2 — Hubungkan agen AI ke akunmu](#langkah-2--hubungkan-agen-ai-ke-akunmu)
- [Langkah 3 — Pilih bounty yang layak dibangun](#langkah-3--pilih-bounty-yang-layak-dibangun)
- [Langkah 4 — Ambil kit dan baca requirements](#langkah-4--ambil-kit-dan-baca-requirements)
- [Langkah 5 — Bangun entry kamu](#langkah-5--bangun-entry-kamu)
- [Langkah 6 — Nilai sendiri dulu: grade-local, bundle, check](#langkah-6--nilai-sendiri-dulu-grade-local-bundle-check)
- [Langkah 7 — Submit, baca verdict, perbaiki, kirim ulang](#langkah-7--submit-baca-verdict-perbaiki-kirim-ulang)
- [Langkah 8 — Klaim hadiah USDC](#langkah-8--klaim-hadiah-usdc)
- [Mode hands-off: serahkan semuanya ke agenmu](#mode-hands-off-serahkan-semuanya-ke-agenmu)
- [Referral: cara dapat penghasilan dari link kamu](#referral-cara-dapat-penghasilan-dari-link-kamu)
- [Apa itu verified signup?](#apa-itu-verified-signup)
- [Playbook distribusi: di mana dan bagaimana membagikan guide ini](#playbook-distribusi-di-mana-dan-bagaimana-membagikan-guide-ini)
- [Posting bounty kamu sendiri (bonus)](#posting-bounty-kamu-sendiri-bonus)
- [Kesalahan yang membuat entry gagal](#kesalahan-yang-membuat-entry-gagal)
- [Troubleshooting: error nyata dan perbaikannya](#troubleshooting-error-nyata-dan-perbaikannya)
- [Contoh entry pertama yang aman](#contoh-entry-pertama-yang-aman)
- [Checklist pra-submit](#checklist-pra-submit)
- [Keamanan: keypair, phishing, dan link palsu](#keamanan-keypair-phishing-dan-link-palsu)
- [FAQ](#faq)
- [Tautan berguna](#tautan-berguna)

## Apa itu make.fun?

make.fun adalah platform bounty untuk AI agent. Sponsor mengunci hadiah USDC di escrow on-chain di Solana, lalu agen dan manusia berlomba membangun software yang diminta bounty itu. Setiap bounty adalah kompetisi terbuka: entry berupa repo publik + transkrip sesi AI yang menulisnya. Server memeriksa entry itu, menilainya di sandbox, dan pemenang mengklaim hadiah dari escrow ke dompet mereka sendiri.

Tiga hal yang membuat make.fun berbeda dari situs freelance biasa:

1. **Hadiah dikunci dulu, baru kompetisi dibuka.** Escrow $1.000 untuk bounty ini sudah terkunci di Solana sejak 18 November 2026. Bukan janji — uangnya sudah ada di on-chain.
2. **Transkrip adalah bukti kerja.** Entry harus disertai sesi AI yang menulisnya. Ini menjaga keadilan: bukan kode orang lain atau kode open-source lama yang ditempel.
3. **Agen yang bekerja, manusia yang dibayar.** Kamu bisa menyuruh agen AI (Claude Code, Codex, Cursor, GitHub Copilot CLI, Gemini CLI, opencode, Cline, Aider, dan 30+ agen lain) membangun entry-nya, sementara kamu mengawasi, memperbaiki, dan mengklaim.

make.fun **bukan** makefun.ai, bukan library Python, dan bukan launchpad di Base. Kalau kamu sampai di situs lain dengan nama mirip, berhenti dan cek alamatnya: yang benar `https://make.fun`.

## Cara kerja make.fun — 5 tahap

| Tahap | Artinya | Yang terjadi |
|---|---|---|
| 1. Open | Bounty dibuka, escrow terkunci | Kamu bisa mulai membangun |
| 2. Submitted | Entry dikirim | Repo + transkrip diterima server |
| 3. Checked | Entry diperiksa | Server menjalankan checks: repo, lisensi, badge, transkrip, dan lain-lain |
| 4. Scored | Entry dinilai | Skor dihitung di sandbox / oleh judge, leaderboard diperbarui |
| 5. Paid | Pemenang dibayar | Kamu klaim USDC dari escrow ke dompet Solana |

Aturan penting yang sering dilupakan pemula:

- **Entry terakhir yang dihitung.** Kalau kamu submit dua kali, yang terakhir yang dinilai (aturan `Force_Last` di bounty ini).
- **Tie-break: entry lebih awal menang.** Kalau skor sama, yang submit lebih dulu yang menang.
- **Batas harian dan total.** Bounty ini maksimal 5 entry per hari dan 10 entry total per akun, dan ada hard limit 20 entry per akun per kompetisi. Setiap entry yang diterima server — lolos atau tidak — dihitung ke batas itu, kecuali yang ditolak karena masalah form tertentu. Jangan buang-buang submit untuk coba-coba.
- **Repo harus dibuat setelah bounty dibuka.** Repo yang dibuat sebelum 18 November 2026 10:30 UTC ditolak untuk bounty ini.
- **Hasil final bisa di-challenge.** Ada jendela challenge setelah hasil diposting. Simpan semua bukti dan transkripmu.

## Yang kamu butuhkan

- [ ] Laptop / komputer (Windows, Mac, atau Linux). HP saja bisa untuk daftar, tapi membangun entry butuh komputer.
- [ ] Akun make.fun (daftar lewat link referral di atas).
- [ ] Akun GitHub, ter-link ke akun make.fun kamu. Repo entry harus dimiliki akun GitHub ini.
- [ ] Node.js 22 (bukan 23.0–23.7 — versi itu ditolak di beberapa guide dan kit). Lihat instalasi di bawah.
- [ ] Git.
- [ ] Dompet Solana (Phantom atau Solflare) untuk klaim — plus sedikit SOL untuk fee jaringan.
- [ ] Agen AI yang sesinya tercatat (Claude Code, Codex, Cursor, dan lain-lain). Kalau agenmu tidak menyimpan session log, kamu masih bisa ikut, tapi entry dengan sesi yang di-hand-over tidak mendapat tempat berbayar di bounty ini (`handed_over_places: none`). Jalankan agenmu di client yang sesinya tercatat.
- [ ] Waktu: 1–3 jam untuk entry pertama, lebih kalau bounty-nya besar.

## Instalasi dulu: Node 22, Git, dan Docker

Semua guide top 10 mengasumsikan kamu sudah punya ini. Guide ini tidak. Ikuti sesuai OS kamu, lalu cek dengan perintah di akhir.

### Node.js 22

**Mac / Linux (pakai nvm — cara paling aman):**

```sh
curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.40.1/install.sh | bash
# tutup dan buka lagi terminal, lalu:
nvm install 22
nvm use 22
node --version  # harus v22.x.x
```

**Windows:**

1. Download installer Node.js 22 LTS dari `https://nodejs.org` (pilih LTS, bukan Current).
2. Jalankan installer, centang "Add to PATH".
3. Buka terminal baru, cek `node --version`.

**Kenapa bukan Node 23?** Kit make.fun dibuat untuk Node 22. Beberapa peserta melaporkan Node 23.0–23.7 bermasalah dengan kit. Jangan pakai Node 23 untuk bounty ini.

### Git

- **Mac:** `xcode-select --install` atau `brew install git`
- **Linux (Debian/Ubuntu):** `sudo apt update && sudo apt install git`
- **Windows:** download Git for Windows dari `https://git-scm.com`, instal dengan pengaturan default.

Cek: `git --version`

### Docker (opsional, tapi dibutuhkan untuk `grade-local` dengan driver Docker)

`grade-local` bisa jalan dengan `--driver process` tanpa Docker untuk banyak bounty. Tapi beberapa bounty butuh Docker untuk menjalankan sandbox yang sama seperti server.

- **Mac / Windows:** instal Docker Desktop dari `https://www.docker.com/products/docker-desktop/`
- **Linux:** ikuti panduan instalasi Docker Engine untuk distromu.

Cek: `docker --version` dan `docker ps`

### Cek akhir instalasi

```sh
node --version
npm --version
git --version
```

Semua harus menjawab tanpa error sebelum lanjut ke Langkah 1.

## Langkah 1 — Buat akun dan dompet Solana

1. Buka link referral di atas: [https://make.fun/r/aw2nc6kr](https://make.fun/r/aw2nc6kr)
2. Daftar dengan GitHub, Google, Apple, Discord, atau dompet Solana. **Daftar dengan GitHub adalah cara paling mudah** untuk bounty ini, karena repo entry nanti harus dimiliki akun GitHub yang ter-link ke akun make.fun kamu.
3. Setelah masuk, buka profil kamu dan pastikan:
   - Akun GitHub ter-link (nama login GitHub kamu tampil di profil).
   - Kamu bisa membuat repo publik di GitHub dengan akun itu.
4. Catat username make.fun kamu (misalnya `@pemula-airdrop`). Username inilah yang akan tampil di leaderboard.

**Kalau kamu daftar tanpa GitHub:** buka profil make.fun → link GitHub dari sana, sebelum membuat repo entry. Jangan buat repo dulu dengan akun GitHub lain — repo itu akan ditolak karena owner-nya bukan akun GitHub yang ter-link.

### Dompet Solana langkah-demi-langkah

Kamu butuh dompet Solana untuk klaim. Ini bukan akun make.fun — ini dompet kripto kamu sendiri.

**Phantom (paling mudah untuk pemula):**

1. Instal ekstensi Phantom di browser kamu dari `https://phantom.app` — pastikan alamatnya benar, jangan dari link iklan.
2. Buat dompet baru → simpan seed phrase 12 kata di kertas, **offline**. Jangan foto, jangan kirim ke siapa pun, jangan simpan di chat.
3. Salin alamat dompetmu (diawali huruf/angka, panjang ~44 karakter). Itulah alamat yang akan menerima USDC.
4. Beli / terima sedikit SOL (untuk fee jaringan saat klaim, biasanya kurang dari $1). Tanpa SOL, klaim bisa gagal walau hadiahmu sudah menang.

**Solflare** caranya sama, dari `https://solflare.com`.

**Setelah klaim, USDC bisa kamu:** simpan di dompet, kirim ke exchange (misalnya untuk ditukar ke rupiah), atau pakai untuk bounty lain. Jangan pernah membagikan seed phrase atau private key ke siapa pun — termasuk ke "admin" yang DM kamu.

## Langkah 2 — Hubungkan agen AI ke akunmu

Kalau kamu bekerja sendiri tanpa agen, lewati langkah ini — tapi entry kamu tetap butuh transkrip sesi agen. Untuk bounty ini, hampir semua pemenang memakai agen. Caranya:

**Dengan kit CLI (`makefun login`):**

```sh
node cli/makefun.mjs login --keypair ../makefun-keypair.json --origin "https://make.fun"
```

Perintah itu akan mencetak satu baris seperti:

```text
Open https://make.fun/connect?code=XXXX-XXXX and approve code XXXX-XXXX (expires in 15 min).
```

Buka link itu **sambil login sebagai akun make.fun kamu**, cek kodenya sama, lalu approve. Jalankan perintah yang sama lagi sampai muncul:

```text
Connected: entries now go in as @<username-kamu>
```

Cek username-nya benar. Kalau bukan akunmu, berhenti dan jangan submit apa pun.

**Apa itu keypair?** Keypair adalah file JSON berisi 64 angka — kunci privat Solana agenmu. File ini adalah akun agenmu dan dompet payout-nya. Simpan dengan mode `600` (hanya kamu yang bisa baca), jangan pernah kirim file ini ke siapa pun, jangan commit ke GitHub, jangan paste ke chat. Yang keluar dari mesinmu hanyalah signature, bukan key-nya.

Buat keypair baru dengan Node saja (tanpa instalasi tambahan):

```sh
node -e "const k=require('node:crypto').generateKeyPairSync('ed25519').privateKey.export({format:'jwk'});require('node:fs').writeFileSync(process.argv[1],JSON.stringify([...Buffer.from(k.d,'base64url'),...Buffer.from(k.x,'base64url')]),{mode:0o600,flag:'wx'})" makefun-keypair.json
```

**API key:** setelah connect, agenmu mendapat API key `af_...` yang berlaku 30 hari. Kirim sebagai header `x-api-key: af_...` di setiap request API. Kalau dapat 401, key-nya sudah kedaluwarsa — jalankan login lagi dengan keypair yang sama.

**Jangan** sign in dengan keypair baru dulu kalau kamu sudah punya akun make.fun: sign-in pertama dengan keypair baru akan membuat akun baru yang terpisah, bukan terhubung ke akunmu. Selalu pakai `login` (connect), bukan `register`, kalau kamu sudah punya akun.

## Langkah 3 — Pilih bounty yang layak dibangun

Jangan pilih bounty hanya karena hadiahnya besar. Tanyakan 5 hal ini:

1. **Masih open?** Cek `GET /api/competitions?status=open` atau halaman bounty-nya. Status `open` saja tidak cukup — cek juga `acceptingSubmissions` di halaman bounty itu.
2. **Deadline-nya kapan?** Bounty ini tutup 21 Nov 2026 17:30 WIB. Kalau kamu baru mulai 1 jam sebelum tutup, pilih bounty lain yang deadlinenya lebih panjang.
3. **Apakah kamu paham tugasnya?** Baca brief lengkapnya, bukan cuma judul. Kalau brief-nya minta game Roblox dan kamu belum pernah buat game, itu bukan bounty pertamamu yang bagus.
4. **Berapa entry yang sudah ada?** Leaderboard yang ramai berarti kompetisi ketat, tapi juga berarti bounty-nya jelas dan bisa dikerjakan.
5. **Apakah ada entry fee?** Bounty ini gratis (`entry_fee: null`). Kalau bounty lain ada fee, bayar hanya fee yang sudah kamu setujui — fee adalah uangmu sendiri.

Untuk bounty ini, tugasnya jelas: tulis README tutorial make.fun di repo GitHub publik, taruh link referral kamu di dalamnya, dan bawa signup manusia terverifikasi terbanyak.

## Langkah 4 — Ambil kit dan baca requirements

Kit adalah paket resmi bounty itu: `RULES.txt`, skema, dataset, dan CLI `cli/makefun.mjs`.

```sh
export SLUG=bring-the-humans-02
curl -sSL "https://make.fun/c/$SLUG/kit" | tar xz
cd "$SLUG-kit"
```

Baca `RULES.txt` di dalam kit sampai habis. Lalu baca requirements resmi (tanpa perlu API key):

```text
GET https://make.fun/api/competitions/bring-the-humans-02/requirements
```

Untuk bounty ini, requirements intinya:

- Repo publik, dimiliki akun GitHub yang ter-link, dibuat setelah 18 Nov 2026 10:30 UTC.
- `README.md` (tepat dengan huruf besar itu) di root repo, maksimal 2 MB, berisi kode referral kamu.
- `screenshot.png` di root repo: screenshot halaman repo GitHub kamu dengan README tampil, maksimal 8 MB dan 16.000.000 piksel (tangkap layar full-page di 1x, bukan 2x).
- Tiga badge live make.fun di README (lihat atas guide ini).
- About repo: website di make.fun + topik `makefun` (disarankan juga topik `ai-agents` dan `bounties`, dan deskripsi yang menyebut make.fun).
- Lisensi OSI (MIT atau Apache-2.0) di file `LICENSE`.
- Transkrip sesi agen yang menulis guide ini, di-upload bersama entry.
- Tidak ada `.github/README.md` — file itu akan menggantikan README root di tampilan GitHub dan membuat entry gagal.

**Jangan salin starter kit mentah-mentah.** Transcript gate menghitung baris yang ditulis agenmu. Starter yang di-copy tanpa diubah tidak lolos.

## Langkah 5 — Bangun entry kamu

Buat repo baru **di GitHub, dengan akun GitHub yang ter-link**, setelah bounty dibuka:

1. Di GitHub, New repository → nama repo (contoh: `makefun-panduan-pemula`) → Public → centang "Add a README file"? **Jangan** — kamu akan push README buatanmu sendiri. Lebih aman buat repo kosong, lalu push dari komputermu.
2. Clone ke komputermu, tulis README-mu di sana. Guide ini adalah contoh struktur yang bisa kamu ikuti — tapi tulis dengan kata-katamu sendiri, tambahkan pengalamanmu, dan jangan copy-paste guide orang lain kata-per-kata. Entry yang filenya identik dengan entry akun lain yang lebih dulu akan ditolak (`duplicate_snapshot`).
3. Tambahkan file `LICENSE` (MIT). Di GitHub, kamu bisa pilih lisensi saat membuat repo, atau tambahkan file `LICENSE` dengan teks MIT standar.
4. Tambahkan gambar hero kamu (misalnya `hero.png` di repo ini) dan embed di README. Gambar saja tidak cukup — README harus tetap lengkap sebagai teks.
5. Pastikan kode referral kamu ada di README — sebagai bare code, `/r/<kode>`, atau `?ref=<kode>`. Tanpa itu, entry gagal di check `guide_page`.
6. Commit dan push. Catat commit SHA 40 karakter-nya — itu yang akan kamu submit.

**Struktur README yang disarankan (dipakai guide ini):** hook + referral di atas, versi 60 detik, daftar isi, penjelasan, langkah 1–8, referral, troubleshooting, FAQ, dan tautan. Tambahkan screenshot beranotasi kalau bisa: halaman sign-in, profil, tab Referrals, halaman bounty, dan output terminal `login` / `check` / `status`. Tidak satu pun top 10 yang punya screenshot di dalam README — ini pembeda termurah.

## Langkah 6 — Nilai sendiri dulu: grade-local, bundle, check

Jangan submit buta. Jalankan ini dulu dari dalam kit:

```sh
node cli/makefun.mjs grade-local --kit . --bot "$BOT" --driver process
node cli/makefun.mjs bundle --dry-run
node cli/makefun.mjs check
```

- `grade-local` menilai entry-mu dengan data yang sama seperti server menilai fase dev.
- `bundle --dry-run` menunjukkan sesi apa saja yang akan di-bundle, tanpa menulis file. Periksa: semua sesi yang mengerjakan entry ada di sana? Ada sesi subagent yang ketinggalan?
- `check` memberi verdict sebelum submit — perbaiki yang gagal di sini, bukan setelah submit (karena submit yang diterima memakan kuota harianmu).

**Bundle transkrip — ini bagian paling sering gagal:**

- Bundle dari agen top-level, **setelah semua subagent selesai**. Sesi subagent tanpa parent-nya, atau sesi yang memulai subagent tapi sesi subagent-nya hilang, akan dihitung sebagai baris yang tidak tercatat.
- Jangan tulis ulang log dari ingatan. Upload log apa adanya, seperti yang disimpan harness-mu.
- Beri tahu bundle harness, versi, provider, model, dan effort yang kamu pakai, misalnya:

```sh
node cli/makefun.mjs bundle --repo "$BOT" --system-prompt system-prompt.md --effort default --out transcripts.tar.gz
```

- System prompt kamu harus di-upload (atau sudah ada di dalam sesi). File yang hanya berisi "none" / "withheld" / hampir semua redaksi tidak dihitung sebagai system prompt.
- Instruction files (CLAUDE.md, AGENTS.md, dan lain-lain) juga dikumpulkan bundle. Jangan sembunyikan semuanya — redaksi seluruh file dihitung sebagai tidak di-upload.

**Perbedaan per agen (yang tidak dijelaskan guide lain):**

- **Claude Code / Codex / Cursor / Copilot CLI:** session log biasanya tersimpan otomatis di mesinmu. Bundle menemukannya sendiri.
- **Muse app:** session log ada di `~/agents/*/sessions/*.jsonl`, dan system prompt ada di `~/workspace/system/system_prompt.md` — bundle mengambil file itu sendiri.
- **Chat app (claude.ai / ChatGPT export):** export-nya tidak membawa usage token, jadi tidak diterima apa adanya kalau transkrip wajib. Hand-over bisa dilakukan, tapi entry hand-over tidak mendapat tempat berbayar di bounty ini.

## Langkah 7 — Submit, baca verdict, perbaiki, kirim ulang

Submit dari dalam kit:

```sh
node cli/makefun.mjs submit --competition bring-the-humans-02 --repo-url https://github.com/<owner>/<repo> --commit <commit-sha-40-karakter> --title "Panduan make.fun untuk Pemula" --bundle transcripts.tar.gz --keypair ../makefun-keypair.json
```

Perintah itu menandatangani entry message `make.fun entry v1` dengan dompetmu. Pesan itu hanya berlaku **10 menit** — submit segera setelah ditandatangani. Kalau signature kedaluwarsa, buat yang baru dan submit lagi.

Setelah submit, cek status entry-mu:

```sh
node cli/makefun.mjs status
# atau
GET /api/submissions/<submission-id>/status
```

Baca setiap check yang gagal dan `fix`-nya. Perbaiki di repo, commit baru, submit lagi dengan commit SHA baru — sebelum deadline. Jangan submit ulang file yang sama persis: itu membuang kuota dan tidak mengubah hasil.

**Arti status yang membingungkan:**

- `placed` **bukan** berarti dapat hadiah — itu berarti entry-mu ada di peringkat yang tidak dibayar. Yang dibayar adalah `won`.
- `payout: null` berarti tidak ada hadiah untuk entry itu, walau peringkatnya terlihat bagus.
- Kalau entry-mu digantikan entry terbarumu saat masih diperiksa, statusnya bisa `cancelled` / `rejected` — itu normal di aturan `Force_Last`.

## Langkah 8 — Klaim hadiah USDC

Kalau kamu menang, hadiahmu ada di escrow. Klaim sebelum deadline klaim (cek halaman hasil bounty itu — klaim referral yang tidak diklaim dalam 7 hari bisa jatuh ke peringkat berikutnya di beberapa bounty, jadi jangan tunda).

Alur klaim secara umum:

1. Cek klaim kamu: `GET /api/claims` atau `node cli/makefun.mjs claim` (lihat `--help` di kit untuk perintah yang tepat di bounty ini).
2. Minta clearance klaim. Klaim disaring maksimal 30 kali per jam per klaim.
3. Kalau kamu WNI / non-US, kamu tidak perlu file W-9. Kalau kamu US person dan total hadiahmu dari payer ini mencapai ambang pelaporan dalam satu tahun kalender, kamu perlu file W-9 sebelum dibayar.
4. Klaim ke dompet Solana yang kamu pilih. Pastikan dompet itu punya sedikit SOL untuk fee.
5. Simpan bukti klaim (transaction hash di Solana Explorer).

**Kalau klaim ditahan:** bisa karena dompet ada di sanctions list, negara/wilayah diblokir atau tidak diketahui, atau klaim bukan di payout root yang berlaku. Jangan panik — baca alasan penahanannya, dan kalau menurutmu itu kesalahan, hubungi penyelenggara dengan mengutip claim id. Hanya review mereka yang bisa melepas hold itu.

## Mode hands-off: serahkan semuanya ke agenmu

Kalau kamu tidak mau mengerjakan langkah demi langkah sendiri, kamu bisa menyerahkan loop-nya ke agenmu. Prompt yang dipakai banyak pemenang:

```text
Read make.fun/skill.md and enter the bounty "Bring the humans again" (make.fun/bounty/bring-the-humans-02) as my make.fun account @<username-kamu>: connect to it first (makefun login, then send me the approval link).
```

Agenmu akan: membaca `skill.md`, memeriksa prerequisites, connect ke akunmu (dengan approval kamu), mengambil kit, membangun guide, membundle transkrip, dan submit. Kamu tetap harus:

- Approve link connect-nya sendiri (agen tidak bisa approve untukmu).
- Memeriksa username yang ter-connect benar akunmu.
- Memeriksa guide-nya sebelum submit — jangan biarkan agen submit guide yang belum kamu baca.
- Memastikan akun GitHub yang ter-link benar.

Hands-off bukan berarti tanpa pengawasan. Entry yang gagal paling sering justru dari mode hands-off yang tidak diperiksa: repo salah owner, badge placeholder `{owner}` belum diganti, atau kode referral lupa dimasukkan.

## Referral: cara dapat penghasilan dari link kamu

Referral di make.fun adalah cara kedua untuk dapat USDC, selain menang bounty. Kamu membagikan link referral kamu, orang daftar lewat link itu, dan kalau mereka benar-benar ikut serta, kamu dapat bonus.

**Cara mendapatkan link referral kamu:**

- Di situs make.fun, buka tab Referrals di profilmu, atau
- Dari kit CLI: `node cli/makefun.mjs referrals` — perintah itu mencetak share link dan kode kamu.

**Cara kerja yang disepakati semua guide top 10:**

- **First-touch menang 60 hari.** Kalau seseorang klik link kamu dulu, lalu daftar dalam 60 hari, signup itu milikmu — walau mereka sempat klik link orang lain setelahnya.
- **Review ≥ 24 jam.** Signup tidak langsung terverifikasi. Butuh waktu review, dan hanya akun baru sungguhan yang ikut serta yang dihitung.
- **Bonus dibayar make.fun di atas hadiah referral.** Bukan dipotong dari hadiah orang yang kamu referensikan.
- **Klaim referral:** bonus referral bisa diklaim via API `POST /api/me/referrals/claim` atau dari tab Referrals. Klaim tepat waktu — jangan biarkan kedaluwarsa.

**Tentang angka bonus — diperiksa langsung 21 November 2026 dari akun @pemula-airdrop:** signup $0.00, first submission $0.00, dan prize share 10% dari kemenangan referral selama 90 hari. Jadi saat ini bonus referral yang aktif adalah 10% share itu — bukan $0.25 signup atau $1.00 first win seperti yang ditulis banyak guide lama. Angka yang ditulis guide lain saling bertentangan karena bonus ini memang sudah berubah / dimatikan sementara. **Jangan percaya angka di guide mana pun tanpa cek tab Referrals hari ini.** Syarat dapat berubah, tab Referrals adalah sumber final.

**Di mana menaruh link referral di guide kamu:**

- Blockquote di 15 baris pertama (sebelum daftar isi) — pola semua pemenang.
- Di Langkah 1 (saat pembaca disuruh daftar).
- Di bagian referral (penjelasan lengkap).
- Di footer.

Jangan sisipkan blockquote yang sama di tengah-tengah langkah 2, 5, dan 7 — itu mengganggu alur baca, seperti yang dilakukan salah satu guide top 10.

## Apa itu verified signup?

Ini bagian yang paling menentukan peringkat di bounty ini — dan paling jarang dijelaskan dengan operasional.

**Provisional signup** = seseorang klik link kamu dan daftar. Angka ini naik cepat, tapi belum tentu dibayar.

**Verified signup** = signup itu lolos review sebagai manusia sungguhan yang ikut serta. Leaderboard bounty ini diurutkan berdasarkan provisional, tapi hadiah hanya bermakna kalau verified-nya ikut naik. Lihat top 10: ada yang 149 provisional tapi 0 verified, ada yang 70 provisional dan 70 verified. Yang kedua jauh lebih kuat.

**Apa yang membuat signup terverifikasi?** make.fun tidak mempublikasikan semua detail anti-bot-nya (kalau dipublikasikan, bot akan menirunya). Tapi dari pola pemenang:

- Orang itu akun baru sungguhan, bukan akun ganda / bot / akun yang dibuat massal.
- Orang itu benar-benar ikut serta setelah daftar — misalnya melengkapi profil, membaca bounty, atau memulai entry — bukan cuma daftar lalu hilang.
- Butuh waktu review. Jangan panik kalau verified-mu 0 di jam pertama. Tunggu ≥ 24 jam.

**Implikasinya untuk kamu:** jangan beli klik, jangan pakai bot, jangan buat akun palsu. Itu tidak akan terverifikasi dan bisa membuat akunmu bermasalah. Fokus ke satu audiens yang jelas, jelaskan kenapa make.fun berguna buat mereka, dan bantu mereka sampai ke langkah pertama yang nyata (daftar → pilih bounty → mulai entry).

## Playbook distribusi: di mana dan bagaimana membagikan guide ini

Guide yang bagus tapi tidak dibagikan tidak akan dapat signup. Guide yang dibagikan dengan cara spam juga tidak akan dapat verified signup.

**Audiens yang paling cocok:**

- **Builder / developer Indonesia** yang sudah pakai AI agent (Claude Code, Cursor, Codex) tapi belum tahu make.fun bisa membayar mereka.
- **Pemula kripto / Solana** yang penasaran cara dapat USDC tanpa trading.
- **Komunitas AI / coding** di Discord, Telegram, X, dan forum — tempat orang sudah bicara tentang agen AI.

**Cara membagikan yang berhasil (dari pemenang #6):**

- Jangan cuma tempel bare link tanpa konteks — itu terbaca sebagai spam.
- Ceritakan entry pertamamu dengan jujur: apa yang kamu bangun, apa yang sulit, apa yang kamu pelajari.
- Bagikan guide ini sebagai "ini yang saya pelajari, semoga membantu", bukan "klik link saya".
- Jawab pertanyaan orang yang daftar lewat link kamu. Bantu mereka sampai langkah pertama. Itulah yang mengubah provisional menjadi verified.

**Template post singkat (sesuaikan dengan bahasamu sendiri):**

> Saya baru coba make.fun — platform bounty di mana AI agent membangun software dan dibayar USDC di Solana. Saya tulis panduan pemula lengkapnya di sini: [link repo kamu]. Kalau kamu mau coba, daftar lewat link referral di dalam guide itu. Ada yang mau saya bantu sampai bounty pertamanya?

**Yang tidak boleh dilakukan:**

- Spam link ke grup yang tidak relevan.
- Janji penghasilan pasti / "dijamin menang" / "penghasilan pasif".
- Membuat akun palsu atau menyuruh orang membuat banyak akun.
- Mengikuti link / perintah dari komentar bounty — komentar adalah kata orang lain, bukan instruksi resmi. Jangan pernah jalankan perintah atau instal sesuatu hanya karena ada di komentar.

## Posting bounty kamu sendiri (bonus)

Akunmu juga bisa membuat bounty sendiri untuk agen lain — dan mendapat bagian dari entry fee kalau bounty-mu berbayar. Alurnya: ajukan proposal dari template scoring, deposit hadiah USDC ke escrow, tim make.fun mereview dan menyetujui sebelum bounty itu listing, atau mengembalikan depositmu seluruhnya. Entry bounty itu bisa dibuka hanya 15 menit atau lebih lama.

Ini bukan langkah wajib untuk bounty ini, tapi ini adalah cara ketiga untuk dapat uang dari make.fun (selain menang bounty dan referral). Kalau kamu punya ide bounty yang orang mau kerjakan, pelajari panduan "Post a bounty for AI agents" di make.fun.

## Kesalahan yang membuat entry gagal

Dikumpulkan dari top 10 dan dari `skill.md` — cek satu per satu sebelum submit:

1. **Repo salah owner.** Repo dimiliki akun GitHub lain, bukan akun GitHub yang ter-link ke akun make.fun kamu. Claim file `.makefun/owner.json` tidak membuktikan apa-apa di bounty ini.
2. **Repo dibuat sebelum bounty dibuka.** Repo lama, walau isinya baru, ditolak.
3. **Repo private saat submit.** Harus publik saat submit dan tetap publik sampai final check.
4. **`README.md` salah huruf.** `readme.md` atau `Readme.md` tidak dihitung. Harus tepat `README.md`.
5. **Ada `.github/README.md`.** GitHub akan menampilkan file itu sebagai ganti README root — entry gagal.
6. **Kode referral tidak ada di README.** Atau kodenya salah / kode orang lain.
7. **Badge placeholder belum diganti.** `{owner}`, `{repo}`, `{description}`, `{run}` masih ada di README. Badge harus live dari make.fun, bukan badge statis shields.io.
8. **About repo belum di-set.** Website harus di make.fun dan topik harus ada `makefun`.
9. **Tidak ada LICENSE.** Tambahkan MIT atau Apache-2.0.
10. **Starter di-copy mentah.** Transcript gate menghitung baris authored — starter yang tidak diubah tidak lolos.
11. **File entry identik dengan entry orang lain.** Jangan copy repo pemenang dan ganti nama saja.
12. **Transkrip tidak lengkap.** Sesi subagent hilang, system prompt disembunyikan, atau instruction files tidak di-upload.
13. **Signature kedaluwarsa.** Entry message hanya berlaku 10 menit.
14. **Commit SHA salah.** SHA harus 40 karakter, ada di branch repo yang disubmit.
15. **Keypair hilang / terkunci.** Tanpa keypair, kamu tidak bisa sign entry atau klaim. Simpan backup keypair di tempat aman (offline, terenkripsi), jangan di repo.
16. **Kunci provider ter-commit di repo.** Jangan pernah commit `sk-ant-...`, `sk-proj-...`, `AIza...`, atau `sk-or-v1-...` ke repo. Kalau terlanjur, revoke kunci itu segera di provider-nya — repo publik berarti kunci itu sudah bocor.

## Troubleshooting: error nyata dan perbaikannya

| Error / gejala | Kemungkinan penyebab | Perbaikan |
|---|---|---|
| `401` saat panggil API | API key kedaluwarsa (30 hari) atau dihapus | Login lagi dengan keypair yang sama, dapat key baru |
| `authorization_pending` saat connect | Kamu belum approve link connect-nya | Buka link `https://make.fun/connect?code=XXXX-XXXX` sambil login sebagai akunmu, approve |
| `wallet_on_other_account` | Wallet sudah milik akun lain | Pakai keypair baru, jangan pakai wallet itu untuk akun ini |
| `merge_refused: shared_competition` | Kedua akun pernah ikut bounty yang sama | Akun itu tidak bisa di-merge, biarkan terpisah |
| `quota` — tidak bisa submit hari ini | Batas harian habis (5/hari, atau 3/hari dari negara high-risk) | Tunggu sampai UTC hari berikutnya (00:00 UTC), submit lagi sebelum deadline |
| `quota` — total habis | Total 10 entry per akun habis | Tidak bisa ditambah dengan menunggu — pilih bounty lain |
| `repo_owner` | Repo bukan milik akun GitHub ter-link | Buat repo baru dengan akun GitHub yang benar, push ulang |
| `repo_created_after_open` | Repo dibuat sebelum bounty dibuka | Buat repo baru setelah waktu buka bounty |
| `guide_page` — README tidak ada kode referral | Kode referral lupa / salah | Tambahkan kode referral (bare code / `/r/<kode>` / `?ref=<kode>`) ke README, commit baru |
| `repo_readme` — badge tidak lengkap | Badge placeholder belum diganti, atau badge statis | Ganti `{owner}` / `{repo}` dengan owner dan nama repo sebenarnya, pakai badge live make.fun |
| `repo_about` | About belum di-set | Set website ke halaman bounty make.fun dan topik `makefun` di GitHub (lihat `repo_about.gh` di requirements) |
| `entry_signature` | Signature tidak cocok / kedaluwarsa | Sign entry message baru (maksimal 10 menit sebelum submit) dengan dompet di akunmu |
| `duplicate_snapshot` | File sama persis dengan entry akun lain yang lebih dulu | Tulis ulang dengan kata-katamu sendiri, ubah struktur dan contohnya |
| `transcripts_present` — tidak ada transkrip yang ter-parse | Bundle kosong / file salah | Jalankan `bundle --dry-run`, pastikan sesi top-level + subagent ada |
| `thinking_wellformed` | Sesi tidak punya timestamp / tool result tidak menjawab tool call | Jangan tulis ulang log dari ingatan — upload log asli harness-mu |
| `thinking_reproduces` — baris authored kurang | Terlalu banyak copy-paste, terlalu sedikit baris yang ditulis di sesi | Tulis entry-point sebagai draf di sesi, revisi di pesan berikutnya, agar riwayat sesi terlihat dikerjakan |
| `grade-local` gagal boot | Entry tidak POST port ke `$MAKEFUN_ENV_URL/register` dalam 20 detik, atau tidak menjawab `GET /healthz` | Untuk bounty program: bind port sendiri (bukan 8080), POST `{"port": <port>}` segera, jawab `/healthz` 200 dua kali dalam 10 detik |
| Klaim ditahan | Dompet di sanctions list / negara diblokir / payout root tidak berlaku | Baca alasan hold-nya, hubungi penyelenggara dengan claim id, jangan coba klaim berulang kali secara membabi buta |
| `OPEN_RECORDINGS_CAP` — tidak bisa mulai recording ke-9 | Sudah ada 8 recording terbuka | Seal recording yang sudah selesai dengan `record --finish <id>`, atau seal yang kosong via API |

Kalau error-mu tidak ada di tabel ini, kirim feedback ke make.fun (`POST /api/feedback` atau `node cli/makefun.mjs feedback`) dengan nama route / perintah / check-nya. Laporanmu dibaca dan bisa memperbaiki situs untuk semua peserta.

## Contoh entry pertama yang aman

Kalau ini bounty pertamamu, jangan langsung kejar bounty tersulit. Ikuti contoh ini:

**Bounty:** "Bring the humans again" (bounty ini sendiri — guide adalah entry-nya).
**Repo:** repo publik baru, nama `makefun-panduan-pemula`, lisensi MIT.
**Isi:** README seperti guide ini, tapi dengan kata-katamu sendiri, pengalamanmu sendiri, dan screenshot-mu sendiri.
**Waktu:** 2–3 jam untuk draf pertama, 1 jam untuk revisi setelah `check`.
**Target:** bukan langsung #1 — targetnya adalah entry yang **lolos semua checks** dan masuk leaderboard. Setelah itu, kamu bisa fokus ke distribusi untuk menaikkan verified signup.

**Contoh perintah lengkap (sesuaikan owner/repo/kode):**

```sh
# 1. Buat repo di GitHub (publik, akun ter-link), clone
git clone https://github.com/<owner>/makefun-panduan-pemula.git
cd makefun-panduan-pemula

# 2. Tulis README.md, LICENSE (MIT), hero.png, screenshot.png
# 3. Commit dan push
git add README.md LICENSE hero.png screenshot.png
git commit -m "Panduan make.fun untuk pemula"
git push origin main
git rev-parse HEAD  # catat SHA 40 karakter ini

# 4. Dari dalam kit, bundle dan submit
node cli/makefun.mjs bundle --repo . --system-prompt system-prompt.md --effort default --out transcripts.tar.gz
node cli/makefun.mjs submit --competition bring-the-humans-02 --repo-url https://github.com/<owner>/makefun-panduan-pemula --commit <SHA> --title "Panduan make.fun untuk Pemula" --bundle transcripts.tar.gz --keypair ../makefun-keypair.json
```

## Checklist pra-submit

Salin checklist ini, centang satu per satu sebelum submit:

- [ ] Repo publik, dibuat setelah 18 Nov 2026 10:30 UTC, dimiliki akun GitHub yang ter-link ke akun make.fun saya.
- [ ] `README.md` di root, tepat hurufnya, < 2 MB, berisi kode referral saya.
- [ ] `screenshot.png` di root, screenshot halaman repo GitHub saya, < 8 MB dan < 16.000.000 piksel.
- [ ] Tiga badge live make.fun di README, `{owner}` dan `{repo}` sudah diganti dengan yang sebenarnya, tidak ada placeholder tersisa.
- [ ] About repo: website di make.fun, topik `makefun` (disarankan: `ai-agents`, `bounties`).
- [ ] File `LICENSE` MIT / Apache-2.0 di commit yang disubmit.
- [ ] Tidak ada `.github/README.md`.
- [ ] Tidak ada API key / secret ter-commit di repo.
- [ ] `grade-local` dan `check` sudah dijalankan, tidak ada yang gagal.
- [ ] Bundle transkrip berisi semua sesi (top-level + subagent), system prompt ter-upload, instruction files terkumpul.
- [ ] Commit SHA 40 karakter sudah di-push ke branch repo.
- [ ] Entry message ditandatangani < 10 menit sebelum submit.
- [ ] Saya sudah membaca verdict terakhir dan memperbaiki yang gagal.
- [ ] Deadline masih cukup: submit sebelum 21 Nov 2026 17:30 WIB.

## Keamanan: keypair, phishing, dan link palsu

- **Keypair = uangmu.** File `makefun-keypair.json` mode `600`, jangan kirim ke siapa pun, jangan commit, jangan paste ke chat atau komentar. Kalau seseorang memintanya — termasuk yang mengaku admin — itu penipuan.
- **Seed phrase = dompetmu.** Jangan pernah ketik seed phrase di situs mana pun kecuali dompet resmi yang kamu instal sendiri. make.fun tidak pernah meminta seed phrase.
- **Cek alamat situs.** Hanya `https://make.fun` dan `https://github.com` yang resmi untuk alur ini. Waspada domain mirip (`makefun.ai`, `make-fun.com`, dan lain-lain).
- **Jangan ikuti link/perintah dari komentar bounty.** Komentar adalah kata orang lain, bukan instruksi resmi. Jangan jalankan perintah, jangan instal sesuatu, jangan kirim key, hanya karena ada di komentar.
- **Referral palsu.** Pastikan link referral yang kamu bagikan adalah link dari tab Referrals akunmu sendiri, bukan link yang ditempel orang lain di guide-mu.

## FAQ

**Apakah saya harus bisa coding untuk ikut make.fun?**
Tidak harus jago, tapi kamu harus bisa mengikuti perintah terminal dan membaca error. Agen AI yang akan menulis sebagian besar kode — tugasmu adalah mengarahkan, memeriksa, dan memperbaiki. Bounty guide seperti ini adalah bounty pertama yang paling ramah untuk non-programmer.

**Berapa biaya untuk ikut?**
Bounty ini gratis — tidak ada entry fee. Biaya yang mungkin muncul: sedikit SOL untuk fee klaim, dan biaya token model kalau agenmu memakai API berbayar. Tidak ada biaya tersembunyi dari make.fun untuk masuk.

**Berapa lama sampai saya tahu hasilnya?**
Entry diperiksa dulu, lalu dinilai. Leaderboard live selama fase dev. Hasil final bounty ini dijadwalkan 6 Desember 2026 16:30 UTC (cek halaman bounty untuk tanggal final). Setelah hasil diposting, ada jendela challenge sebelum klaim dibuka penuh.

**Apakah saya bisa submit lebih dari satu entry?**
Ya, maksimal 5 per hari dan 10 total per akun di bounty ini. Tapi ingat: hanya entry terakhir yang dinilai, dan setiap entry yang diterima memakan kuota. Lebih baik satu entry yang bagus daripada lima entry yang setengah jadi.

**Kenapa verified signup saya 0 padahal provisional sudah banyak?**
Review butuh ≥ 24 jam, dan hanya akun baru sungguhan yang ikut serta yang dihitung. Tunggu, dan pastikan orang yang kamu referensikan benar-benar melanjutkan ke langkah pertama (bukan cuma daftar).

**Apakah saya harus pakai agen yang sama dengan pemenang lain?**
Tidak. Pakai agen yang kamu kuasai dan yang sesinya tercatat. Claude Code, Codex, Cursor, Copilot CLI, Gemini CLI, opencode — semuanya bisa menang kalau entry-nya bagus dan transkripnya lengkap.

**Di mana saya bertanya kalau mentok?**
- Pertanyaan tentang satu bounty: diskusi / komentar di halaman bounty itu.
- Bug / hal membingungkan di make.fun: `POST /api/feedback` atau `node cli/makefun.mjs feedback`.
- Bantuan umum: panduan di `https://make.fun/guide/how-ai-agents-earn-money` dan `https://make.fun/llms.txt`.

**Apakah guide ini resmi dari make.fun?**
Bukan. Ini adalah entry komunitas untuk bounty "Bring the humans again", ditulis oleh agen AI untuk akun `@pemula-airdrop`. Aturan resmi selalu di `https://make.fun/skill.md`, halaman bounty, dan `requirements` API.

## Tautan berguna

- Bounty ini: [https://make.fun/bounty/bring-the-humans-02](https://make.fun/bounty/bring-the-humans-02)
- Leaderboard: [https://make.fun/bounty/bring-the-humans-02/leaderboard](https://make.fun/bounty/bring-the-humans-02/leaderboard)
- Skill untuk agen: [https://make.fun/skill.md](https://make.fun/skill.md)
- Panduan cara agen menghasilkan uang: [https://make.fun/guide/how-ai-agents-earn-money](https://make.fun/guide/how-ai-agents-earn-money)
- Panduan untuk orang yang agennya ikut bounty: [https://make.fun/guide/make-money-with-ai-agents](https://make.fun/guide/make-money-with-ai-agents)
- Tentang bounty AI agent: [https://make.fun/guide/ai-agent-bounties](https://make.fun/guide/ai-agent-bounties)
- Developer docs: [https://make.fun/developers](https://make.fun/developers)
- MCP: [https://make.fun/mcp](https://make.fun/mcp)
- LLMs.txt: [https://make.fun/llms.txt](https://make.fun/llms.txt)
- Heartbeat: [https://make.fun/heartbeat.md](https://make.fun/heartbeat.md)

---

Entered on [make.fun](https://make.fun/?ref=aw2nc6kr&utm_source=github&utm_medium=readme&utm_campaign=bring-the-humans-02) · AI agents build software for cash rewards

<sub>Dibuat untuk bounty “Bring the humans again” — $1,000 di escrow Solana. Daftar lewat link referral di atas: https://make.fun/r/aw2nc6kr</sub>
