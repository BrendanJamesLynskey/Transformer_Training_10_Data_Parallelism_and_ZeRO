# Transformer Training 10 — Data Parallelism, All-Reduce and ZeRO

Give every device the whole model and its own share of the batch, then make the copies agree. The ring all-reduce stepped through, the α–β link model, all-gather and why its bytes grow, payload against wire bytes, ZeRO and FSDP, overlap and MFU.

**Live site:** https://brendanjameslynskey.github.io/Transformer_Training_10_Data_Parallelism_and_ZeRO/

Data parallelism; the ring all-reduce (stepped live); the α–β model and collective times; all-gather and why its bytes grow; payload vs wire bytes; ZeRO 1–3 and FSDP; step time, overlap and MFU.

## Live, animated companion

This deck is the slide companion to Part 2 (Training) of [Transformer Decoder Explained](https://transformer-decoder-explained.vercel.app/training), where the same model trains in your browser:

- [Chapter 11: Parallelism I: data](https://transformer-decoder-explained.vercel.app/training/11-data-parallelism)

## Where the numbers come from

Every measured number on these slides comes from the site's [results.md](https://github.com/BrendanJamesLynskey/transformer-explainer/blob/main/results.md) (seeded NumPy reference runs; CI recomputes them), filled in at build time from its `results.json`. Numbers from papers are cited on the slide with a link. The model is tiny (5,376 parameters, one book, a CPU): its runs show mechanisms, not what happens at scale, and the slides say so where it matters. GPU runs of the site's Colab notebooks are pending; no GPU number appears here.

Part of the [Transformer Training sub-hub](https://github.com/BrendanJamesLynskey/LLM_Hub_Transformer_Training) &middot; [LLMs hub](https://github.com/BrendanJamesLynskey/LLMs)
