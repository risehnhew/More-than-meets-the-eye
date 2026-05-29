# More Than Meets the Eye

This repository hosts the image data accompanying the paper **More Than Meets the Eye**.

## Dataset

The current release contains the `Original/` image set:

| Split | Categories | Images per category | Total images | Format |
| --- | ---: | ---: | ---: | --- |
| `Original/` | 100 | 5 | 500 | PNG |

Each subdirectory under `Original/` corresponds to one idiomatic expression or phrase. Each directory contains five PNG images named with numeric image IDs.

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
```

The uploaded dataset is approximately 374 MiB. Individual image files are below 6 MiB.

## Repository Structure

```text
.
+-- Original/        # 100 phrase-level folders, 500 PNG images total
`-- README.md
```

Folder names are used as category labels. Some labels use `_s` in place of an apostrophe, for example `cat_s eyes`, `dog_s dinner`, and `devil_s advocate`.

## Using the Images

Clone the repository:

```bash
git clone https://github.com/risehnhew/More-than-meets-the-eye.git
cd More-than-meets-the-eye
```

Enumerate the images in Python:

```python
from pathlib import Path

root = Path("Original")
items = [
    {"label": path.parent.name, "path": path}
    for path in root.glob("*/*.png")
]

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

If you use this repository or the dataset, please cite the corresponding paper. Citation details will be added once the paper information is available.

## License

License information will be added when the dataset release metadata is finalized.
