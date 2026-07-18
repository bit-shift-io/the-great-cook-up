# Parse Recipe

Takes one or more recipe URLs and generates markdown recipe files in your repo format.

## Usage

```
/parse-recipe <url> [url2] [url3] ...
```

## Examples

Single recipe:
```
/parse-recipe https://example.com/amazing-pasta-recipe
```

Multiple recipes (batch):
```
/parse-recipe https://example.com/recipe1 https://example.com/recipe2 https://example.com/recipe3
```

Paste raw URL text directly:
```
/parse-recipe https://example.com/recipe
```

## What it does

1. Fetches recipe data from provided URL(s)
2. Extracts: title, servings, prep/cook time, ingredients, method, and notes
3. Generates markdown files named after the recipe title
4. Saves files in the repo with your standard format:
   - `# Recipe Title`
   - `Serves:` and `Time:` metadata
   - `## Ingredients` section
   - `## Method` section (numbered steps)
   - `## Notes` section (with original source URL)

## Format example

```markdown
# Apple & Celery Salad

Serves: 4
Time: 15 min prep + 60 min cook

## Ingredients

* 500g sausages
* 2 Tbl oil
* ...

## Method

1. Make dressing...
2. Make salad...

## Notes

Original: https://example.com/recipe
```

## Notes

- Files are created in the repo root directory
- Filenames are generated from recipe title (lowercase, hyphenated)
- Works with any recipe URL (AllRecipes, Food Network, etc.)
- Can process multiple URLs in a single command
