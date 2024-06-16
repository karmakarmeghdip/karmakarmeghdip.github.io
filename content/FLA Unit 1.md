---
~
---
### Introduction to Alphabet, Languages, and Grammars

#### Alphabet
- **Definition**: An alphabet is a finite set of symbols or characters.
- **Notation**: Commonly denoted by Σ (Sigma).
- **Example**: Σ = {a, b, c}.

#### Languages
- **Definition**: A language is a set of strings formed from an alphabet.
- **Types**: Natural languages (e.g., English), formal languages (e.g., programming languages).
- **Example**: For Σ = {a, b}, a language could be L = {aa, ab, ba}.

### Grammars
- **Definition**: A grammar is a set of rules that describe how strings in a language can be formed.
- **Components**:
  - **N**: Set of non-terminal symbols.
  - **Σ**: Set of terminal symbols (alphabet).
  - **P**: Set of production rules.
  - **S**: Start symbol (usually a member of N).

### Productions and Derivation
- **Productions**: Rules that define how non-terminal symbols can be replaced with terminal symbols or other non-terminal symbols.
  - **Notation**: A → α, where A is a non-terminal and α is a string of terminals and/or non-terminals.
- **Derivation**:
  - **Process**: Starting from the start symbol, repeatedly replace non-terminals using production rules to generate a string in the language.
  - **Types**: Leftmost derivation, rightmost derivation.
  - **Example**: Given grammar G with productions S → AB, A → a, B → b:
    - Derivation: S ⇒ AB ⇒ aB ⇒ ab.

### Chomsky Hierarchy of Languages
The Chomsky hierarchy categorizes formal languages based on their generative grammars.

#### Types of Grammars and Corresponding Languages
1. **Type 0: Recursively Enumerable Languages**
   - **Grammar**: Unrestricted grammar.
   - **Production**: α → β, where α and β are strings of terminals and non-terminals.
   - **Machine**: Turing machine.
   - **Example**: Any language that can be recognized by a Turing machine.

2. **Type 1: Context-Sensitive Languages**
   - **Grammar**: Context-sensitive grammar.
   - **Production**: αAβ → αγβ, where A is a non-terminal and α, β, γ are strings of terminals and non-terminals with γ not being empty.
   - **Machine**: Linear bounded automaton.
   - **Example**: L = {a^n b^n c^n | n ≥ 1}.

3. **Type 2: Context-Free Languages**
   - **Grammar**: Context-free grammar.
   - **Production**: A → γ, where A is a non-terminal and γ is a string of terminals and/or non-terminals.
   - **Machine**: Pushdown automaton.
   - **Example**: L = {a^n b^n | n ≥ 0}.

4. **Type 3: Regular Languages**
   - **Grammar**: Regular grammar.
   - **Production**: A → aB or A → a, where A and B are non-terminals and a is a terminal.
   - **Machine**: Finite automaton.
   - **Example**: L = {a^n | n ≥ 0}.

### Summary
- **Alphabet**: Set of symbols.
- **Language**: Set of strings from an alphabet.
- **Grammar**: Set of production rules.
- **Derivation**: Process of generating strings from the start symbol using production rules.
- **Chomsky Hierarchy**: Classification of languages into four types based on grammar restrictions and computational power.