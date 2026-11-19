# Contributing — Historical Codebase Reference

> This repository is an archive of inherited work from the former Nervestack / NSPL project. The former identity is not current branding; successor identity is undecided. The Programming Language (PL) Division Unit is **CLOSED / NOT OPERATING**. This guide documents the historical development layout and does not announce an active contribution programme.

The source tree is retained for inspection, preservation and technical continuity. No ongoing maintenance or support commitment is implied.

## Historical project structure

```
├── src/                  # Preserved frontend and runtime source
├── third_party/          # Third-party dependencies
├── tools/                # Legacy editor extension and scripts
├── docs/                 # Historical documentation
├── examples/             # Legacy source examples
├── tests/                # Historical test suite
└── README.md             # Current archive status
```

## Historical build and test notes

The commands below are retained as reference only; dependencies, paths and build behaviour may have changed.

```bash
cd src/runtime
# On Windows, the historical build script was:
.uild.bat
```

```bash
py src/frontend/frontend.py examples/your_file.NSPL
py tests/test_runner.py
```

Consult [IMPLEMENTATION_STATUS.md](./IMPLEMENTATION_STATUS.md) for the historical feature record. Its claims have not been independently re-verified.

## Legacy VS Code extension

The package in `tools/vscode_extension/` retains its former language ID, grammar scope and `.nspl` extension for compatibility with existing files. These identifiers are historical, not approved successor branding.

For the current organisational and preservation position, see the root [README](../README.md).
