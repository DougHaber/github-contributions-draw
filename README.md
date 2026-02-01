# draw-commits

Small script that creates backdated empty Git commits to "draw" a pattern on a Git contribution graph.

## How it works

- Reads up to 7 lines of text from stdin or a file.
- Any non-space character becomes a commit.
- Commits are dated at noon for each day in the target year.
- One commit per day. No fancy shading support.

## Usage

When run inside a Git repo, this script will add commits. Within seconds of pushing, GitHub updates the contribution graph.

Run inside a Git repository:

```bash
./draw-commits -y 2025 pattern.txt
```

Dry run (prints what would be committed):

```bash
./draw-commits -y 2025 --dry-run pattern.txt
```

You can also pipe in a 7-line pattern:

```bash
banner "Hello" | ./draw-commits -y 2025
```

## License

BSD-3-Clause. See `LICENSE`.
