# Augmanity – Static Website

This repository contains a static HTML version of the Augmanity website.

You can run it:
- Locally without any tools (just open `index.html`)
- Locally using DDEV (recommended for a cleaner setup and HTTPS)

There is no backend, no database, and no server-side code.  
It’s just HTML, CSS, and JavaScript.

The `.ddev/` folder is not included on purpose.  
Each person sets it up locally if they want to use DDEV.

---

## Option 1: Run it without DDEV

Because this is a static site, you can:

- Clone the repository, or
- Download the repository as a ZIP and extract it

Then open `index.html` directly in your browser.

Note: Some things may behave differently when opening the files directly without a local server.

---

## Option 2: Run it with DDEV (recommended)

Using DDEV provides a local web server and HTTPS, which avoids most browser issues.

---

## What you need (for DDEV)

Make sure you have:

- Docker
- Docker Compose
- DDEV

DDEV installation guide:  
https://ddev.readthedocs.io/en/stable/#installation

---

## Run the site with DDEV

### 1) Get the project into a DDEV directory

You have two options:

#### Option A: Clone the repository (recommended)

1. Open your terminal inside WSL
2. Go to the directory where you keep your DDEV projects (example):

```bash
cd ~/ddev
````

3. Clone the repository into that directory:

```bash
git clone <REPOSITORY_URL>
```

4. Go into the project folder:

```bash
cd <REPOSITORY_FOLDER>
```

---

#### Option B: Download the ZIP manually

1. Download the repository as a ZIP from GitHub
2. Extract the ZIP into your DDEV projects directory (for example `~/ddev`)
3. Rename the extracted folder if needed
4. Open a terminal and go into the folder:

```bash
cd <REPOSITORY_FOLDER>
```

---

### 2) Configure DDEV

Run:

```bash
ddev config
```

When prompted, use:

* Project type: `php`
* Docroot: `.`
* Project name: `augmanity-clean` (or any name you prefer)

Even though the site is static, `php` is used so DDEV provides a local web server.

---

### 3) Start the project

```bash
ddev start
```

---

### 4) Open the website

```bash
ddev launch
```

Or open it manually in your browser:

```
https://augmanity-clean.ddev.site
```

---

## Stop or remove the project

Stop the project:

```bash
ddev stop
```

Remove the project completely:

```bash
ddev delete
```

---

## Notes

* This is a fully static website
* No backend or database is required
* If you see 404 errors:

  * Make sure `index.html` is in the project root
  * Make sure the DDEV docroot is set to `.`
