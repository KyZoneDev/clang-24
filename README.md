# clang-24

Prebuilt LLVM/Clang **24.0.0git** (built from `llvm/llvm-project` `main`) with `lld` and LLVM binutils,
intended for building Android kernels (`LLVM=1 LLVM_IAS=1`).

- Host: Linux x86_64 (Ubuntu runner), libstdc++ statically linked.
- Targets: AArch64, ARM, X86.
- Releases: see the *Releases* page. Archive layout has `bin/` at the root:

```bash
mkdir clang && wget -qO- <release .tar.gz url> | tar -xz -C clang
export PATH=$PWD/clang/bin:$PATH
```

Build manually: Actions -> *Build Clang* -> Run workflow (optionally give an llvm-project ref).
