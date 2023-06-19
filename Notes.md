# Lesson 1 - Introduction
## Two types of large language models (LLMs)
- Base LLM: predicts next word
  - Eg. today is **a sunny day.** The bold words are the prediction.
- Instruction tuned LLM: tries to follow instructions
  - RLHF: Reinforcement learning with human feedback
  - Eg. What is the capital of France? **The capital is Paris.** The bold words are following the instructions.

---
# Lesson 2 - Guidelines for Prompting
## Two principles of prompting
- Write clear and specific instructions
  ### Tactics
  1. Use delimiters to clearly indicate distinct parts of the input, like: ```, """, < >, <tag> </tag>
    - avoid prompt injections
  2. Ask for a structured output
  3. Ask the model to check whether conditions are satisfied
  4. "Few-shot" prompting 少量训练提示
    - Give successful examples of completing tasks, then ask model to perform the task
- Give the model time to “think”
  ### Tactics
  1. Specify the steps required to complete a task
  2. Instruct the model to work out its own solution before rushing to a conclusion

## Model Limitations
Hallucinations 幻觉 = make statements that sounds real but are not true


---
# Lesson 3 - Iterative Prompt Development 
**Idea-Implementation(code/data)/Prompt-Experiment result-Error Analysis** REPEAT

## Exercise
### Exercise 1:Generate a marketing product description from a product fact sheet
```
fact_sheet_chair = """
OVERVIEW
- Part of a beautiful family of mid-century inspired office furniture, 
including filing cabinets, desks, bookcases, meeting tables, and more.
- Several options of shell color and base finishes.
- Available with plastic back and front upholstery (SWC-100) 
or full upholstery (SWC-110) in 10 fabric and 6 leather options.
- Base finish options are: stainless steel, matte black, 
gloss white, or chrome.
- Chair is available with or without armrests.
- Suitable for home or business settings.
- Qualified for contract use.

CONSTRUCTION
- 5-wheel plastic coated aluminum base.
- Pneumatic chair adjust for easy raise/lower action.

DIMENSIONS
- WIDTH 53 CM | 20.87”
- DEPTH 51 CM | 20.08”
- HEIGHT 80 CM | 31.50”
- SEAT HEIGHT 44 CM | 17.32”
- SEAT DEPTH 41 CM | 16.14”

OPTIONS
- Soft or hard-floor caster options.
- Two choices of seat foam densities: 
 medium (1.8 lb/ft3) or high (2.8 lb/ft3)
- Armless or 8 position PU armrests 

MATERIALS
SHELL BASE GLIDER
- Cast Aluminum with modified nylon PA6/PA66 coating.
- Shell thickness: 10 mm.
SEAT
- HD36 foam

COUNTRY OF ORIGIN
- Italy
"""
```

