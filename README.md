Inspired by recent Gemini API improvements from Google I/O and Google's Notebook LM, I built a tool that helps Students convert PDF educational content into animated explanatory videos with speech synthesis using Google's models.

## How It Works

Upload a PDF and the application generates an animated video that visually explains the content, helping students learn faster through multimedia presentation.

https://github.com/user-attachments/assets/76e914ab-7ca7-47af-8302-69cb6f5a7f8f

Here is the generated Video (~ 20 mintues after)

https://github.com/user-attachments/assets/efe064f8-aa6e-4c01-be10-b5a88529ae1b

Note: No Voice added yet

## Current Status and Goal
This is a proof of concept with known issues (text overlapping, animation conflicts, frame positioning). The goal is creating a Gemini-compatible library that generates educational videos in under 9 lines of code using AST(Abstract Syntax Tree) validation, caching, and abstraction layers.

```python
from google import ExplainGenerator # Or a more suitable top-level class name

# For Gemini
explainer_gemini = ExplainGenerator(
    model_name='gemini-2.5-pro-latest',
    api_key='YOUR_GEMINI_API_KEY'
)

scene_gemini = explainer_gemini.from_pdf("myfiles/OrganicChemistry.pdf", video_quality="h")

scene_gemini.generate()
```
