Syntax Error Detection and Recovery System
Team Details
Team Member Name	ID Number
G. Sirisha	2420030091
K.Mounika	2420030102
P.Manogna	2420030104
K.Siri	2420030213
Supervisor: P. Krishna Kishore

1. Project Title
Syntax Error Detection and Recovery System

2. Abstract
The Syntax Error Detection and Recovery System is a compiler-based application designed to detect, analyze, and recover from syntax errors in source code. The system performs lexical analysis and syntax analysis to convert source code into tokens and verify whether the program follows a predefined grammar. It identifies common syntax errors such as missing semicolons, unmatched brackets, missing parentheses, unexpected tokens, and invalid statement structures. For every detected error, the system provides the error location, type, expected token, found token, and a meaningful explanation.

A key feature of the system is its error recovery mechanism, which allows the parser to continue analyzing the source program instead of stopping at the first syntax error. Classical compiler techniques such as panic-mode recovery, phrase-level recovery, and error productions are used to recover from invalid input and resume parsing. The system can also generate a parse tree and recovered source representation to help users understand how the parser processes erroneous input.

The proposed system provides an interactive and educational platform for understanding syntax analysis and compiler error handling. It helps users identify multiple syntax errors in a single program, understand the cause of each error, and observe the recovery process. The project demonstrates important Compiler Design concepts while providing scope for future enhancements such as automated correction suggestions, advanced parsing techniques, multiple programming-language grammars, and graphical compiler-phase visualization.

3. Problem Statement
Syntax errors can interrupt the compilation process and make it difficult for programmers to identify and correct multiple errors efficiently. Traditional error reporting may provide limited information or stop parsing after encountering an error.

This project aims to develop a system that can detect syntax errors, identify their locations and causes, provide meaningful error messages, and recover from errors so that parsing can continue.

4. Objectives
No.	Objective
1	Perform lexical analysis and generate tokens.
2	Analyze source code using a predefined grammar.
3	Detect and classify syntax errors.
4	Identify the line and position of each error.
5	Display expected and found tokens.
6	Implement panic-mode error recovery.
7	Implement phrase-level error recovery.
8	Handle common errors using error productions.
9	Continue parsing after recoverable errors.
10	Generate parse trees for source programs.
11	Provide correction suggestions.
12	Display a clear error report through an interactive interface.
5. System Architecture
                         ┌──────────────────────────┐
                         │       SOURCE CODE        │
                         │      User Input/UI       │
                         └────────────┬─────────────┘
                                      │
                                      ▼
                         ┌──────────────────────────┐
                         │   LEXICAL ANALYZER       │
                         │                          │
                         │  Source Code → Tokens    │
                         └────────────┬─────────────┘
                                      │
                                      ▼
                         ┌──────────────────────────┐
                         │      TOKEN STREAM        │
                         │                          │
                         │ Keywords | IDs | Numbers │
                         │ Operators | Delimiters   │
                         └────────────┬─────────────┘
                                      │
                                      ▼
                         ┌──────────────────────────┐
                         │     SYNTAX ANALYZER      │
                         │                          │
                         │   Grammar Validation     │
                         └────────────┬─────────────┘
                                      │
                                      ▼
                         ┌──────────────────────────┐
                         │      PARSE TREE          │
                         │                          │
                         │  Syntactic Structure     │
                         └────────────┬─────────────┘
                                      │
                                      ▼
                         ┌──────────────────────────┐
                         │   ERROR DETECTION        │
                         │                          │
                         │ Missing / Extra /        │
                         │ Unexpected Tokens        │
                         └────────────┬─────────────┘
                                      │
                                      ▼
                         ┌──────────────────────────┐
                         │    ERROR RECOVERY        │
                         │                          │
                         │  • Panic Mode            │
                         │  • Phrase Level          │
                         │  • Error Productions     │
                         └────────────┬─────────────┘
                                      │
                                      ▼
                         ┌──────────────────────────┐
                         │   RECOVERED PROGRAM      │
                         │                          │
                         │ Corrected / Recovered    │
                         │ Source Representation    │
                         └────────────┬─────────────┘
                                      │
                                      ▼
                         ┌──────────────────────────┐
                         │     ERROR REPORT         │
                         │                          │
                         │ Line | Column | Type     │
                         │ Expected | Found         │
                         │ Suggestion | Recovery    │
                         └──────────────────────────┘
