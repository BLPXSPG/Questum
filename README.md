# Questum

## 📌 Requirements

To run Questum, ensure you have the following dependencies installed:

- Python >= 3.10
- pandas >= 1.5.3
- faiss-cpu >= 1.7.4
- transformers >= 4.38.2

---

## 📂 Dataset

The bilingual dataset is stored in the following directories:
- `./chinese` – Contains the **Chinese dataset**.
- `./english` – Contains the **English dataset**.

For detailed information about the datasets, please refer to the respective `README.md` files available in both **Chinese** and **English**.

---

## 🎮 Gameplay & Evaluation

### ▶ Running the Method on the Chinese Dataset
To run Questum on the **Chinese dataset**, execute the following command:

```bash
python main.py --script_name "孤舟萤（6人）" --output_root_path "./log_cn"
```

Here, `script_name` is the name of the script you want to run.

### ▶ Running the Method on the English Dataset
To run Questum on the **English dataset**, execute:

```bash
python main.py --script_name "Solitary Boat Firefly (6 people)" --output_root_path "./log_en" --is_english 1
```

### ▶ Model Selection
By default, the method uses the **GPT-3.5 16k** model. However, Questum also supports:
- LLaMA2 (7B, 13B, 70B)
- Gemma7B

To use a different model, include the `--model_type` parameter and specify the model path in the `main.py` file.

---

## 📜 Gameplay & Evaluation Logs

Game and evaluation logs are stored in the following directories:
- `./log_cn` – Logs for **Chinese dataset** runs.
- `./log_en` – Logs for **English dataset** runs.

### 📊 Log File Structure
Each game execution generates log files with the following structure:

- `*.xlsx` – Contains **dialogue history** and generated responses.
- `evaluation.xlsx` – Stores **evaluation results** for the generated responses.

---

## 🎭 Murder Mystery Game Rules & Procedure

Questum is a structured **role-playing deduction game** that combines:
- **Logical reasoning** 🔍
- **Deception and strategy** 🎭
- **Immersive storytelling** 📖

### 🏛️ Detailed Rules

### 🔹 Rule 1: Player Roles
The total number of players depends on the script. There may be **one or more murderers**, while the rest are **civilians**.

### 🔹 Rule 2: Civilian Objectives
Civilians must collaborate to **solve the murder case**, collecting evidence and reasoning to identify the murderer while avoiding false accusations.

### 🔹 Rule 3: Lying Restrictions
Only **murderers** are allowed to **lie**. Civilians must provide **honest** answers and disclose all known information to uncover the truth.

### 🔹 Rule 4: Character Scripts
At the start of the game, each player receives a **character script** detailing their role and background.

### 🔹 Rule 5: Information Gathering
Players cannot see each other’s character scripts and must collect information **through interactions**.

### 🔹 Rule 6: Voting Mechanism
During the **voting phase**, players vote on who they suspect is the murderer:
- If a murderer receives **more than 50% of votes**, the civilians win.
- Otherwise, the murderer wins.

---

## ⏳ Game Procedure

### 🃏 **Stage 1: Character Script Distribution**
The host distributes **character scripts** containing:
- Character name
- Role (Murderer or Civilian)
- Background story

### 🗣 **Stage 2: Self-Introduction**
Players introduce their characters to establish the scenario.

### 🕵️ **Stage 3: Open Questioning Rounds**
Three **interrogation rounds** allow players to gather and analyze clues.

### ⚖️ **Stage 4: Voting**
Players cast **anonymous votes** to identify the suspected murderer.

### 🎭 **Stage 5: Outcome Reveal**
The final result is revealed, determining whether the civilians successfully identified the murderer.

---

## 🔥 Example Scenario: *Solitary Boat Firefly*

The *Solitary Boat Firefly* scenario consists of **six players** and **four victims**.

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

Each player is modeled as an agent:
\[ \mathcal{A} = \{a_i\}_{i=1}^{6} \]

Each victim is modeled as:
\[ \mathcal{V} = \{v_k\}_{k=1}^{4} \]

---

## 🔎 Character Example: *Ethan Carter* (Murderer)

### 📖 **Character Background (C₁)**
_"Coming from the Carter family, you are often called 'Ethan'. Born in 1886, your life has been filled with extraordinary episodes..."_

### 🧐 **Suspicion State (\(s_{ijk}\))**
Each victim maintains a **suspicion matrix** indicating whom they suspect.

Example: If victim *Benjamin Harper* has a suspicion row `[1,0,0,1,0]`, it means they suspect:
- Olivia Bennett
- Sophia Wallace

Thus, Benjamin Harper’s suspect list is: `[Olivia Bennett, Sophia Wallace]`

### 🎯 **Individual Objectives (\(o_i\))**
Ethan Carter's hidden objectives include:
1. 🕵️ Conceal that he **killed William Brooks**
2. 🕵️ Conceal that he **killed Samuel Foster**
3. 🔍 Uncover the **truth about an unsolved past event**
4. 🤐 Hide his **relationship with Henry Dawson**
5. ... (additional hidden objectives)

---

✨ *Get ready to step into a world of mystery and intrigue!* ✨

