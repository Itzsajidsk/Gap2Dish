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
