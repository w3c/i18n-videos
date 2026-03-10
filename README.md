# W3C Internationalization Videos Repository

This repository stores internationalization-related video metadata and assets, including titles, descriptions, subtitles, and thumbnails.

Some videos can exist in more than one media edition for the same language. For example:

- the original English recording with English and Chinese subtitles
- a separately recorded Chinese narration with Chinese subtitles

To support both cases, the repository is organized around three dimensions:

- `video`: the conceptual work or topic
- `edition`: one published media asset, with its own audio track and URL
- `locale`: translated metadata and subtitles for that edition

## Repository Structure

```
videos/
├── video-slug/
│   ├── thumbnail.jpg
│   └── editions/
│       ├── en-original/
│       │   ├── edition.yaml
│       │   ├── en/
│       │   │   ├── README.md
│       │   │   └── subtitles.srt
│       │   ├── zh-Hans/
│       │   │   ├── README.md
│       │   │   └── subtitles.srt
│       │   └── ja/
│       │       ├── README.md
│       │       └── subtitles.srt
│       └── zh-Hans-rerecord/
│           ├── edition.yaml
│           ├── thumbnail.jpg
│           └── zh-Hans/
│               ├── README.md
│               └── subtitles.srt
```

## Why This Model

Subtitle timing belongs to a specific recording, so subtitles should live under an edition.

Re-recorded audio usually has its own URL, duration, thumbnail, and subtitle timing.

The same locale can appear in more than one edition, such as `zh-Hans` subtitles on `en-original` and `zh-Hans` subtitles on `zh-Hans-rerecord`.

See [docs/repository-structure.md](docs/repository-structure.md) for the full rationale.

## Contributing

See [CONTRIBUTING.md](CONTRIBUTING.md) for contribution guidelines.
