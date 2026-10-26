# Reading the Eyes

An open eyes-only emotion reading test. Each item shows a black and white photograph of one person's eye region, asks "Which word best describes what this person is thinking or feeling?", and offers four words, one of them intended. There are 40 items and one practice item. The photographs are new, the words are our own, and everything is released openly so researchers, teachers and clinicians can use, adapt and test it.

## Credit to the original format

The format comes from the Reading the Mind in the Eyes Test, revised version (Baron-Cohen, S., Wheelwright, S., Hill, J., Raste, Y., and Plumb, I., 2001, Journal of Child Psychology and Psychiatry, 42(2), 241 to 251); no photograph, word or item is taken from it.

## How the photographs were made

The photographs are AI generated and show no real person. They were made with GPT Image, through the image generation tool of the OpenAI Codex CLI. Each prompt combines three parts: a photographic specification shared by every item, a description of the person (sex, age, ethnicity, a detail such as hair or glasses), and a description of the expression that covers only what the eye region can show (brows, lids, the skin around the eyes, gaze, intensity). Three takes were generated per item under different light. The takes were reviewed for hard faults (a mouth, text, colour, a render look, an uncanny eye, a gaze that gives the answer away) and for the word a viewer would likely pick, and one take was chosen. Three items were regenerated after review with a different individual of the same description. The full prompt of every chosen take is in `prompts.md`.

## How the words were chosen

The words are our own. There is a closed pool of 40 states: each of the 40 targets is the only target of one item and also appears as a foil in at least one other item, so no word gives the answer away by appearing once. All four words in an item share one valence (13 positive, 15 negative and 12 neutral items). Near-synonyms never appear in the same item. The vocabulary is meant for a ten-year-old, and every word has a one-sentence glossary entry in English and in Spanish. The Spanish is in the informal register (tú), and the adjectives agree in gender with the person in each item, so the Spanish glossary is keyed by the exact form shown.

## Calibration status

The items are candidates until they have been tested. The comparison group is being built on neuropsych.io. The retention rule follows the 2001 study: an item is kept when at least half of the people choose the intended word and no other word is chosen by more than a quarter, after 225 answers per item. Item statistics will be added to this repository as they come in, and the item list may shrink if items fail the rule. Until then, treat a score as a count of intended words, not as a norm-referenced result.

## Licences

- Images (`images/`): CC0 1.0 Universal. See `LICENSE-IMAGES.md`.
- Words, glossaries, the item file and any statistics (`items.json`, `items.csv`, `prompts.md` and later statistics files): CC BY 4.0. Attribute to "Neuropsych, https://neuropsych.io". See `LICENSE-DATA.md`.

## Cite this set

Neuropsych (2026). Reading the Eyes: an open eyes-only emotion reading test. https://github.com/cristiandominguezrl/reading-the-eyes

## Take the test

- English: https://neuropsych.io/tests/reading-the-eyes/
- Spanish: https://neuropsych.io/es/tests/reading-the-eyes/

## Files

| Path | What it holds |
|------|---------------|
| `items.json` | The instrument: version, the question and the glossaries in English and Spanish, the 40 items (id, valence, words in both languages, image paths, person description, expression description) and the practice item. |
| `items.csv` | One row per item: id, valence, the target and three foils in English and in Spanish, and the two image paths. |
| `prompts.md` | The common photographic specification and the full prompt of the chosen take of every item. |
| `images/1200x480/<id>.jpg` | The 41 photographs as served on neuropsych.io: grayscale, 1200 by 480 pixels. |
| `images/full/<id>.png` | The same 41 photographs at full resolution, 1983 by 793 pixels. |
| `LICENSE-IMAGES.md` | CC0 1.0 Universal legal code, covering `images/`. |
| `LICENSE-DATA.md` | CC BY 4.0 legal code, covering the item file, the glossaries and any statistics. |
| `CHANGELOG.md` | Release history. |

Item ids run from `eyes-01` to `eyes-40`, and the practice item is `eyes-practice`.
