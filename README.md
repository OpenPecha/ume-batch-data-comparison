# Ume Batch 5 — ITv2 vs ITv3 comparison data

This folder holds the data used to compare **ITv2** and **ITv3** on the same work: **Ume Batch 5**, covering **385 tasks**.

Use these files when you want to see how the two interface versions differ in quality (how much the transcripts change across annotators and reviewers) and in time (how long each role spent on a task).

## What’s in here

> **Viewing these files on GitHub:** the two `*_FR.csv` files are several MB, and GitHub will not preview files that large in the browser (“Sorry about that, but we can’t show files that are this big right now”). The files are complete and uploaded correctly. To read them, click **Download raw file** on the file page, or clone the repo and open them locally. The two `*_time.csv` files are small enough to preview normally.
>
> Transcripts include Tibetan text. When you open a CSV in Excel or Google Sheets, import it as **UTF-8** so the text displays correctly.

| File | Version | What it contains |
| --- | --- | --- |
| `Ume_batch_5_v2_FR.csv` | ITv2 | Full review (FR) export: transcripts, character-diff metrics, rejections, and related review fields |
| `Ume_batch_5_v3_FR.csv` | ITv3 | Same kind of FR export for ITv3 |
| `v2_time.csv` | ITv2 | Time spent per task, in seconds, by role |
| `v3_time.csv` | ITv3 | Time spent per task, in seconds, by role |

Each time file has **385 rows** (one per task), plus a header row.

## How the two versions differ in the data

The workflows are not identical, so the columns are not identical either:

- **ITv2:** two annotators, two reviewers, and a final reviewer. Time columns: `annotator_1_seconds`, `annotator_2_seconds`, `reviewer_1_seconds`, `reviewer_2_seconds`, `final_reviewer_seconds`.
- **ITv3:** three annotators and one reviewer. Time columns: `annotator_1_seconds`, `annotator_2_seconds`, `annotator_3_seconds`, `reviewer_seconds`.

Tasks are identified by `file_number`. Join a version’s FR file to its time file on that field when you need both quality and timing for the same task.

## Source

- Batch: **ume_batch_5** (ITv3 exports use the batch name `ume_batch_5_v3`)
- Image / page files come from the OCR-Benchmark Ume Batch 5 set
- Exports are the full-review CSVs plus the per-task timing CSVs for each interface version
