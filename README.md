# Experimenting with Multi-agent Systems in Math Problem Solving
I conducted a small experiment over this hot weekend in Sydney, driven by curiosity about the effectiveness of pairing agents with critics in solving math problems.
Experiment Setup:
I selected 100 abstract algebra questions from the widely-used evaluation dataset MMLU, available at MMLU GitHub. For this experiment, GPT-3.5-turbo was the chosen Language Model (LM) to support the agents, as I hypothesized that GPT-4 might solve the problems too easily on its own, negating the need for a critic. Additionally, the cost of invoking the GPT-4 API is substantially higher than that of GPT-3.5-turbo.
Initially, I used the OpenAI API to solve the 100 questions with a single agent, serving as a baseline for performance.
Multi-agent Approach:
Subsequently, I employed the Microsoft AutoGen multi-agent framework to create two agents: a "student" and a "critic." These agents worked collaboratively to tackle the same set of 100 questions.
Results and Observations:
The single agent scored 36 out of 100.
The team of the student and critic improved the score to 42 out of 100.
However, a detailed examination of the critic's interventions revealed mixed outcomes:
The critic correctly corrected the student's incorrect answers 6 times.
Contrarily, it misled the student from correct to incorrect answers 8 times.
The critic also identified incorrect answers by the student and proposed alternative incorrect solutions 8 times.
Interestingly, despite the seemingly counterproductive role of the critic at times, the combined student-critic team outperformed the single agent.
Cautions and Further Research:
It's crucial not to draw definitive conclusions from this minimal experiment. The dataset size of 100 questions is too small to form solid arguments. Additionally, repeating the experiment is necessary, as agents may provide different responses to the same question in multiple runs.
During my experiment, I researched "multi-agent MMLU" and discovered several recent publications. A cursory review of these works, such as the MIT paper titled "Improving Factuality and Reasoning in Language Models through Multiagent Debate" (Read Paper), revealed fascinating findings. For instance, these comprehensive studies suggest:
Increasing the number of agents in a team can potentially enhance the final score.
Allowing more extended debates among agents could lead to improved results.
Encouraging agents to exhibit more "stubbornness" in their reasoning might yield better solutions.
Conclusion: 
The small experiment was quite cost effective as a weekend entertainment, costing me less than $1.
