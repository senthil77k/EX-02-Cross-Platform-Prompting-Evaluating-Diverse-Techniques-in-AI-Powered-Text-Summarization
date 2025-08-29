# EX-02-Cross-Platform-Prompting-Evaluating-Diverse-Techniques-in-AI-Powered-Text-Summarization

## AIM
To evaluate and compare the effectiveness of prompting techniques (zero-shot, few-shot, chain-of-thought, role-based) across different AI platforms (e.g., ChatGPT, Gemini, Claude, Copilot) in a specific task: text summarization.

## Scenario:

### Step 1:

Summarize the following 500-word article on “The Basics of Blockchain Technology” in 120–150 words for undergraduate students. Keep it clear and beginner-friendly.


### Step 2 (Feedback):

Please revise the summary to make it even simpler and include at least two real-world examples of blockchain applications.

## Algorithm

Here is an algorithm that incorporates zero-shot, few-shot, chain-of-thought, and role-based prompting for text summarization across AI platforms. The logic helps select and adapt the optimal prompting strategy based on the platform’s strengths and task requirements.


The adaptive summarization algorithm selects prompting style based on input complexity and platform strengths, constructing tailored prompts that can be iteratively refined for best summary quality (see full algorithm in the project documentation).

***

## Adaptive Prompt Selection for Text Summarization

### Inputs
- Source text (to be summarized)
- Task requirements (conciseness, tone, technical depth, audience)
- Target AI platform (e.g., ChatGPT, Gemini, Claude, Copilot)

### Steps

1. **Analyze Task Requirements**
   - Identify summary goals (e.g., concise, technical, creative).
   - Define output preferences (length, format, tone, target audience).

2. **Select AI Platform**
   - Choose platform best suited for the task:
     - Creative/role-adapted summaries → ChatGPT
     - Factual/concise summaries → Gemini
     - Technical/methodical summaries → Claude
     - Productivity/basic summaries → Copilot

3. **Choose Prompting Technique**
   - If task is standard or general → **Zero-shot**
   - If task is specialized, nuanced, or format-sensitive → **Few-shot**
   - If task is technical, long, or needs logical structure → **Chain-of-thought**
   - If output must be tailored to a specific role or audience → **Role-based**

4. **Construct Prompt**
   - Zero-shot: Summarize the following text focusing on X.
   - Few-shot: Example: (Sample text + summary). Now summarize: (Your text) in the same manner.
   - Chain-of-thought: Walk through the main points step-by-step, explaining their significance, then summarize in Y sentences.
   - Role-based: As a [professional role], summarize the text for [audience] emphasizing [key aspect].

5. **Execute & Refine**
   - Submit chosen prompt to the target AI platform.
   - Review summary, check for goal alignment and quality.
   - Refine prompt structure or technique if results are not satisfactory.


A direct comparison of prompting techniques—**zero-shot**, **few-shot**, **chain-of-thought**, and **role-based**—for text summarization across major AI platforms reveals that each method has distinct strengths and is best suited to different summary tasks and platforms. Effectiveness varies based on the specificity, complexity, and format of the input text, as well as the platform’s underlying model and training.

## Prompting Techniques Explained

- **Zero-shot**: Fast and efficient, suitable for everyday summarization tasks when the source material is familiar to the model; strong pre-training is required for accuracy.
- **Few-shot**: Improves summary quality for specialized or nuanced texts by providing examples; best when tone, style, or format are critical.
- **Chain-of-thought**: Boosts complex reasoning and stepwise detail in summaries; often applied for technical or lengthy texts, especially when logic or sequencing is needed.
- **Role-based**: Tailors content for specific audiences or professional needs; most applicable when summaries must reflect particular priorities, such as policy or business-relevant insights.
## AI Platform Performance in Text Summarization

| Platform      | Best Use Cases                         | Prompting Strengths                       | Noted Weaknesses                          |
|---------------|---------------------------------------|-------------------------------------------|-------------------------------------------|
| **ChatGPT**   | Writing, creativity, brainstorming[4] | Few-shot, zero-shot, role-based[5]   | Less precise on highly technical tasks |
| **Claude**    | Structured planning, technical summaries[4] | Chain-of-thought, few-shot[6][4] | Sometimes verbose, less creative    |
| **Gemini**    | Factual, contextual, concise summaries[4] | Zero-shot, chain-of-thought, role-based[4][5] | Less playful, needs refinement on tone |
| **Copilot**   | Productivity, quick info engineering[7] | Zero-shot, role-based                    | Limited creative output    |

## Empirical Findings

- In comparative tests, **Gemini** consistently delivered concise, accurate summaries using zero-shot and chain-of-thought prompts for factual or contextual tasks.
- **ChatGPT** excelled in creative and engaging summary tasks, responding best to few-shot and role-based prompts for storytelling and tailored content.
- **Claude** offered the highest clarity and structural organization, particularly in methodical or step-by-step summaries leveraging chain-of-thought and few-shot strategies.
- Research indicates that in many summarization tasks, **simple zero-shot prompting can outperform few-shot and role-based** methods, especially when the platform's pre-trained knowledge aligns closely with the input material.

## Best Practices for Text Summarization Prompts

- Use **zero-shot** for standard documents, time-sensitive summaries, or when minimal customization is needed.
- Select **few-shot** for highly technical domains, inconsistent source material, or when the required summary format is nuanced.
- Apply **chain-of-thought** for long, complex texts needing logical flow or ordered key points.
- Adopt **role-based** prompting to ensure summaries resonate with a specific audience or professional context.




## Result



In summary, prompting technique effectiveness varies with the text's complexity, summary’s intended use, and platform capabilities; no universal winner exists, but matching prompt style to platform strengths yields optimal results in text summarization.
