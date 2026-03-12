# Chapter 1 — Shell Basics

This chapter introduces the core shell commands and how to navigate and inspect files.

## ✅ Exercises
- Use `pwd` to print the current working directory.
- List files with `ls`, including hidden files: `ls -la`.
- Read a file with `cat`, `less`, or `more`.
- Use `echo` and `printf` to print text.
- Use command history: `history` and `!!`.

## 📋 Example commands
```bash
pwd
ls -la
cat example.txt
echo "Hello Linux"
history | tail -n 10
```

## 📝 Files in this folder
- `example.txt` — sample text file to read with `cat`.
- `README.md` — this guide.

---

## 🧪 Try it in a real Linux environment (WSL/Docker)
```bash
cd /workspace/01-shell-basics
cat example.txt
ls -la
```