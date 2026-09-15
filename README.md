# Signal Management in Pharmacovigilance — toolkit and companion tool

Companion materials to **_Signal Management in Pharmacovigilance: From Detection and Validation to
Benefit–Risk Decisions and Regulatory Action_** by Dr. Hafez Selim, MD, PhD (Selim Medical Press, 2026).

**https://abdu94-hash.github.io/signal-management-tool/**

## What is here

| Path | What it is |
|---|---|
| `index.html` | Landing page — the index Appendix D of the book points to |
| `tool/index.html` | **Signal Management Decision Support** — the companion tool, one self-contained page |
| `toolkit/` | The 24 editable files: 20 Word documents, 4 spreadsheets, plus a zip of the set |
| `CHANGELOG.md` | Corrections made after publication, with dates |

## The companion tool

Nine modules following the signal lifecycle, plus a scenario laboratory.

| # | Module | What it gives you |
|---|---|---|
| 1 | Signal validation | Five gates — novelty, clinical coherence, evidence quality, alternative causes, proportionality — and a documented disposition, including non-validation with objective reopening triggers |
| 2 | Prioritization | The five-domain scale scored 1–5 out of 25 with the book's anchors on screen, plus a mandatory clinical-override field |
| 3 | Quantitative screen | PRR and ROR with 95% confidence intervals, expected count, chi-square, and the Information Component with IC₀₂₅ |
| 4 | Observed to expected | Person-time, expected count, O/E and an exact Poisson interval, with background-rate sensitivity |
| 5 | Time to onset | n, mean, median, Tukey-halves quartiles, IQR and range, with a histogram and cumulative curve, and a right-skew flag |
| 6 | Evidence integration | A totality-of-evidence table where you record the weight each source earns **for this question** and why — no fixed hierarchy, no score |
| 7 | Causality structure | The Bradford Hill considerations as a reasoning structure, each with the caution attached to it. Deliberately computes no total |
| 8 | Benefit–risk | Structured effects table plus subgroup decomposition, giving NNT and NNH for the whole population, the remainder, and the susceptible subgroup |
| 9 | Decision record | A traceable record with conclusion, rationale, residual uncertainty, actions, owner, due date and reopening triggers |

The **scenario laboratory** runs three staged cases — a delayed drug-induced liver injury, an oncology
thromboembolism cluster, and an algorithmic ranking that puts a nonspecific alert above a fatal syndrome —
with scoring and an expert debrief. **Copy the full assessment** exports every completed module as plain text.

### What it deliberately does not do

The book argues that some things must not be reduced to a number, and the tool follows it:

- Evidence integration applies **no fixed source-weight hierarchy**. A randomized trial is not automatically
  superior for a rare delayed event, so the tool asks you to justify the weight rather than assigning one.
- The causality module computes **no score**. Assigning points to the Bradford Hill considerations is a misuse —
  they are neither independent nor commensurable, and they carry different weight for different mechanisms.
- Benefit–risk is **not** collapsed into a single margin. The decomposition is there because the actionable
  question is usually whether the risk concentrates in an identifiable subgroup.

Scoring bands, thresholds and response times are illustrative company designs, not regulatory requirements.
The tool says so where they appear.

## Worked examples

Every module carries a "load the book's example" control, reproducing the book exactly:

- Disproportionality — PRR 7.20 (4.57–11.35), ROR 7.24 (4.58–11.43), N<sub>exp</sub> 4.16, IC 2.39, IC₀₂₅ 1.71, χ² 98.7
- Observed to expected — 19,165 person-years, 0.958 expected, O/E 12.5 (6.5–21.9)
- Time to onset — n 12, mean 20.0, median 8.5, IQR 4–27
- Prioritization — 21 of 25
- Benefit–risk — NNT 25, NNH 1,250 overall; 4,750 in the remaining population and 83 in the susceptible subgroup

All products, patients and data are **fictional educational composites**.

## Privacy

Everything runs in your browser. No storage, no analytics, no network request of any kind — the tool page
makes exactly one request, for itself. Nothing you type leaves the machine, and closing the tab discards it.
You can save the page and run it offline.

If you use an AI browser assistant supporting the Web Model Context API, the tool page offers it read access
to the summary you have entered; a cloud-backed assistant would take that content off the machine.

## Technical

No build step, no dependencies, no CDN. The tool registers its calculators as
[WebMCP](https://github.com/webmachinelearning/webmcp) tools via `document.modelContext`, so an agentic
browser can call them directly.

To run locally:

```bash
python3 -m http.server 8000
```

## Status

Content last reviewed **September 2026**. Regulatory statements reflect the position at that date, including
the replacement of FAERS by the FDA Adverse Event Monitoring System (AEMS) on 11 March 2026 and the deletion
of the validated-signal notification under Article 21(2) of Commission Implementing Regulation (EU) 520/2012
by Regulation (EU) 2025/1466, in force 12 August 2025. Re-check against current guidance before relying on it.

## Disclaimer

Educational. Does not replace applicable law, current regulatory guidance, medical judgment, or the
procedures of any company or competent authority.

## License

See [LICENSE](LICENSE).
