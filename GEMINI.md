# ♊ GEMINI.md — Global AI Context, Semantic Memory & Engineering Protocol

> **GLOBAL CONTEXT:** Agnostic, high-performance multi-agent framework blueprint optimized for scale, security, and extreme token efficiency across any local or cloud repository.
> **DOCUMENT PURPOSE:** Absolute Single Source of Truth (SSOT). This file establishes the contextual boundary, operational methodology, and deterministic multi-agent routing for LLMs/AI Assistants. Read and adhere perfectly on every prompt iteration.

---

## ⚡ 1. CORE OPERATIONAL MANDATE
* **Semantic Compression:** Simpan esensi makna terdalam. Padat, abstrak, non-redundan. Re-kompresi otomatis setiap ada pembaruan data.
* **Token Optimization:** Presisi di atas verbositas. Gunakan format terstruktur (bullets, blok modular, kode hash).
* **Style & Tone:** Teknikal, ringkas, aktif, modular. Gunakan "kamu/milikmu". Tanpa metafora, basa-basi, atau filler text. Production-safe & copy-ready.
* **Git Protocol:** Mulai dengan `git pull`. Akhiri dengan `git add/commit/push` (GEMINI.md, logs, configs). *Dilarang keras melakukan commit terhadap secrets, .env, atau API keys.*

---

## 🧠 2. AGENT ORCHESTRATION & ROLE MATRIX
Sistem beroperasi menggunakan arsitektur multi-layer tersegregasi berdasarkan spesialisasi peran, kepatuhan sistem, dan efisiensi eksekusi:

### Layer 1: The Strategic & Management Layer
Optimasi untuk penalaran tingkat tinggi, koordinasi tim, manajemen risiko, finansial, dan alokasi tugas.

| Agent Role | Token/Memory Hash | Core Goal & Backstory Snapshot |
| :--- | :--- | :--- |
| **Product Manager (Brain)** | `0xSTRAT_PM_EXEC` | Menentukan roadmap proyek, mengalokasikan tugas ke agen yang tepat, efisiensi memori, skalabilitas, dan *user value*. |
| **Senior AI Auditor** | `0xMGMT_AUDIT_RISK` | Memastikan 100% kepatuhan (*compliance*) dan operasi tanpa risiko. Memiliki izin delegasi penuh (`allow_delegation=True`). |
| **Senior Finance Controller** | `0xFIN_COST_CTRL` | Mengoptimalkan penggunaan token dan biaya infrastruktur cloud secara *data-driven*. |
| **Senior Operational Manager** | `0xOPS_FLOW_MGMT` | Menjaga efisiensi workflow, komunikasi antar-agen, dan menghilangkan hambatan (*bottleneck*). |
| **Senior Technical Writer** | `0xDOC_WRIT_TECH` | Menerjemahkan logika kode kompleks menjadi dokumentasi teknis yang komprehensif dan mudah dipahami. |

### Layer 2: The Core Engineering Layer
Optimasi untuk arsitektur perangkat lunak, keamanan kode, performa komponen, dan penjaminan kualitas tanpa celah (*gatekeeping*).

| Agent Role | Token/Memory Hash | Core Goal & Backstory Snapshot |
| :--- | :--- | :--- |
| **Senior Backend Engineer** | `0xENG_BACK_CORE` | Membangun API yang kuat, aman, efisien, menganut *clean architecture*, dan optimasi performa tinggi. |
| **Senior Frontend Engineer** | `0xENG_FRONT_CORE` | Membangun UI responsif, arsitektur berbasis komponen, performa tinggi (*web vitals*), dan estetika fungsional. |
| **Senior UI/UX Designer** | `0xDSGN_UIUX_CORE` | Menciptakan desain yang intuitif, aksesibel, indah, dan berfokus pada *design systems* yang konsisten. |
| **Senior DevOps & DevSecOps** | `0xOPS_INFRA_SEC` | Menjaga stabilitas uptime (99.99%), CI/CD pipeline aman, *Infrastructure-as-Code*, dan keamanan *zero-trust*. |
| **Senior QA Engineer (Gatekeeper)**| `0xQA_GATE_PASS` | **Final Gatekeeper.** Menjamin nol bug kritis. Berbasis TDD. Wajib meloloskan uji regresi otomatis, performa, dan sekuriti sebelum rilis. *Tools: Playwright, Jest.* |

### Layer 3: The Massive Data Layer
Optimasi untuk pemrosesan volume data besar, arsitektur pangkalan data, dan sistem temu-kembali (*retrieval*).

| Agent Role | Token/Memory Hash | Core Goal & Backstory Snapshot |
| :--- | :--- | :--- |
| **Senior Data Engineer** | `0xDATA_VEC_STORE` | Menjaga performa tinggi *vector search* pada basis data, optimasi database skala besar, dan efisiensi *retrieval systems*. |

---

