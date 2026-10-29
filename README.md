# A.I. Matrix: Authentic vs. Synthetic Image Generation

Does training an AI image generator on synthetic images produce better results than training it on real ones? This project compared two Stable Diffusion models, one trained on each, and tested the difference statistically.

**Authors:** Jayden Paige and Ricky Moore | STEM Capstone, completed May 2025

## Key Results

| Model trained on | Mean score (1-5) | Std. dev. |
|---|---|---|
| Authentic images | 2.72 | 1.05 |
| Synthetic images | 3.12 | 1.05 |

A paired t-test gave **p = 0.0114**, so the difference was statistically significant.

## Method

1. Built two datasets of 200 face images each: one [synthetic](https://huggingface.co/datasets/TLeonidas/this-person-does-not-exist) and one [authentic](https://huggingface.co/datasets/HK83/real_people_3000).
2. Trained a Stable Diffusion model on each in Google Colab.
3. Generated 75 images per model from the prompt "Image of a girl with blonde hair."
4. Scored every image from 1 (horrible) to 5 (excellent) on a Likert scale based on how well it matched the prompt.
5. Compared the two sets of scores with a paired t-test.

## Limitations

- Small sample (75 images per model) and a single prompt
- Scoring was subjective, based on a Likert scale rather than an automated metric
- Small training sets (200 images each)

## Contents

- [`report/`](report/): full written report with literature review
- [`presentation/`](Public Copy - AI Matrix_ Report - Google Docs.pdf): capstone slides
- [`results/`](results/): score data and charts

## Tools

Python, Google Colab, Stable Diffusion, Hugging Face, paired t-test analysis