6. Architecture Components
Component	Description
Source Code Input	Accepts source code from the user.
Lexical Analyzer	Converts source code into meaningful tokens.
Token Stream	Stores keywords, identifiers, operators, literals, and delimiters.
Syntax Analyzer	Checks tokens according to the defined grammar.
Parse Tree	Represents the syntactic structure of the input.
Error Detector	Identifies violations of grammar rules.
Error Classifier	Determines the type and location of the syntax error.
Error Recovery Engine	Attempts to recover and continue parsing.
Recovered Program	Represents the source after applicable recovery operations.
Error Reporter	Displays detailed error information and suggestions.
User Interface	Provides source-code input and visual output.
7. Compiler Processing Flow
Source Code
     ↓
Lexical Analysis
     ↓
Token Generation
     ↓
Syntax Analysis
     ↓
Parse Tree Construction
     ↓
Syntax Error Detection
     ↓
Error Classification
     ↓
Error Recovery
     ↓
Recovered Parse Tree
     ↓
Error Report
     ↓
Correction Suggestion
8. Main Features
Feature	Description
Source Code Editor	Allows users to enter or paste source code.
Lexical Analysis	Generates tokens from source code.
Syntax Analysis	Validates program structure.
Syntax Error Detection	Detects grammar violations.
Error Classification	Categorizes detected errors.
Line & Column Detection	Shows the exact error location.
Expected Token Detection	Shows the token expected by the parser.
Unexpected Token Detection	Shows the token actually encountered.
Panic Mode Recovery	Skips invalid tokens and resumes parsing.
Phrase-Level Recovery	Performs local corrections.
Error Productions	Handles predefined common mistakes.
Multiple Error Detection	Reports more than one error in a single program.
Parse Tree Visualization	Displays syntactic structure.
Correction Suggestions	Provides possible corrections.
9. Technologies Used
Category	Technology
Programming Language	Python
Frontend	HTML, CSS, JavaScript
Compiler Implementation	Python
Parsing	Recursive Descent / Predictive Parsing
Grammar	Context-Free Grammar
Visualization	HTML, CSS, JavaScript
Database	Not Required
Version Control	Git
Repository Hosting	GitHub
10. Project Structure
SyntaxErrorDetectionRecovery/
│
├── backend/
│   │
│   ├── lexer/
│   │   ├── lexer.py
│   │   └── tokens.py
│   │
│   ├── parser/
│   │   ├── parser.py
│   │   ├── grammar.py
│   │   └── parse_tree.py
│   │
│   ├── error_detection/
│   │   └── error_detector.py
│   │
│   ├── error_recovery/
│   │   ├── panic_mode.py
│   │   ├── phrase_level.py
│   │   └── error_productions.py
│   │
│   ├── analyzer/
│   │   └── syntax_analyzer.py
│   │
│   ├── reports/
│   │   └── error_report.py
│   │
│   └── main.py
│
├── frontend/
│   ├── index.html
│   ├── style.css
│   └── script.js
│
├── tests/
│   ├── valid_programs/
│   └── invalid_programs/
│
├── requirements.txt
├── .gitignore
└── README.md
11. Module Description
Module	File	Responsibility
Lexer	lexer.py	Converts source code into tokens.
Token Definition	tokens.py	Defines token types.
Grammar	grammar.py	Defines grammar rules.
Parser	parser.py	Performs syntax analysis.
Parse Tree	parse_tree.py	Creates the parse tree.
Error Detection	error_detector.py	Detects syntax errors.
Panic Recovery	panic_mode.py	Implements panic-mode recovery.
Phrase Recovery	phrase_level.py	Performs local error corrections.
Error Productions	error_productions.py	Handles common syntax mistakes.
Analyzer	syntax_analyzer.py	Integrates analysis modules.
Report Generator	error_report.py	Creates error reports.
Main Application	main.py	Starts the backend application.
12. Grammar
The project will use a controlled grammar for the supported programming constructs.

program
    → statement*

statement
    → declaration
    | assignment
    | if_statement
    | print_statement

declaration
    → type identifier = expression ;

