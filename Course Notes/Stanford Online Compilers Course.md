# Week 1
## Introduction
There are 2 main approaches to implementing programming languages -
- Interpreters
	- Takes your program and data and produces an output
- Compilers
	- Takes your program and gives out an executable, which is then run separately on your data. That will product the output.

Formula Translation Project, led by John Backus, led to development of FORTRAN 1
- The first compiler
- Modern compilers still preserve the outline of FORTRAN 1

Structure of FORTRAN 1
1. Lexical Analysis
2. Parsing
3. Semantic Analysis
4. Optimization
5. Code Generation

## Structure of a compiler
How computers understand a program - Taking the analogy of how humans understand language
- Step 1: Humans understand words in a sentences. Lexical Analysis divides a program text into "words" or "tokens"
	- For example in -
		if x == y then z = 1; else z = 2;
		if, x, , ;, =, blank spaces etc are all tokens.

- Step 2: Parsing
	- Once humans understand the words, in the next step they try to understand the sentence structure.
	- Parsing is diagramming sentences. The diagram is a tree.
	- From a conversation with ChatGPT -
		- **Parsing:** Parsing is the process of analyzing a sentence or a piece of text into its grammatical components, such as nouns, verbs, adjectives, adverbs, prepositions, conjunctions, and so on. It involves understanding the syntactic structure of the sentence and how each word functions within that structure. Parsing helps us identify the relationships between words and how they come together to form meaningful expressions.
		- **Diagramming Sentences:** Diagramming sentences is a visual method of representing the grammatical structure of a sentence. In this approach, different parts of speech and their relationships are represented using specific symbols and lines. For example, a simple sentence like "The cat sat on the mat" might be diagrammed as:
		-   The cat
		    |        \
		   sat      on
		         \
	             mat
