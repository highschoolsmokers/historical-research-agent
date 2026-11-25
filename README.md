# Historical Research Agent

A historical research agent for writers. Helps you investigate real people, cultures, places, and events — and organize your findings into structured reference documents.

## What It Does

- **Historical research** — Investigates periods, people, places, cultures, and events, surfacing the vivid, story-relevant details writers actually need
- **Newspaper & media lookups** — Searches digitized newspaper archives to find contemporary coverage of events in specific places and periods
- **Manuscript review** — Reads your drafts and flags anachronisms by severity, with period-accurate alternatives
- **Fact-checking** — Flags anachronisms, common misconceptions, and gaps between documented history and your narrative
- **Source confidence scoring** — Rates information reliability from primary sources (★★★★) down to popular belief (★)
- **Research organization** — Maintains structured Markdown reference files using templates

## Install

### As a Claude Code plugin

```bash
/plugin marketplace add highschoolsmokers/writer-utilities-marketplace
/plugin install historical-research-agent
```

### Manual install

```bash
claude --agent agents/historical-research.md
```

Or copy into your global agents directory:

```bash
cp agents/historical-research.md ~/.claude/agents/historical-research.md
claude --agent historical-research
```

### As a system prompt

The `agents/historical-research.md` file can be used as a system prompt with any Claude API integration.

## Templates

The `templates/` directory contains starter templates for research entries:

| Template | Use For |
|----------|---------|
| `research-index.md` | Top-level index for all research on a project |
| `person.md` | A real historical figure |
| `location.md` | A city, region, or place in a specific era |
| `culture.md` | A culture or society at a specific point in time |
| `event.md` | A historical event |
| `timeline.md` | Chronology with concurrent world events |
| `daily-life.md` | A day in the life of a specific time, place, and class |
| `language-glossary.md` | Period vocabulary, slang, idioms, and speech patterns |
| `comparison.md` | Comparing different sources/accounts of the same subject |
| `research-brief.md` | General research on a topic, with newspaper coverage |

### Using templates

Point the agent at a template when starting a new entry:

```
"I need a person entry for Frederick Douglass during his time in Rochester.
Use the person template."
```

The agent will copy the template, fill in what it can from research, and flag what needs your input.

## Example Usage

### Research a historical period

```
"I'm writing a story set in 12th-century Kyoto. Research daily life for a
low-ranking court noble — what they ate, wore, how they spent their days,
and what social pressures they faced."
```

### Look up newspaper coverage

```
"Find newspaper coverage of the 1900 Galveston hurricane — what were papers
in Houston and New Orleans reporting in the days before and after? I want
to know how the story unfolded in real time."
```

### Research a real person

```
"Research Ada Lovelace's relationship with Charles Babbage. What do we
actually know from letters and contemporary accounts vs. what's been
romanticized later?"
```

### Fact-check a draft

```
"Read my chapter set in 1920s Harlem (./drafts/chapter-3.md) and flag
anything that's anachronistic — wrong slang, objects that didn't exist
yet, events out of order, that kind of thing."
```

### Review a manuscript

```
"Review this chapter (./drafts/chapter-7.md) for historical accuracy. 
Categorize issues by severity — I need to know what's definitely wrong
vs. what's just uncertain."
```

### Research a location in a specific era

```
"What did San Francisco's Barbary Coast look like in 1875? I need the
sights, sounds, smells — what a character walking through would experience."
```

### Build a daily-life reference

```
"Create a daily-life entry for a merchant's wife in 1340s Florence.
I need to know what her day looked like hour by hour — meals, tasks,
social interactions, sensory details."
```

### Build a period language glossary

```
"Put together a language glossary for 1860s New York — especially
Five Points slang and working-class speech. I need to know what words
to use and which ones to avoid as anachronisms."
```

### Compare conflicting accounts

```
"Create a comparison entry for the death of Cleopatra — what do the
ancient sources actually say vs. the popular version? I want to know
where the accounts diverge."
```

## Tips

- **Start with your project.** Tell the agent what you're writing, the period, and what you need
- **Point it at your files.** The agent works best when it can read your existing notes, outlines, and drafts
- **Ask for newspapers.** Contemporary media coverage gives you period-accurate language and reveals how people experienced events in real time
- **Track what's real vs. invented.** The templates include sections for separating documented fact from your fictional choices
- **Use the glossary template for dialogue.** Period language is where most historical fiction breaks immersion — build a glossary before writing dialogue-heavy scenes
- **Check source confidence.** The agent rates findings from ★★★★ (primary source) to ★ (popular belief) so you know what to trust

## License

MIT. See [LICENSE](LICENSE).
