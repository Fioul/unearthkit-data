# unearthkit-data

Open data behind [UnearthKit](https://unearthkit.com/), an independent guide to metal detectors, pinpointers and digging gear for the United States. Updated 2026-10-17.

| File | What it holds | Rows |
| --- | --- | --- |
| [detectors.csv](detectors.csv) | Metal detectors and pinpointers, one row per model: technology, frequencies, waterproofing, weight, coils, battery, search modes, target ID, warranty and status | 57 |
| [detector-sources.csv](detector-sources.csv) | The maker and dealer pages those specs come from, with the date each was read | 68 |
| [land-rules.csv](land-rules.csv) | What the official texts say about metal detecting on federal land and in 10 states, one row per rule | 62 |
| [land-rules-sources.csv](land-rules-sources.csv) | The official texts those rules come from, with the date each was read | 30 |

## Detectors and pinpointers

Brands: Bounty Hunter, Fisher, Garrett, Minelab, Nokta, Teknetics. Every row comes from a spec page, product page or manual that the maker publishes, read between 16 October 2026 and 17 October 2026. For a few specs a dealer page or an archived copy of the maker's page fills a gap; `detector-sources.csv` says which. The files hold facts only, in our own words and layout. No maker text, image or logo is copied, and no product price is included.

- A cell is empty when no source we read gives the value. `not_published` names those fields; nothing is estimated.
- When one maker page gives two different values for the same spec, `conflicts` shows both (`field: first | second`) and the main column then holds one of them or stays empty. Nothing is settled.
- `status` is `current` or `discontinued` as the maker shows it. It is empty when we could not confirm it.
- `frequencies_khz` lists fixed frequencies. `frequency_range_khz` is used instead for detectors with a user-set range; `frequency_note` repeats the maker's own wording, such as which frequencies apply in which mode.
- `waterproof_part` says which part is rated, for example the whole detector or the coil. `weight_lb` is the figure we use; `weight_text` is how the maker writes it.
- `coils` lists the search coils with the maker's own names: size, coil type, shape, and model code in brackets.

## Land rules

Each rule is a plain-words summary of one official text: the Code of Federal Regulations on ecfr.gov, or a state code or agency page, read between 16 October 2026 and 17 October 2026. `citation` gives the section; `kind` tells what sort of rule it is, such as prohibited, allowed with limits, or removal prohibited. Some texts were read on the copy kept by Cornell's Legal Information Institute because the official site could not be read; `land-rules-sources.csv` marks them.

**This is not legal advice.** Rules change, land managers can add their own, and a text read on one date may no longer apply. Check local rules before you dig.

Not covered: Michigan and Oklahoma (no official text could be read), Florida only in part (some official pages could not be read), and every state not listed in the file. A missing state does not mean detecting is allowed there.

## License and credit

To the extent Julien Fourel holds rights in the compilation and the wording, they are licensed under [CC BY 4.0](LICENSE): free to quote, chart and republish, including commercially. Please credit “UnearthKit” with a link to https://unearthkit.com/. Specs and legal texts as such belong to no one; we claim no rights in them. Brand and model names belong to their owners and are used only to say which products they are. UnearthKit is independent and is not affiliated with any brand named in these files. It earns commissions on some links to retailers; they play no part in these files.

How UnearthKit builds its pages: https://unearthkit.com/method/#open-data
Corrections: https://unearthkit.com/method/#corrections
