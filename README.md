# Dimas Adrian Haifa Arfan: Personal Website

A simple website built with [Astro](https://astro.build). All content lives in Markdown files, so you update the site by editing text, not code.
Website sederhana dengan Astro. Semua isi ada di file Markdown, jadi kamu mengubah isi cukup dengan mengedit teks.

---

## 1. Put it online / Cara memasang online (once / sekali saja)

1. Create a GitHub account and a **new public repository** named `USERNAME.github.io` (use your real username).
   Buat akun GitHub dan repository publik baru bernama `USERNAME.github.io`.
2. `astro.config.mjs` is already set for `dimasadrian17/portofolio`. If you use another repository, edit `site` and `base` there.
   Buka `astro.config.mjs`, ganti `USERNAME` dengan username GitHub kamu.
3. Upload every file and folder of this project to the repository (GitHub: *Add file → Upload files*, or use Git).
   Unggah semua file dan folder proyek ini ke repository.
4. In the repository go to **Settings → Pages → Source** and choose **GitHub Actions**.
   Di repository: **Settings → Pages → Source**, pilih **GitHub Actions**.
5. Wait 1 to 3 minutes. Your site is at `https://USERNAME.github.io`. Check progress in the **Actions** tab.
   Tunggu 1–3 menit. Website ada di `https://USERNAME.github.io`. Lihat progres di tab **Actions**.

> If you name the repository something else (for example `portfolio`), add `base: '/portfolio',` in `astro.config.mjs`.
> Kalau nama repository berbeda, tambahkan `base: '/nama-repo',` di `astro.config.mjs`.

Every time you save (commit) a change on the `main` branch, the site rebuilds and updates by itself.
Setiap kali kamu menyimpan (commit) perubahan di branch `main`, website otomatis diperbarui.

## 2. How to update content / Cara update isi

You can edit directly on github.com: open a file, click the pencil icon, edit, then **Commit changes**.
Kamu bisa mengedit langsung di github.com: buka file, klik ikon pensil, edit, lalu **Commit changes**.

| I want to / Saya ingin | Where / Lokasi |
|---|---|
| Change the home text / Ubah teks Home | `src/pages/index.astro` |
| Change About text and skills | `src/content/about/` |
| Add a job, organization, or competition | `src/content/experience/` |
| Add a project | `src/content/projects/` |
| Add a certificate | `src/content/certificates/` + image in `public/img/certs/` |
| Add a Medium article or YouTube video | `src/content/writing/` |
| Change contact details | `src/pages/contact.md` |

Files are shown in **file-name order**, so start names with a number (`13-my-new-article.md`).
Urutan tampil mengikuti **nama file**, jadi awali nama dengan angka.

### Add a Medium article or video / Tambah artikel atau video
Copy any file in `src/content/writing/`, rename it (for example `13-my-new-article.md`) and edit:

```
---
type: "Article"            # Article or Video
title: "My new write-up"
date: "26 Oct 2026"        # optional
tags: ["Cybersecurity"]    # Cybersecurity, Network, Telecommunications, Fiber optic
url: "https://medium.com/@dimasarfan62/..."
thumb: "img/writing/my-thumbnail.jpg"   # optional image in public/img/
blurb: "One sentence about it."
---
```

### Add a certificate / Tambah sertifikat
Put the image (JPG, about 1300 px wide) in `public/img/certs/`, then copy a file in `src/content/certificates/`:

```
---
category: "Webinars"       # Competitions, Bootcamps, Courses, or Webinars
title: "Name of the certificate"
issuer: "Who gave it"
date: "5 Nov 2026"
tag: "Participant"         # optional label
image: "img/certs/my-certificate.jpg"
---
```

### Add a job, project, or competition / Tambah pekerjaan atau proyek
Copy a file in `src/content/experience/` (or `projects/`). The text below the `---` lines is the description. Use `- ` for bullet points.

```
---
section: "Organizations"   # heading; rows with the same section are grouped
when: "Jan – May 2027"
title: "Role, Company"
where: "Surabaya"          # optional
photos: [{"src":"img/experience/my-photo.jpg","caption":"What the photo shows"}]
---
- First thing I did.
- Second thing I did.
```

## 3. Preview on your computer (optional) / Pratinjau di komputer (opsional)

Install [Node.js](https://nodejs.org) 20 or newer, then:

```
npm install
npm run dev
```

Open the address it shows (usually http://localhost:4321).

## 4. Tips

- Resize photos before adding them (about 1200 px on the long side, JPG). Big files make the site slow.
  Kecilkan foto sebelum ditambahkan (sekitar 1200 px, JPG) agar website tidak lambat.
- Keep `package-lock.json` in the repository; the deploy workflow uses it.
- Do not publish your phone number on a public site if you want to avoid spam.
