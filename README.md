# Github pages ortamında React uygulamalarını yayınlama

Table of Contents
- [Github pages ortamında React uygulamalarını yayınlama](#github-pages-ortam%c4%b1nda-react-uygulamalar%c4%b1n%c4%b1-yay%c4%b1nlama)
  - [Gerekli adımlar](#gerekli-ad%c4%b1mlar)
    - [1- `npx create-react-app my-app`](#1--npx-create-react-app-my-app)
    - [2- `npm install gh-pages --save-dev`](#2--npm-install-gh-pages---save-dev)
    - [3- `package.json dosyasını aşağıdaki şekilde düzenliyoruz.`](#3--packagejson-dosyas%c4%b1n%c4%b1-a%c5%9fa%c4%9f%c4%b1daki-%c5%9fekilde-d%c3%bczenliyoruz)
      - [`"name"` satırının üzerine;](#%22name%22-sat%c4%b1r%c4%b1n%c4%b1n-%c3%bczerine)
      - [`scripts` bölümünün içine;](#scripts-b%c3%b6l%c3%bcm%c3%bcn%c3%bcn-i%c3%a7ine)
    - [4- `github.com üzerinden uygulama adımızla aynı bir repo oluşturuyoruz.`](#4--githubcom-%c3%bczerinden-uygulama-ad%c4%b1m%c4%b1zla-ayn%c4%b1-bir-repo-olu%c5%9fturuyoruz)
    - [5- `npm run deploy`](#5--npm-run-deploy)
  - [**Not: Yukarıdaki adımları yapmakta zorlananlar için video kaynağı Link.**](#not-yukar%c4%b1daki-ad%c4%b1mlar%c4%b1-yapmakta-zorlananlar-i%c3%a7in-video-kayna%c4%9f%c4%b1-link)
## Gerekli adımlar

React uygulamamızı github pages ortamında yayınlamak için bir takım işlemler gerekiyor.


### 1- `npx create-react-app my-app`

Herzaman ki gibi react uygulamamızı oluşturuyoruz.
`cd my-app` komutu ile dizinin içine giriyoruz.

### 2- `npm install gh-pages --save-dev`

Dizinimize geliştirme bağımlılığı olarak `gh-pages` reposunu ekliyoruz.

### 3- `package.json dosyasını aşağıdaki şekilde düzenliyoruz.`

#### `"name"` satırının üzerine;

    "homepage": "githubkullaniciadi.github.io/uygulama-adi", yazıyoruz.

#### `scripts` bölümünün içine;

    "predeploy": "npm run build",
    "deploy": "gh-pages -d build", satırlarını ekliyoruz.

### 4- `github.com üzerinden uygulama adımızla aynı bir repo oluşturuyoruz.`

Oluşturduğumuz repoyu localimizdeki uygulama klasörü ile eşleştiriyoruz. Ardından `git push -u origin master` komutu ile Github'a yüklüyoruz.

### 5- `npm run deploy`

Bu komutu terminalimize yazdıktan sonra React uygulamamız Github pages ortamında yayınlanmaya başlamıştır.

## **Not: Yukarıdaki adımları yapmakta zorlananlar için video kaynağı [Link](https://www.youtube.com/watch?v=BZidYA3dgXA).**
