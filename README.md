# Gap2Dish

It is an Intelligent Recipe Navigator
An end-to-end Flask web app that suggests recipes based on available ingredients using graph-inspired greedy ranking plus backtracking search, with ingredient gap analysis and substitution recommendations.

Quickstart (Windows)
Create and activate a virtual environment
python -m venv .venv
.venv\\Scripts\\activate
Install dependencies
pip install -r requirements.txt
Run the app
python app.py
Open the UI
Visit http://localhost:5000
Features
Ingredient-based suggestions with substitution support
Greedy pre-ranking + backtracking plan search
Gap analysis highlighting missing ingredients and alternatives
Responsive, modern UI (HTML/CSS/JS)
Project Structure
app.py
flavorgraph/
  engine.py
  __init__.py
templates/
  index.html
static/
  styles.css
  app.js
data/
  recipes.json
  substitutions.json
  ingredient_tags.json
requirements.txt
README.md
Data Format
Recipes in data/recipes.json follow this shape:

{
  "id": "unique_id",
  "title": "Name",
  "ingredients": ["ingredient", "ingredient2"],
  "instructions": ["Step 1", "Step 2"],
  "tags": ["tag1", "tag2"]
}
Notes
Substitutions map ingredient → alternatives in data/substitutions.json.
Ingredient tags are optional metadata for future enhancements.
License
MIT


Gap2Dish — a data-driven flavour pairing and recipe discovery platform that models the relationships between ingredients, recipes and sensory attributes to help home cooks, recipe developers and food-tech teams discover better, more creative combinations.

How it works 
1)Data collection
Gather recipes and ingredient info from cookbooks, websites or your dataset.
2)Build the flavor graph
Create nodes for ingredients (and optionally recipes or taste attributes).
Add edges between nodes when ingredients appear together in recipes; weight edges by how often or how strongly they co-occur
3)Generate recommendations
For a given ingredient or recipe, find nearby nodes in the graph, rank them by score, and return top pairings or substitutions.
Apply filters (dietary limits, cuisine, availability) to keep suggestions practical.

Tech highlights
Python — backend (Flask app; see app.py and requirements.txt)
HTML — frontend templates or static pages
CSS — styling for the web UI
JavaScript — client-side interactivity or API calls
JSON — API request/response payloads
Markdown — docs/README
