## Domino assembly

### 4 Registers (2 bits)
🁤 🁥 🁦 🁧, (32 bit)
### 8 Operations (3 bits)
🁣 🁪 🁱 🁸 🁿 🂆 🂍 🁢



| **Instructions**                    ||||**Description**| 
| - | - |- |- |-|
| `🁣` _(op, 3 bits)_| `R1` _(reg, 2 bits)_.|`R2` _(reg, 2 bits)_.|`I` _(imm, 9 bits)_.|`R1` = `R2` + `I`|
| `🁪` _(op, 3 bits)_| `R1` _(reg, 2 bits)_.|`R2` _(reg, 2 bits)_.|`R3` _(reg, 2 bits)_.|`R1` = `R2` + `R3`|
| `🁱` _(op, 3 bits)_|`I` _(imm, 13 bits)_.|||JUMP `I` lines|
| `🁸` _(op, 3 bits)_| `R1` _(reg, 2 bits)_.|`R2` _(reg, 2 bits)_.|`I` _(imm, 9 bits)_.|JUMP `I` lines if `R1` == `R2`|
| `🁿` _(op, 3 bits)_| `R1` _(reg, 2 bits)_.|`I` _(imm, 11 bits)_.||`R1` = `I`|
| `🂆` _(op, 3 bits)_||||Input int to `🁤`|
| `🂍` _(op, 3 bits)_||||Output int from `🁤`|
| `🁢` _(op, 3 bits)_||||Exit programm|


### Immediates
###### Syntax 
Flip the dominos to the side, the left side represents 1s and the right side 0s
If the imm is shorter than the max bit size for the instruction, 0s or 1s depending on postive or negative will be filled between bit 1 and the rest of the bits
###### Examples
🀸 = -1,
🀲🀸 = 1,
🀲🀹 = 2,
🀾🀵🀹 = -3,
🀲🁆 = 7,
🀲 = 0,🀾🀳🀹🀹 = -11, As you can see, it is very intuitive and will probably soon replace numbers in all languages

### Comments
Although it is not recommended to add comments due to the self-explainable nature of the language, It is possible to add comments by simply writing anything after each instruction as anything after the dominos will be ignored


### How to use
```zsh
./domino <filepath>
```
##### Note: Only files ending with .domino can be used

#### Run the faculty example included in this repo
```zsh
./domino faculty.domino
```
