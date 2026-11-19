# Historical Programming Language Context (Formerly NSPL v2.0)

> **Historical reference notice — 19 November 2026:** This document preserves implementation and syntax context from the former Nervestack / NSPL project. Those identifiers remain only for technical continuity and provenance; they are not current branding. Successor project and language identities are undecided. The Programming Language (PL) Division Unit is **CLOSED / NOT OPERATING**, and naming exploration is paused. See the repository [README](../README.md) for current status.

---

**Overview**

The former project implemented an interpreted language with a Python frontend (lexer/parser) and a C-based runtime (interpreter), communicating via a JSON AST. Details below are preserved as historical implementation notes and should be checked against source before being treated as current behaviour.

## 1. Syntax & Structure

### Comments

- **Single-line:** `< This is a comment >`
- **Multi-line:** `<^ This is a\nmulti-line comment ^>`

### Variables & Constants

- **Constants:** `firm name = value` (Immutable)
- **Variables:** `name = value` (Mutable, created on assignment)
- **Types:** `Num` (Integer/Float), `Text` (String), `On`/`Off` (Boolean), `Nil`
- **String Interpolation:** `"Value: |variable|"`

### Collections (Packs)

- **Syntax:** `pack(item1, item2, ...)`
- **Access:** `list~>0` (The `~>` operator is the exclusive access operator; `.` is invalid)
- **Example:**
  ```nervestack
  firm numbers = pack(1, 2, 3)
  firm mixed = pack("A", 42, On)
  ```

### Control Flow

```nervestack
when x > 10:
    show "High"
otherwise when x > 5:
    show "Medium"
otherwise:
    show "Low"
done

traverse i from 1 to 10:
    show i
done
```

### Functions

- **Keyword:** `spec`
- **Return:** `forward value` or `giving value` (deprecated in the historical notes)

```nervestack
spec add(a, b):
    forward a + b
done

firm result = add(10, 20)
```

### Error Handling

```nervestack
attempt:
    trigger "ErrorName"
trap "ErrorName":
    show "Caught error"
done
```

## 2. Object-Oriented Programming (OOP)

### Blueprints (Classes)

```nervestack
blueprint Dog:
    has name
    has age

    < Constructor >
    prep (n, a):
        own~>name = n
        own~>age = a
    done

    < Method >
    spec bark:
        show "|own~>name| says Woof!"
    done
done
```

### Instantiation & Usage

```nervestack
firm myDog = spawn Dog("Buddy", 5)
myDog~>bark()
show myDog~>age
```

## 3. Modules

- **Import:** `bring "module_name"`
- **Toolkit (Library):** `toolkit Math:` ... `done`

## 4. Historical Execution Model

1. **Frontend:** Parses legacy `.NSPL` source and generates a JSON AST.
2. **Runtime:** Loads the JSON AST and executes the program.
3. Performance, memory-management and backend claims are not independently verified by this historical note.

## 5. Historical Key Keywords

`firm`, `show`, `spec`, `prep`, `blueprint`, `spawn`, `pack`, `each`, `when`, `otherwise`, `attempt`, `trap`, `trigger`, `forward`, `own`, `adopt`.
