# Universal User-Oriented Programming (UOP)

> **Historical reference notice — 19 November 2026:** This document preserves UOP material created under the former Nervestack / NSPL identity. Those names are historical identifiers, not current branding. The successor project and language identities remain undecided. The Programming Language (PL) Division Unit is **CLOSED / NOT OPERATING**; naming exploration is paused. This document is retained for technical and historical reference and does not indicate an active product or operating division. See the repository [README](../README.md) for current status.

---

Universal User-Oriented Programming (UOP) is the design philosophy historically associated with the Nervestack language. It prioritizes human readability, intuition, and clarity, aiming to bridge the gap between human thought processes and machine execution.

---

## The Core Principles of UOP

1. **Human-Centric Keywords:** Language constructs are named with common words that clearly describe their function (e.g., `ask`, `show`, `when`, `attempt`). This minimizes the cognitive load required to understand the code's intent.
2. **Intuitive Structure:** The syntax is designed to follow the logical flow of human thought. For example, error handling with `attempt-trap` reads like a plain-language description of trying an action and catching a problem.
3. **Clarity Over Brevity:** The historical design emphasizes clarity over cryptic symbols and abbreviations.
4. **Universal Accessibility:** The historical design aimed to be approachable for a wide audience, including beginners, educators, artists, and engineers.

---

## Historical Implementation Approach

The former implementation combined a Python frontend with a C/C++ runtime. The exact implementation details vary across project stages and should be checked against the corresponding source code; this historical description is not a performance certification or comparative claim.

## UOP in Practice

UOP was reflected in the former language's syntax and modular structure.

| Feature | Historical UOP implementation | Rationale |
|---|---|---|
| **Functions** | `spec` | "Specification" implies defining a clear behavior. |
| **Interfaces** | `bridge` | A "bridge" is a relatable metaphor for connecting separate things. |
| **Modules** | `toolkit` | A "toolkit" is an intuitive name for a collection of reusable tools. |
| **Conditionals** | `when`, `otherwise` | These words describe decision-making. |
| **Error Handling** | `attempt`, `trap`, `trigger` | This vocabulary frames error handling as an active process. |
| **Input/Output** | `ask`, `show` | These are direct, action-oriented words for user interaction. |

**Historical example:**

```nervestack
spec login:
    firm username = ask "Enter your username: "
    firm password = ask "Enter your password: "

    attempt:
        funcall authenticate(username, password)
        show "Welcome back!"
    trap AuthenticationError:
        show "Login failed. Please check your credentials."
    done
done
```

---

## UOP and Traditional Paradigms

UOP can be understood as a design philosophy that places emphasis on the user's mental model and the clarity of code intent. This is a conceptual comparison, not a claim that UOP supersedes other paradigms or that it has been validated as a distinct formal paradigm.

| Aspect | UOP (historical formulation) | Traditional OOP/procedural approaches |
|---|---|---|
| **Primary Focus** | The user's mental model and clarity of intent. | Data structures, objects and procedures. |
| **Syntax** | Natural-language-inspired, semantic keywords. | Varies by language and implementation. |
| **Goal** | Make code a medium for clear communication. | Provide precise instructions for execution. |
| **Performance** | Depends on the implementation. | Depends on the implementation. |

---

## Conclusion

UOP is a design philosophy preserved in this repository's historical language-design work. Its central emphasis is the human user: both the developer writing code and the end-user interacting with software.
