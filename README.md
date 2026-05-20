# SKILLS

Reusable Cursor agent skills for software engineering workflows. These skills are generic and can be dropped into any repository.

## Skills

| Skill | Purpose |
|-------|---------|
| `implement/` | Write production-grade code following SOLID, YAGNI, DRY, and fail-closed principles |
| `write-design/` | Write structured design documents for new features and integrations |
| `review-design/` | Review design documents against the codebase with detailed findings |
| `revise-design/` | Critically assess review feedback and revise design docs accordingly |
| `code-review/` | Perform thorough two-level code reviews (line-by-line + systemic impact) |

## Usage

### In Cursor

Reference a skill in chat with `@`:

```
@skills/implement/SKILL.md Implement the login feature
@skills/code-review/SKILL.md Review the changes in src/auth/
```

### Adding to your repo

Copy the skills you want into your repo's `skills/` directory. Then create a `skills/context.md` with your repo-specific conventions (language, toolchain, naming, key paths). Each skill opens with a reference to `context.md` for local details.

```
your-repo/
  skills/
    context.md              <-- your repo's conventions
    implement/SKILL.md
    code-review/SKILL.md
    ...
```

See the `context.md` in the [permit0 repo](https://github.com/permit0-ai/permit0) for a reference example.

## Workflow

The skills form a lifecycle:

```
Plan --> Review Plan --> Revise Plan --> Implement --> Review Code
 |           |               |              |             |
 v           v               v              v             v
write-design review-design revise-design implement    code-review
```

Each skill is independent -- use any subset you need.

## License

Apache 2.0
