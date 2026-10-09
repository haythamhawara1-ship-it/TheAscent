# The Ascent

Working through **_The C Programming Language_** (K&R, 2nd edition) together.

## Layout

Each of us has our own folder, so we never edit the same files and never get merge conflicts.

```
Haytham/           <- Haytham's work
Nour/              <- Nour's work
shared-projects/   <- projects we build together
```

## Naming files

- Exercises: `ex1-01.c`, `ex1-02.c`, ... `ex5-13.c` (chapter-number, two-digit exercise number so they sort properly)
- Book examples you type out: a short descriptive name, e.g. `hello.c`, `fahr_celsius.c`
- Put a comment at the top of every file saying what it is:

```c
/* Exercise 1-3: Modify the temperature conversion program to print a heading. */
```

## Compiling and running

```sh
clang -Wall -Wextra -std=c11 Haytham/hello.c -o hello
./hello
```

(`gcc` works the same way.) The compiled program is ignored by git (see `.gitignore`), so only commit `.c` / `.h` files.

## Formatting

Code uses K&R style, configured in `.clang-format`. To auto-format a file:

```sh
clang-format -i Haytham/hello.c
```

In VS Code, install the **C/C++** extension and turn on *Format On Save*; it picks up `.clang-format` automatically.

## Daily git workflow

```sh
git pull                          # 1. get your friend's latest work FIRST
# ... write code ...
git status                        # 2. see what changed
git add Haytham/ex1-01.c          # 3. stage the file(s)  (or: git add .)
git commit -m "Add exercise 1-1"  # 4. save a snapshot with a message
git push                          # 5. upload to GitHub
```
