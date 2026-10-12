# Common Programming Naming Conventions

Naming conventions are standardized patterns for formatting multi-word identifiers (such as variable names, function names, classes, constants, and file paths) in source code.

---

## Quick Reference Summary

| Convention | Pattern Example | Common Use Cases |
| :--- | :--- | :--- |
| **camelCase** | `myVariableName` | JS/TS variables, Java methods, Go unexported identifiers |
| **PascalCase** | `MyClassName` | Classes, types, interfaces, React components |
| **snake_case** | `my_variable_name` | Python variables/functions, Rust, SQL columns |
| **SCREAMING_SNAKE_CASE** | `MAX_BUFFER_SIZE` | Global constants, environment variables, enum values |
| **kebab-case** | `my-variable-name` | URLs, CSS class names, HTML attributes, package names |
| **SCREAMING-KEBAB-CASE** | `MY-VARIABLE-NAME` | HTTP headers, legacy systems (COBOL) |
| **flatcase** | `myvariablename` | Package names in Java/Go, database names |
| **UPPERFLATCASE** | `MYVARIABLENAME` | Legacy macro definitions, assembly labels |
| **Hungarian Notation** | `strUserName`, `bIsValid` | Win32 API, older C/C++ codebases |

---

## Detailed Breakdown

### 1. camelCase (Lower Camel Case)
- **Format:** The first letter is lowercase; the first letter of each subsequent concatenated word is capitalized. No delimiters.
- **Example:** `userProfileId`, `calculateTotalPrice()`, `isAvailable`
- **Common Ecosystems:**
  - **JavaScript / TypeScript:** Variables, object properties, functions, methods.
  - **Java:** Method names, field/variable names.
  - **C# / Swift / Kotlin:** Local variables, parameters, function names.
  - **Go:** Unexported (package-private) functions and variables.

---

### 2. PascalCase (Upper Camel Case)
- **Format:** The first letter of every concatenated word is capitalized. No delimiters.
- **Example:** `UserProfileController`, `CalculateTotal()`, `CustomerRecord`
- **Common Ecosystems:**
  - **Object-Oriented Languages (C#, Java, C++, TypeScript):** Class names, interface names, type aliases, structs, enums.
  - **React / UI Frameworks:** Component names (`UserProfile.jsx`, `<NavigationMenu />`).
  - **C#:** Method and property names (unlike Java/JS, C# prefers PascalCase for methods).
  - **Go:** Exported (public) functions, structs, and variables.

---

### 3. snake_case (Pothole Case)
- **Format:** All lowercase characters, with words separated by an underscore (`_`).
- **Example:** `user_profile_id`, `calculate_total_price()`, `order_items`
- **Common Ecosystems:**
  - **Python:** Variable names, function names, module/file names (per PEP 8).
  - **Rust:** Function names, variable names, module names.
  - **Ruby:** Method names, variable names, file names.
  - **SQL & Databases:** Table names and column identifiers (`first_name`, `created_at`).
  - **C / C++:** Standard library naming (`std::vector::push_back`).

---

### 4. SCREAMING_SNAKE_CASE (MACRO_CASE / UPPER_SNAKE_CASE)
- **Format:** All uppercase characters, with words separated by an underscore (`_`).
- **Example:** `API_BASE_URL`, `MAX_RETRY_COUNT`, `DEFAULT_TIMEOUT_MS`
- **Common Ecosystems:**
  - **Universal:** Global constants, configuration parameters, and compile-time constants.
  - **Environment Variables:** `.env` files (`DATABASE_URL`, `PORT`).
  - **Languages (Java, C, C++, Python, TypeScript):** Enum values and constants marked `final` or `const`.

---

### 5. kebab-case (Lisp-case / Dash-case)
- **Format:** All lowercase characters, with words separated by a hyphen (`-`).
- **Example:** `user-profile-id`, `main-navigation-menu`, `button-primary`
- **Common Ecosystems:**
  - **Web Technologies:** HTML custom elements, CSS class names, HTML data attributes (`data-user-id`).
  - **Web URLs / Slugs:** REST endpoints, route slugs (`/api/v1/user-profiles`).
  - **Package Registries:** npm package names, Git branch names (`feature/user-auth`).
  - **Languages:** Lisp, Clojure, Racket (where `-` is a valid identifier character).

---

### 6. Hungarian Notation
- **Format:** A prefix indicating the data type or scope precedes the variable name.
  - *Systems Hungarian:* Prefixes physical data type (`strName` for string, `iCount` for integer, `bActive` for boolean).
  - *Apps Hungarian:* Prefixes logical purpose (`rwPosition` for row, `colPosition` for column).
- **Example:** `strCustomerName`, `pNextNode` (pointer), `bIsEnabled`
- **Common Ecosystems:**
  - Historical Windows Win32 API programming (C/C++).
  - Largely discouraged in modern typed languages with IDE type inspection, though boolean prefixes (`is...`, `has...`, `can...`) remain widely adopted.

---

## Best Practices Across Languages

1. **Maintain Internal Consistency:** Follow the established convention of the existing codebase or team style guide.
2. **Follow Language Idioms:**
   - Python: [PEP 8](https://peps.python.org/pep-0008/)
   - Java: [Oracle Code Conventions](https://www.oracle.com/java/technologies/javase/codeconventions-namingconventions.html)
   - C#: [Microsoft C# Coding Conventions](https://learn.microsoft.com/en-us/dotnet/csharp/fundamentals/coding-style/coding-conventions)
   - Go: [Effective Go Naming](https://go.dev/doc/effective_go#names)
3. **Be Intention-Revealing:** Choose descriptive names over abbreviations (e.g., `userAccount` instead of `usrAcc`).