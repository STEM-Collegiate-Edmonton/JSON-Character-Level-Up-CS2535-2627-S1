# JSON Character Level Up

## Basic Premise

Create a Python program that reads a Dungeons & Dragons character from `level_1_character.json`, applies a set of predetermined level-up changes, and writes the updated character to a new file named `level_2_character.json`.

The goal is to demonstrate that you can load structured JSON data, access nested objects and lists, modify values, and save the changed data without altering the original file.

## Basic File Structure

Your starter folder will contain:

```text
basic/
├── main.py
└── level_1_character.json
```

After running your program, it should contain:

```text
basic/
├── main.py
├── level_1_character.json
└── level_2_character.json
```

## Basic Requirements

* [ ] Import the `json` module and use `json.load()` to read `level_1_character.json`.
* [ ] Increase the character's `level` by **1** and `armor_class` by **1**.
* [ ] Access the nested `attributes` object and increase `strength` by **2** and `constitution` by **1**.
* [ ] Add `"Survival"` to the character's `skills` list.
* [ ] Add `"Silver Dagger"` to the character's `weapons` list.
* [ ] Leave all other character information unchanged.
* [ ] Write the modified character to a new file named `level_2_character.json` using `json.dump()`.
* [ ] Use `indent=4` when writing the new JSON file.

> Fully completing the Basic Requirements earns **16/20 marks, or 80%**.

## Basic Assessment — 16 Marks

| Assessment Item | Criteria | Marks |
|---|---|---:|
| Reading JSON Data | Correctly opens and loads `level_1_character.json` using the `json` module. | 2 |
| Character Progression | Correctly increases the character's level and armor class by 1. | 2 |
| Nested Attribute Processing | Correctly accesses the nested attributes and updates strength and constitution by the required amounts. | 3 |
| Processing Lists | Correctly adds the required skill and weapon to their existing lists. | 3 |
| Preserving Existing Data | Keeps all information that was not meant to change intact. | 2 |
| Writing JSON Data | Creates `level_2_character.json` without overwriting the original file. | 3 |
| JSON Formatting | Uses `indent=4` to create a readable JSON file. | 1 |
|  | **Total** | **16** |

## Advanced Premise

Extend your Basic program so that it can level up a character from **any existing level** rather than only from level 1 to level 2.

You should be able to begin this task by copying your Basic `main.py` into the Advanced folder and modifying it.

Instead of using predetermined upgrades, the program will ask the user how the character should be improved. It must also validate the user's input and handle errors so that incorrect input does not cause the program to crash.

## Advanced File Structure

Your starter folder will contain:

```text
advanced/
├── main.py
└── level_1_character.json
```

The program should create new character files as the character levels up. For example:

```text
advanced/
├── main.py
├── level_1_character.json
├── level_2_character.json
├── level_3_character.json
└── level_4_character.json
```

## Advanced Requirements

* [ ] Ask the user which character level they want to level up from and use that value to determine which `level_n_character.json` file should be loaded.
* [ ] Increase the character's `level` and `armor_class` by **1**.
* [ ] Ask the user which of the six attributes they want to increase and increase the selected attribute by **1**.
* [ ] Ask the user for a new skill and add it to the character's `skills` list.
* [ ] Ask whether a new weapon should be added. If the user chooses yes, ask for the weapon and add it to the `weapons` list.
* [ ] Write the updated character to `level_n_character.json`, where `n` is the character's **new level**.
* [ ] Validate user input so invalid attribute names, level values, and yes/no responses are not accepted.
* [ ] Use error handling so problems such as entering the wrong datatype or requesting a character file that does not exist do not cause the program to crash.

## Advanced Assessment — 4 Marks

| Assessment Item | Criteria | Marks |
|---|---|---:|
| Dynamic Level-Up | Uses user input to load the appropriate character file and automatically creates the correctly named file for the next level. | 1 |
| Custom Character Upgrades | Allows the user to select an attribute, add a skill, and optionally add a weapon while correctly updating the JSON data. | 1 |
| Input Validation | Prevents invalid level, attribute, and yes/no values from being accepted. | 1 |
| Error Handling | Handles incorrect datatypes, missing character files, and other expected input errors without crashing. | 1 |
|  | **Total** | **4** |