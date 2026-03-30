# Content Guide

This guide explains how to update the NZAIO website content.

## 1. Get the project

If you do not have the project yet:

```bash
git clone https://github.com/NZAIO/nzaiolympiad.github.io.git
cd nzaiolympiad.github.io
npm install
```

If you already have the project:

```bash
cd nzaiolympiad.github.io
git pull origin main
```

## 2. Main files to edit

- Homepage: `src/content/homepage/-index.md`
- About: `src/content/about/-index.md`
- Contact: `src/content/contact/-index.md`
- Support Us: `src/content/pages/support-us.md`
- Editions overview: `src/content/blog/-index.md`
- Edition pages: `src/content/blog/`

Example edition page:

- `src/content/blog/2026-edition.md`

## 3. Add images

Put images in these folders:

- Edition or event images: `public/images/editions/`
- Logo or brand images: `public/images/nzaio/`

Use clear file names so others can understand what each image is for.

## 4. How to refer to images in Markdown

Use normal Markdown image syntax:

```md
![Students at camp](/images/editions/2026-camp-work.jpeg)
```

You can see real examples in:

- `src/content/blog/2026-edition.md`

## 5. How to add a new edition

1. Create a new Markdown file inside `src/content/blog/`
2. Copy the structure of `src/content/blog/2026-edition.md`
3. Update the title, date, description, cover image, and page content
4. Add any new images to `public/images/editions/`

## 6. Preview locally

Run:

```bash
npm run dev
```

Then open the local address shown in the terminal.

## 7. Publish changes

When your edits are ready:

```bash
git add .
git commit -m "Update website content"
git push origin main
```

After pushing to `main`, GitHub Actions will automatically rebuild and publish the website.

## 8. Notes

- Most updates only require editing Markdown files and adding images.
- Be careful when editing files in `src/config/`, `.github/`, or Astro layout files, as those affect site structure and deployment.
