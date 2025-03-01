# Questum

## Requirements

* Python >= 3.10
* pandas >= 1.5.3
* faiss-cpu >= 1.7.4
* transformers >= 4.38.2

## Dataset
The bilingual dataset is housed within the `./chinese` and `./english` folders. For detailed information, please refer to the `README.me files` located in these folders, available in both **Chinese** and **English** versions, respectively.


## Gameplay and Evaluation
To run our method on the Chinese dataset, please use the following:
```
Python main.py --script_name "孤舟萤（6人）" --output_root_path "./log_cn"
```

Here, `script_name` is the name of the script you want to run.

To run our method on the English dataset, please use the following:
```
Python main.py --script_name "Solitary Boat Firefly (6 people)" --output_root_path "./log_en" --is_english 1
```


The default model is the `GPT-3.5 16k` version. However, we also offer code support for using models such as LLaMA2 (7B, 13B, 70B) and Gemma7B. Please include the `--model_type` parameter and add the path to your model in the main.py file.


## Gameplay and Evaluation log
The log files are stored in the `./log_cn` and `./log_en` folders. The log files contain the following information:
* `*.xlsx`: The log file contains the dialogue history and the generated responses.
* `evaluation.xlsx`: The log file contains the evaluation results of the generated responses.




# 🎭 Murder Mystery Game Rules & Procedure

## 🏛️ Detailed Rules

### 🔹 Rule 1:
The total number of players depends on the script. There may be one or more murderers, while the rest are civilians.

### 🔹 Rule 2:
Civilian players must collaborate to solve a meticulously planned murder case, collecting evidence and reasoning to identify the real murderer while ensuring they are not mistaken as one. Murderers must concoct lies to hide their identity and achieve their secret objectives.

### 🔹 Rule 3:
Only **murderer players** can lie. They may frame others to deflect suspicion. **Civilians** must answer honestly and provide all known information to uncover the truth.

### 🔹 Rule 4:
At the start of the game, each player receives a **character script** detailing their role and identity.

### 🔹 Rule 5:
Players cannot see each other's character scripts. They must collect information solely through **interactions**.

### 🔹 Rule 6:
During the **voting phase**, players vote for who they think is the murderer. If a murderer gets **more than 50% of votes**, the civilians win. Otherwise, the murderer wins.

---

## ⏳ Game Procedure

### 🃏 **Stage 1: Distribution of Character Scripts**
The host distributes character scripts, which include:
- Name
- Role (Murderer or Civilian)
- A brief character backstory

### 🗣 **Stage 2: Self-Introduction Session**
Players introduce their characters, setting the stage for interactions.

### 🕵️ **Stage 3: Open Questioning Rounds**
Three rounds of questioning allow players to interrogate and gather clues.

### ⚖️ **Stage 4: Voting**
Players cast **anonymous votes** to determine the suspected murderer.

### 🎭 **Stage 5: Outcome Reveal**
The final results are revealed, determining if the civilians correctly identified the murderer.

---

## 🔥 Example: *Solitary Boat Firefly* Script

The *Solitary Boat Firefly* scenario features **six players** and **four victims**:

### 🎭 **Players:**
- Ethan Carter
- Olivia Bennett
- Lucas Hayes
- Nathan Sullivan
- Sophia Wallace
- Henry Dawson

### ⚰ **Victims:**
- William Brooks
- Samuel Foster
- Benjamin Harper
- Charles Reynolds

Each player is modeled as an agent **\( \mathcal{A} = \{a_i\}_{i=1}^{6} \)**  
Each victim is modeled as **\( \mathcal{V} = \{v_k\}_{k=1}^{4} \)**  

---

## 🔎 Character Example: *Ethan Carter* (Murderer)

### 📖 **Character Background (C₁)**
*"Coming from the Carter family, you are often called 'Ethan'. Born in 1886, your life has been filled with extraordinary episodes..."*

### 🧐 **Suspicion State (\(s_ijk\))**
Each victim has a **suspicion matrix** indicating whom they suspect among the five other players.

**Example:**  
If victim *Benjamin Harper* has a row `[1,0,0,1,0]`, it means they suspect:
- Olivia Bennett
- Sophia Wallace  

**Thus, Benjamin Harper's suspect list is:** `[Olivia Bennett, Sophia Wallace]`

### 🎯 **Individual Objectives (\(o_i\))**
Ethan Carter's goals include:
1. 🕵️ Concealing that he **killed William Brooks**
2. 🕵️ Concealing that he **killed Samuel Foster**
3. 🔍 Discovering the **truth about an unsolved past event**
4. 🤐 Hiding his **relationship with Henry Dawson**
5. ... (additional hidden objectives)

---

## 🎮 Summary

This structured role-playing game blends **deduction, deception, and storytelling**, challenging players to think critically, interrogate effectively, and immerse themselves in character-driven narratives.

---
✨ *Get ready to step into a world of mystery and intrigue!* ✨
