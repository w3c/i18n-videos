# Contributing to W3C Internationalization Videos

## Adding a New Video

1. **Choose or create a video folder** under `videos/`
   - Use kebab-case for video slugs (e.g., `html-forms`, `css-layout`)

2. **Create an `editions/` folder** inside the video folder. Each edition represents one concrete recording or upload.

3. **Create one edition folder** for each media edition.

4. **Create locale folders** inside the edition folder using BCP 47 language tags (e.g., `en`, `fr`, `ar`).

5. **Add required files** in each locale folder:
   - `README.md`: localized title and description for that edition
   - `subtitles.srt`: subtitle file for that edition and locale
