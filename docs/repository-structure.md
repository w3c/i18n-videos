# Repository Structure

Use three levels:

1. `video`: the conceptual work
2. `edition`: one concrete published recording or upload
3. `locale`: one language's metadata and subtitle track for that edition

```text
videos/<slug>/editions/<edition-id>/<locale>/
```

## Directory Layout

```text
videos/
└── introduction/
    ├── thumbnail.jpg
    └── editions/
        ├── en-original/
        │   ├── edition.yaml
        │   ├── en/
        │   │   ├── README.md
        │   │   └── subtitles.srt
        │   ├── zh-Hans/
        │   │   ├── README.md
        │   │   └── subtitles.srt
        │   └── ja/
        │       ├── README.md
        │       └── subtitles.srt
        └── zh-Hans-rerecord/
            ├── edition.yaml
            ├── thumbnail.jpg
            └── zh-Hans/
                ├── README.md
                └── subtitles.srt
```

### `edition.yaml`

Metadata for one published media asset:

```yaml
id: en-original
kind: original
audioLanguage: en
```

For a re-recorded Chinese version:

```yaml
id: zh-Hans-rerecord
kind: rerecord
audioLanguage: zh-Hans
basedOn: en-original
```

### `<locale>/README.md`

Localized title and description for that edition.

### `<locale>/subtitles.srt`

Subtitle track for that edition in that locale.

## Naming Guidance

Use edition IDs that encode audio language and edition type:

- `en-original`
- `zh-Hans-rerecord`
