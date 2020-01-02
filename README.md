## Github pages ortamında React uygulamalarını yayınlama

## Gerekli adımlar

React uygulamamızı github pages ortamında yayınlamak için bir takım işlemler gerekiyor.

### `npx create-react-app my-app`

Herzaman ki gibi react uygulamamızı oluşturuyoruz.
`cd my-app` komutu ile dizinin içine giriyoruz.

### `npm install gh-pages --save-dev`

Dizinimize geliştirme bağımlılığı olarak `gh-pages` reposunu ekliyoruz.

### `package.json dosyasını aşağıdaki şekilde düzenliyoruz.`

`"name"` satırının üzerine `"homepage": "githubkullaniciadi.github.io/uygulama-adi",` yazıyoruz.
`scripts` bölümünün içine;
`"predeploy": "npm run build",`
`"deploy": "gh-pages -d build,"` satırlarını ekliyoruz.

### `github.com üzerinden uygulama adımızla aynı bir repo oluşturuyoruz.`

Oluşturduğumuz repoyu localimizdeki uygulama klasörü ile eşleştiriyoruz. Ardından `git push -u origin master` komutu ile Github'a yüklüyoruz.

### `npm run deploy`

Bu komutu terminalimize yazdıktan sonra React uygulamamız Github pages ortamında yayınlanmaya başlamıştır.


**Not: Yukarıdaki adımları yapmakta zorlananlar için video kaynağı [Link](https://www.youtube.com/watch?v=BZidYA3dgXA).**


