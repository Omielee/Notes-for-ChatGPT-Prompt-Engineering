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