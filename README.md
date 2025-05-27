With the recent improvement to the Gemini API proposed at the Google I/O events. It made me think about making an helpful tool for Student who want to gain understand of contents at a fast rate.

The application takes in a pdf content of a material you are willing to understand and then generate animated Video [with speech] that helps the user understand the content visually [Inspired by Google's Notebook LM]

[Frontend video - which is in the same directory in mp4 format]

Here is the generated Video (~ 20 mintues after)

[Video]

For ease of use, I was thinking of making it in a Gemini surported library, and the video could be generated in less than 9 lines of code. Several abstractions makes this possible, which involved several Abstract Syntax Tree code validation, caching, etc.

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