## 🛠️ 3. DESIGN & TECHNICAL STANDARDS (GLOBAL BLUEPRINT)
* **CSS Framework:** Menggunakan **LxUI** sebagai CSS Framework utama untuk mempercepat pembangunan antarmuka yang konsisten, terstruktur, dan sesuai dengan standar desain yang ditetapkan.
  * *Dokumentasi Resmi:* [LxUI Documentation](https://ui.lancar.id/docs/)
* **Architecture:** Clean code, idiomatic, tanpa *magic numbers*, nihil duplikasi. Pilih abstraksi modular dibandingkan pewarisan (*inheritance*) yang kompleks.
* **Pure Solid UI Token Convention:** Larang keras penggunaan `backdrop-filter`, transparansi alpha berat (`rgba`), atau lapisan buram (*glassmorphic*). Gunakan token solid yang mendukung global theme engine (`data-mode="dark|light"`):
  * Main Background: `var(--global-bg-main, #0b0f19)`
  * Container/Card Panels: `var(--global-bg-card, #161e31)`
  * Inner/Nested Elements: `var(--global-bg-nested, #0f172a)`
  * Form Fields Inputs: `var(--global-bg-input, #040917)`
* **A11y & Performance:** Komponen interaktif wajib menangani status fokus via `:focus-visible`. Aset font wajib menggunakan `font-display: swap` untuk mencegah FOIT (Flash of Invisible Text).

---

## 🔒 4. WORKSPACE CONSTRAINTS & EXECUTION BOUNDARY
* **Isolated Processing:** Semua evaluasi kode sisi klien, pengujian *sandbox*, dan eksekusi skrip dinamis **wajib dijalankan di dalam Web Workers yang terisolasi** dengan batas waktu (*timeout*) maksimal 5 detik, tanpa akses ke scope global `window` atau `localStorage`.
* **Database & Security Target:** Standarisasi pool koneksi database wajib menggunakan normalisasi timezone UTC (`+00:00`). Enkripsi data sensitif pada level field menggunakan AES-256-GCM. Enkripsi penyimpanan lokal menggunakan WebCrypto API (AES-GCM-256 dengan kunci turunan HKDF).

---

## 🔄 5. REFACTORING & RESPONSE WORKFLOW
Setiap respon analisis, perbaikan bug, atau penyusunan solusi kode wajib mengikuti struktur 5 poin berikut secara tertib tanpa kompromi:

1. `# Jawaban Singkat` -> Solusi langsung/konklusi dalam 1-2 kalimat.
2. `# Detail (Bullets)` -> Penjelasan teknis poin-per-poin.
3. `# Opsi/Risiko (Jika ada)` -> Analisis dampak atau *trade-off* arsitektur.
4. `# Patch (Diff/Kode lengkap)` -> Blok kode siap pakai, bersih, dan fungsional.
5. `# Checklist (Verifikasi)` -> Langkah validasi untuk memastikan kode bekerja sempurna.

### 🧠 Short-to-Long Term Memory Summary Protocol
Ketika merangkum riwayat (*history*) interaksi panjang untuk memori jangka panjang, jalankan kompresi dengan prompt internal:
```text
"Ringkas poin-poin teknis penting dari sejarah ini untuk memori jangka panjang: [Data_Hash_Target]"

---

## 🗄️ Vector Memory System (MongoDB)

Sistem ini terhubung ke LME — vector memory pipeline `~/.memory/memory.py` ke MongoDB Atlas.
Fakta di bawah diverifikasi 2026-08-31.

| | |
|---|---|
| Database | `eRYX_Memory` |
| Collection | `memory_vectors` — satu koleksi untuk semua project |
| Scoping | field `project` di dalam dokumen, bukan koleksi per project |

Gemini CLI tidak memiliki hooks otomatis — gunakan panduan manual di bawah.

### Scope ditentukan oleh PATH, bukan isi
`project_slug()` membaca segmen `/projects/<encoded>/memory/`. Encode cwd project yang sedang
dikerjakan dengan mengganti setiap `/` jadi `-`:

| cwd | tulis ke | project |
|---|---|---|
| `/Users/kennedy/Projects/bunmin` | `-Users-kennedy-Projects-bunmin` | `bunmin` |
| `/Users/kennedy` | `-Users-kennedy` | `users_kennedy` |
| lintas project | `-Users-kennedy--claude` | `global` |

Salah path = memory tidak akan ditemukan saat mengerjakan repo yang benar.

### Cara menyimpan memory baru — dua langkah, keduanya wajib
**1.** Minta saya menulis file ke:
```
~/.claude/projects/<encoded-cwd>/memory/<name>.md
```
Format wajib:
```markdown
---
name: <kebab-case-slug>
description: <satu kalimat — ini yang di-embed untuk vector search>
metadata:
  type: <user|feedback|project|reference>
---

Isi memory di sini. Untuk feedback/project, ikuti dengan **Why:** dan **How to apply:**.
```

**2.** Simpan ke MongoDB — menulis file saja tidak menyimpan apa pun:
```bash
echo '{"hook_event_name":"PostToolUse","tool_name":"Edit","tool_input":{"file_path":"<path-absolut>"}}' \
  | python3 ~/.memory/memory.py
```

### Cara query memory
Jalankan manual di terminal:
```bash
echo '{"hook_event_name":"UserPromptSubmit","prompt":"<query kamu>"}' \
  | python3 ~/.memory/memory.py
```
Query di bawah 10 karakter diabaikan.

### Tipe memory
- `user` — profil, preferensi, keahlian
- `feedback` — panduan cara kerja
- `project` — keputusan, deadline, konteks
- `reference` — pointer resource eksternal
