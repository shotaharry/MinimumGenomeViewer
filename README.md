# JCVI-Syn3A Genome Browser

An interactive genome browser for the minimal synthetic bacterium **JCVI-Syn3A** (CP016816.2, 543,379 bp).

## Features

- **Gene visualization** — CDS, tRNA, rRNA, ncRNA, misc_RNA をカラーコードで表示
- **RNA-seq coverage** — GSE205017 の 4 サンプル（normal / stationary × 2）を重ねて表示
- **GM12 comparison** — JCVI-syn1.0 (GM12) ゲノムとの比較表示（BLASTn/BLASTp 結果を重畳）
- **Gene info panel** — 遺伝子クリックで機能・配列・外部リンク（NCBI / UniProt / AlphaFold）を表示
- **Search** — 遺伝子名・locus tag でジャンプ
- **Circular view** — ゲノム全体を環状に表示
- **Gene groups & markers** — 遺伝子をグループ分けしてマーカー（○△□★）を配置
- **Gene comments** — 各遺伝子にメモを記入
- **Sequence copy** — 指定領域の塩基配列をコピー
- **Random gene picker** — ランダムに遺伝子を選択

## Usage

`syn3A_genome_browser/index.html` をブラウザで直接開く（サーバー不要）。

```
open syn3A_genome_browser/index.html
```

## Data sources

| データ | 由来 |
|---|---|
| ゲノムアノテーション | CP016816.2 (NCBI) |
| RNA-seq | GSE205017 (SRR19432056–59) |
| GM12 比較 | CP001668 / NZ_CP001668.1 |

## Repository structure

```
syn3A_genome_browser/
├── index.html          # メインブラウザ（全コード内包）
├── genes.json          # 遺伝子アノテーション
├── compare/            # GM12 比較データ（BLAST結果・PAF・FASTA）
└── rnaseq/
    ├── coverage.json   # RNA-seq カバレッジ（4サンプル）
    └── genome/         # Syn3A ゲノム配列
```
