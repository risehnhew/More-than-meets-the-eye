# More Than Meets the Eye

This repository hosts the DIVA image dataset accompanying the ACL 2026 paper **More Than Meets the Eye: Measuring the Semiotic Gap in Vision-Language Models via Semantic Anchorage**.

## Paper

- **Title:** More Than Meets the Eye: Measuring the Semiotic Gap in Vision-Language Models via Semantic Anchorage
- **Author:** Wei He
- **Venue:** ACL 2026 Main Conference
- **arXiv:** [2604.17354](https://arxiv.org/abs/2604.17354)
- **DOI:** [10.48550/arXiv.2604.17354](https://doi.org/10.48550/arXiv.2604.17354)

## Dataset

The current release contains two image sets:

| Split | Description | Categories | Images per category | Total images | Format | Size |
| --- | --- | ---: | ---: | ---: | --- | ---: |
| `Original/` | Original image set | 100 | 5 | 500 | PNG | 374.37 MiB |
| `xeval/` | Extended evaluation image set | 100 | 5 | 500 | PNG | 105.40 MiB |
| **Total** |  | 100 | 10 | 1,000 | PNG | 479.77 MiB |

Each subdirectory under `Original/` and `xeval/` corresponds to one idiomatic expression or phrase. The two image sets use the same 100 category labels.

Example:

```text
Original/
  acid test/
    02817176209.png
    03133054749.png
    ...
  act of god/
    13874381277.png
    73444821016.png
    ...
xeval/
  acid test/
    12066404241_new.png
    34849537511_new.png
    ...
```

The `Original/` images use numeric PNG filenames. The `xeval/` images use numeric filenames with the `_new.png` suffix.

## Repository Structure

```text
.
+-- Original/        # 100 phrase-level folders, 500 PNG images total
+-- xeval/           # 100 phrase-level folders, 500 PNG images total
`-- README.md
```

Folder names are used as category labels. Some labels use `_s` in place of an apostrophe, for example `cat_s eyes`, `dog_s dinner`, and `devil_s advocate`.

## Using the Images

Clone the repository:

```bash
git clone https://github.com/risehnhew/More-than-meets-the-eye.git
cd More-than-meets-the-eye
```

Enumerate all images in Python:

```python
from pathlib import Path

items = []
for split in ["Original", "xeval"]:
    root = Path(split)
    for path in root.glob("*/*.png"):
        items.append({
            "split": split,
            "label": path.parent.name,
            "path": path,
        })

print(len(items))
print(items[0])
```

## Categories

<details>
<summary>Show all 100 categories</summary>

- acid test
- act of god
- agony aunt
- ancient history
- apples and oranges
- armchair critic
- baby blues
- bad apple
- banana republic
- beached whale
- bear market
- best man
- big cheese
- big fish
- big wig
- black box
- black sheep
- brain surgery
- brass ring
- bread and butter
- bull market
- bun in the oven
- busy bee
- cat_s eyes
- chicken feed
- chocolate teapot
- close shave
- cold feet
- cold turkey
- copy cat
- couch potato
- devil_s advocate
- dirty money
- dirty word
- dog_s dinner
- donkey work
- eager beaver
- elbow grease
- eye candy
- fancy dress
- field work
- flea market
- flower child
- flying saucer
- ghost town
- grass roots
- graveyard shift
- gravy train
- green fingers
- green light
- guinea pig
- hair of the dog
- heart of gold
- heart of stone
- hen party
- high life
- honey trap
- hot air
- hot potato
- inner circle
- ivory tower
- loan shark
- lounge lizard
- love triangle
- low-hanging fruit
- marching orders
- monkey business
- nest egg
- night owl
- old flame
- open book
- pain in the neck
- panda car
- party animal
- peas in a pod
- piece of cake
- pig_s ear
- pins and needles
- pipe dream
- private eye
- rat race
- rat run
- red flag
- rocket science
- secret santa
- shrinking violet
- silver bullet
- smoking gun
- snail mail
- snake in the grass
- sour grapes
- spring chicken
- thin ice
- top dog
- two-way street
- watering hole
- wet blanket
- white elephant
- white hat
- zebra crossing

</details>

## Citation

If you use this repository or the dataset, please cite the corresponding paper:

```bibtex
@misc{he2026morethanmeets,
  title = {More Than Meets the Eye: Measuring the Semiotic Gap in Vision-Language Models via Semantic Anchorage},
  author = {He, Wei},
  year = {2026},
  eprint = {2604.17354},
  archivePrefix = {arXiv},
  primaryClass = {cs.CL},
  doi = {10.48550/arXiv.2604.17354},
  url = {https://arxiv.org/abs/2604.17354},
  note = {Accepted to the Main Conference of ACL 2026}
}
```

## License

License information will be added when the dataset release metadata is finalized.