assignment
    → identifier = expression ;

if_statement
    → if ( condition ) { statement* }

print_statement
    → print ( expression ) ;

condition
    → expression relational_operator expression

expression
    → term ((+ | -) term)*

term
    → factor ((* | /) factor)*

factor
    → identifier
    | number
    | ( expression )

type
    → int
    | float
    | string
13. Error Types
Error Type	Example
Missing Semicolon	int a = 10
Missing Parenthesis	if (a > b {
Missing Brace	if (a > b) {
Unmatched Bracket	(a + b]
Unexpected Token	int = 10;
Invalid Expression	a + * b
Extra Token	int a = 10;;
Invalid Statement	Incorrect statement structure
14. Error Recovery Techniques
Panic Mode Recovery
Invalid Token
      ↓
Skip Tokens
      ↓
Find Synchronizing Token
      ↓
Resume Parsing
Typical synchronization tokens:

;
}
)
{
Phrase-Level Recovery
Detected Error
      ↓
Check Expected Token
      ↓
Insert / Delete / Replace Token
      ↓
Continue Parsing
Error Productions
Common mistakes are represented explicitly in the grammar to provide meaningful error messages.

15. Example
Input
int a = 10
int b = 20;

if (a > b {
    print(a);
}
Error Report
Error	Line	Type	Expected	Found	Recovery
1	1	Missing Semicolon	;	int	Phrase-Level
2	4	Missing Parenthesis	)	{	Phrase-Level
Recovered Code
int a = 10;
int b = 20;

if (a > b) {
    print(a);
}
16. User Interface Structure
┌──────────────────────────────────────────────────────────────┐
│       SYNTAX ERROR DETECTION AND RECOVERY SYSTEM             │
├───────────────────────────────┬──────────────────────────────┤
│                               │                              │
│        SOURCE CODE            │        ERROR REPORT          │
│                               │                              │
│  1  int a = 10                │  Line 1                     │
│  2  int b = 20;               │  Missing ';'                │
│  3  if (a > b {               │  Expected: ;                │
│  4      print(a);              │  Found: int                 │
│  5  }                          │                              │
│                               │  Line 3                     │
│                               │  Missing ')'                │
│                               │  Expected: )                │
│                               │  Found: {                   │
├───────────────────────────────┴──────────────────────────────┤
│ [ Analyze Code ]   [ Recover Errors ]   [ Clear ]            │
├──────────────────────────────────────────────────────────────┤
│                         TOKENS                                │
├──────────────────────────────────────────────────────────────┤
│ int | ID | = | NUMBER | int | ID | = | NUMBER | ; | ...      │
├──────────────────────────────────────────────────────────────┤
│                     RECOVERED CODE                            │
├──────────────────────────────────────────────────────────────┤
│ int a = 10;                                                   │
│ int b = 20;                                                   │
│                                                               │
│ if (a > b) {                                                  │
│     print(a);                                                 │
│ }                                                             │
└──────────────────────────────────────────────────────────────┘
17. Functional Requirements
ID	Requirement
FR-01	The system shall accept source code as input.
FR-02	The system shall perform lexical analysis.
FR-03	The system shall generate tokens.
FR-04	The system shall perform syntax analysis.
FR-05	The system shall detect syntax errors.
FR-06	The system shall identify line and column numbers.
FR-07	The system shall display expected and found tokens.
FR-08	The system shall classify syntax errors.
FR-09	The system shall apply error-recovery techniques.
FR-10	The system shall continue parsing after recoverable errors.
FR-11	The system shall generate an error report.
FR-12	The system shall provide correction suggestions.
FR-13	The system shall display recovered source code.
FR-14	The system shall visualize the parse tree.
18. Testing
Test Case	Input	Expected Result
TC-01	Valid program	No syntax errors
TC-02	Missing ;	Missing semicolon detected
TC-03	Missing )	Missing parenthesis detected
TC-04	Missing }	Missing brace detected
TC-05	Unexpected token	Unexpected token reported
TC-06	Invalid expression	Expression error reported
TC-07	Multiple errors	Multiple errors detected
TC-08	Unmatched brackets	Bracket mismatch detected
19. Installation and Execution
Prerequisites
Requirement	Version / Tool
Python	3.10+
Git	Latest stable version
Web Browser	Chrome / Edge / Firefox
Code Editor	VS Code recommended
Clone Repository
git clone <YOUR-GITHUB-REPOSITORY-URL>
cd SyntaxErrorDetectionRecovery
Create Virtual Environment
python -m venv venv
Activate Virtual Environment
Windows
venv\Scripts\activate
Linux / macOS
source venv/bin/activate
Install Dependencies
pip install -r requirements.txt
Run Backend
python backend/main.py
Run Frontend
Open:

frontend/index.html
20. Development Phases
Phase	Activity	Status
Phase 1	Project Selection	✅ Completed
Phase 2	Problem Definition	✅ Completed
Phase 3	Requirement Analysis	🔄 In Progress
Phase 4	Grammar Design	⏳ Pending
Phase 5	Lexical Analyzer	⏳ Pending
Phase 6	Parser	⏳ Pending
Phase 7	Parse Tree	⏳ Pending
Phase 8	Error Detection	⏳ Pending
Phase 9	Error Recovery	⏳ Pending
Phase 10	Frontend	⏳ Pending
Phase 11	Integration	⏳ Pending
Phase 12	Testing	⏳ Pending
Phase 13	Documentation	⏳ Pending
Phase 14	Final Demonstration	⏳ Pending
21. Team Responsibilities
Team Member	Primary Work	Supporting Work
G. Sirisha	Lexical Analyzer and Parser	Parser Integration
K. Mounika	Error Detection and Recover	Testing
K. Siri	Frontend Development	System Integration
22. Expected Output
The completed system will be able to:

✓ Accept source code
✓ Generate tokens
✓ Validate syntax
✓ Detect syntax errors
✓ Identify error location
✓ Classify errors
✓ Show expected and found tokens
✓ Recover from syntax errors
✓ Continue parsing after errors
✓ Generate recovered code
✓ Generate parse trees
✓ Display correction suggestions
✓ Provide a complete error report
23. Future Enhancements
Enhancement	Description
Multiple Language Support	Support C, Java, or Python-like grammars
Advanced Parsing	Add LL(1), SLR, LR, or LALR parsing
Smart Correction	Improve automatic correction suggestions
Parse Tree Visualization	Interactive graphical parse trees
Grammar Editor	Allow users to define grammar rules
Syntax Highlighting	Highlight keywords, identifiers, and errors
Error Statistics	Display error-frequency statistics
Report Export	Export error reports
Compiler Visualization	Visualize all compiler phases
Web Deployment	Deploy the application online
24. Limitations
Limitation	Description
Limited Grammar	Initial version supports a predefined grammar
Syntax Focus	Primarily handles syntax errors
No Runtime Execution	Source programs are not executed
Limited Automatic Correction	Only recoverable errors are corrected
No Full Compiler Backend	Machine-code generation is outside the initial scope
25. Project Scope
                 SYNTAX ERROR DETECTION
                         AND
                    RECOVERY SYSTEM
                           │
          ┌────────────────┼────────────────┐
          │                │                │
          ▼                ▼                ▼
      LEXICAL          SYNTAX           ERROR
      ANALYSIS         ANALYSIS         HANDLING
          │                │                │
          ▼                ▼                ▼
       Tokens          Parse Tree      Detection
                                           │
                                           ▼
                                       Recovery
                                           │
                              ┌────────────┼────────────┐
                              ▼            ▼            ▼
                          Panic Mode   Phrase Level   Error
                                                       Productions
26. Conclusion
The Syntax Error Detection and Recovery System is designed to provide a practical implementation of syntax analysis and error handling concepts in Compiler Design. The system processes source code through lexical analysis, token generation, syntax analysis, parse-tree construction, error detection, and error recovery. By using techniques such as panic-mode recovery, phrase-level recovery, and error productions, the system can continue parsing after encountering recoverable syntax errors and provide meaningful information to the user. The modular architecture makes the project easy to develop, test, demonstrate, and extend with advanced parsing and correction techniques.

Supervisor
P. Krishna Kishore

Team
S.No.	Name	ID Number
1	G. Sirisha	2420030091
2	K.Mounika	2420030102
3	P.Manogna	2420030104
4	K.Siri	2420030213
