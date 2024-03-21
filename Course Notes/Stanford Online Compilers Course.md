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
		- **Diagramming Sentences:** Diagramming sentences is a visual method of representing the grammatical structure of a sentence. In this approach, different parts of speech and their relationships are represented using specific symbols and lines.
- Parsing an English sentence -
![sentence](https://milanxchauhan.notion.site/image/https%3A%2F%2Fprod-files-secure.s3.us-west-2.amazonaws.com%2F8447141e-4ed1-44ed-a146-204aece2647f%2F00f9716b-de56-4454-9089-176f282ed24b%2FUntitled.png?table=block&id=47d1c504-6276-412d-84ed-4f14d2574b54&spaceId=8447141e-4ed1-44ed-a146-204aece2647f&width=2000&userId=&cache=v2)
- Parsing a code statement -
![code](https://milanxchauhan.notion.site/image/https%3A%2F%2Fprod-files-secure.s3.us-west-2.amazonaws.com%2F8447141e-4ed1-44ed-a146-204aece2647f%2Fade01085-de31-4463-aa0a-054b36519f93%2FUntitled.png?table=block&id=65aaa17c-27c4-4399-811c-d6f9e8761654&spaceId=8447141e-4ed1-44ed-a146-204aece2647f&width=1420&userId=&cache=v2)

- Step 3: Semantic Analysis
	- Once sentence structure is understood, we can try to understand the "meaning" of that sentence.
	- Semantic analysis refers to the process of understanding the meaning of words, phrases, sentences, or entire texts within a given context. It involves interpreting the relationships between words, identifying the intended message or information conveyed, and extracting the underlying semantics or logical structure of the content.
	- Compilers perform limited semantic analysis to catch inconsistencies.
	- Ambiguities in the English language can make it hard to understand what is being conveyed. For example in the sentence - Jack said Jerry left his assignment at home. Here 'his' could refer to either Jack or Jerry.
	- Programming languages define strict rules (for example - variable bindings) to avoid such ambiguities.

- Step 4: Optimization
	- Optimization is similar to editing an article in English.
	- Optimization involves modifying programs so that they -
		- Run faster
		- Use less memory
	- We have to make whether we are actually optimizing the code or not. For example -
		X = Y * 0 is the same as X = 0
		This feels like an optimization, but this only works if X & Y are integers. In case of NaN, this in invalid. Because -
		NaN * 0 = NaN

- Step 5: Code Generation
	- It involves translating the intermediate representation of a program (often in the form of an abstract syntax tree or intermediate code) into the actual executable machine code. Intermediate representation is like breaking a big puzzle or story into smaller, easier parts so that the computer can understand and work on them step by step.
	- Code Gen produces assembly code (usually)