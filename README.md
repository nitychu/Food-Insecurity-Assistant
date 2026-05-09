# Food-Insecurity-Assistant
# AI4SG Food Insecurity Assistant
AI prototype that uses Gemini image recognition and structured extraction to recommend food for low cost meal plans. 

## Problem
People that have food insecurity in the Bay Area usually struggle to find affordable or healthy meals only using ingrediants they already have. Many people don't have clear information on nutrition or recipes because of limited budgets and ingredients. 

## AI Capability
This project uses structured data extraction and image recognition with the Gemini API. Structured extraction helps organize ingredient and nutrition information into consistent outputs, while image recognition allows users to upload food images and receive recipe and pricing recommendations automatically.

## Workflow
The user either uploads an image of ingredients or types a list of available food items. Gemini analyzes the image or text input, identifies ingredients, pulls nutritional quality, recommends recipes, and then estimates any pricing or cheaper alternatives. The generated output helps users make low-cost meal decisions more efficiently.

Screenshots of outputs and edge case testing are included in the notebook.

## Failure Case
One edge case involved uploading an image of trash instead of food ingredients. The system correctly identified the image as non-food, but still processed parts of the workflow before stopping. This demonstrated that unclear or misleading image inputs can slow down the system and reduce efficiency.

## Oversight and Tradeoff
Human review should occur whenever uploaded images are unclear or when the AI has low confidence in ingredient identification. One improvement would be adding an earlier image validation step before running the full workflow. The tradeoff is increased processing complexity and slightly slower response times, but it reduces unnecessary API usage and incorrect outputs.
