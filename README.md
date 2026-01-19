# Rust Skills

> 179 production-ready Rust guidelines for AI coding agents

A comprehensive set of Rust best practices designed for AI coding assistants. Works with Claude Code, Cursor, Windsurf, GitHub Copilot, OpenAI Codex, Aider, Zed, Amp, and 20+ other agents.

## Quick Install

```bash
npx add-skill leonardomso/rust-skills
```

Or using the skills CLI:

```bash
npx skills add leonardomso/rust-skills
```

## Usage

Once installed, invoke the skill in your agent:

```
/rust-skills Review my error handling code
```

```
/rust-skills Check this async code for issues
```

```
/rust-skills Help me design a public API for this module
```

```
/rust-skills Optimize memory usage in this function
```

## What's Included

### 14 Categories, 179 Rules

| Category | Rules | Impact | Description |
|----------|-------|--------|-------------|
| **Ownership & Borrowing** | 12 | CRITICAL | Borrow over clone, Arc/Rc, lifetimes |
| **Error Handling** | 12 | CRITICAL | thiserror/anyhow, context chains, `?` |
| **Memory Optimization** | 15 | CRITICAL | SmallVec, arenas, zero-copy patterns |
| **API Design** | 15 | HIGH | Builder pattern, newtypes, sealed traits |
| **Async/Tokio** | 15 | HIGH | spawn_blocking, channels, cancellation |
| **Compiler Optimization** | 12 | HIGH | LTO, inlining, PGO, SIMD |
| **Naming Conventions** | 16 | MEDIUM | Rust API Guidelines naming rules |
| **Type Safety** | 10 | MEDIUM | Newtype pattern, parse don't validate |
| **Testing** | 13 | MEDIUM | Proptest, mockall, criterion |
| **Documentation** | 11 | MEDIUM | Doc examples, intra-doc links |
| **Performance Patterns** | 11 | MEDIUM | Iterators, entry API, collect patterns |
| **Project Structure** | 11 | LOW | Workspaces, module organization |
| **Clippy & Linting** | 11 | LOW | Lint configuration, CI setup |
| **Anti-patterns** | 15 | REFERENCE | Common mistakes to avoid |

## Manual Installation

<details>
<summary><strong>Claude Code</strong></summary>

**Global (all projects):**
```bash
git clone https://github.com/leonardomso/rust-skills.git ~/.claude/skills/rust-skills
```

**Project-specific:**
```bash
git clone https://github.com/leonardomso/rust-skills.git .claude/skills/rust-skills
```
</details>

<details>
<summary><strong>OpenCode</strong></summary>

```bash
git clone https://github.com/leonardomso/rust-skills.git .opencode/skills/rust-skills
```
</details>

<details>
<summary><strong>Cursor</strong></summary>

```bash
git clone https://github.com/leonardomso/rust-skills.git .cursor/skills/rust-skills
```

Or copy to `.cursorrules`:
```bash
curl -o .cursorrules https://raw.githubusercontent.com/leonardomso/rust-skills/master/SKILL.md
```
</details>

<details>
<summary><strong>Windsurf</strong></summary>

```bash
mkdir -p .windsurf/rules
curl -o .windsurf/rules/rust-skills.md https://raw.githubusercontent.com/leonardomso/rust-skills/master/SKILL.md
```
</details>

<details>
<summary><strong>OpenAI Codex</strong></summary>

```bash
git clone https://github.com/leonardomso/rust-skills.git .codex/skills/rust-skills
```

Or use AGENTS.md:
```bash
curl -o AGENTS.md https://raw.githubusercontent.com/leonardomso/rust-skills/master/SKILL.md
```
</details>

<details>
<summary><strong>GitHub Copilot</strong></summary>

```bash
mkdir -p .github
curl -o .github/copilot-instructions.md https://raw.githubusercontent.com/leonardomso/rust-skills/master/SKILL.md
```
</details>

<details>
<summary><strong>Aider</strong></summary>

Add to `.aider.conf.yml`:
```yaml
read: path/to/rust-skills/SKILL.md
```

Or run with:
```bash
aider --read path/to/rust-skills/SKILL.md
```
</details>

<details>
<summary><strong>Zed</strong></summary>

Zed supports AGENTS.md. Copy to your project root:
```bash
curl -o AGENTS.md https://raw.githubusercontent.com/leonardomso/rust-skills/master/SKILL.md
```
</details>

<details>
<summary><strong>Amp (Sourcegraph)</strong></summary>

```bash
git clone https://github.com/leonardomso/rust-skills.git .agents/skills/rust-skills
```
</details>

<details>
<summary><strong>Cline / Roo Code</strong></summary>

```bash
mkdir -p .clinerules
curl -o .clinerules/rust-skills.md https://raw.githubusercontent.com/leonardomso/rust-skills/master/SKILL.md
```
</details>

<details>
<summary><strong>AGENTS.md Standard</strong></summary>

For any agent supporting the [AGENTS.md](https://agents.md) standard:
```bash
curl -o AGENTS.md https://raw.githubusercontent.com/leonardomso/rust-skills/master/SKILL.md
```
</details>

## Full Rule Index

See [SKILL.md](./SKILL.md) for the complete rule index with links to individual rule files.

Each rule file in `rules/` contains:
- Brief explanation of why it matters
- Bad code example
- Good code example
- Additional context and references

## Sources

These guidelines synthesize best practices from:
- [Rust API Guidelines](https://rust-lang.github.io/api-guidelines/)
- [Rust Performance Book](https://nnethercote.github.io/perf-book/)
- [Rust Design Patterns](https://rust-unofficial.github.io/patterns/)
- Production codebases: ripgrep, tokio, serde, polars, axum
- Clippy lint documentation

## Contributing

Contributions welcome! Please follow the existing rule format when adding new rules.

## License

MIT
