# Instalasi

```bash
npx degit mzaini30/svelte my-project
cd my-project
npm i
```

# Struktur folder

| Keterangan | Folder |
|---|---|
| File Svelte | src/pages |
| Static files | public |
| Output | hasil |

# Fitur

## Code splitting

Cukup jalankan 

```bash
npm run build
```

## Router berbasis file

Kita menggunakan Routify.

## Hot module reload

Dia nggak mereset state saat kita development. Cukup jalankan:

```bash
npm run dev
```

## Bootstrap

Udah ada Bootstrap. Tinggal pakai aja.

## SEO

Ini isi dari `public/index.html`:

```html
<!DOCTYPE html>
<html lang="en">
<head>
	<meta charset='utf-8'>
	<meta name='viewport' content='width=device-width,initial-scale=1'>

	<title></title>
	<meta name="description" content="">
	<meta property="og:image" content="favicon.png">

	<link rel='icon' type='image/png' href='favicon.png'>
	<link rel='stylesheet' href='bootstrap.min.css'>
	<link rel='stylesheet' href='global.css'>
	<link rel='stylesheet' href='build/bundle.css'>

	<script defer src='main.js' type="module" ></script>
</head>

<body>
</body>
</html>
```

Nanti tinggal disesuaikan aja tag title, meta description, dan og image.

## Loader

Cara menggunakan:

```javascript
import {isLoading} from '@/store'
$isLoading = true // untuk mengaktifkan loader
$isLoading = false // untuk mematikan loader
```

Itu harus diletakkan di dalam folder `halaman`.

## Absolute path

Contoh:

```javascript
import {nama} from '@/data/nama'
```

Tapi, bisa juga relative path seperti:

```javascript
import {nama} from '../../../nama'
```

## Tanggal

Mendapatkan tanggal terkini dengan format 2020-08-17 00:19:45

Caranya:

```html
<script>
	import {tanggal} from '@/tanggal'
</script>
<p>{tanggal()}</p>
```

# Terjemahan?

Boleh. Misalnya aja mau nerjemahkan ke bahasa Jepang, maka buat file `README-jp.md` yang berisi terjemahan README ini dalam bahasa Jepang.
