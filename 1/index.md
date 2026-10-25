---
title: "The First Interactive Narrative Challenge (INCH 1)"
description: "The first Interactive Narrative Challenge (INCH) was an international research competition and showcase that evaluated storytelling algorithms in 2027."
---

The Interactive Narrative Challenge (INCH) is an international research
competition and showcase of interactive storytelling algorithms. The first INCH
was announced at the
[2026 AAAI AIIDE conference](https://sites.google.com/view/aiide2026/home), and
the results will be announced at at the 2027 AAAI AIIDE conference.

# Dates

- [Intent to Participate](https://forms.gle/NhgM6j6QjwB7BPuP7) Deadline: 30 July
  2027
- Submission Deadline: 8 October 2027
- WINCH Workshop: November 2027
- Results Announced: November 2027

# Requirements

- Participants must submit a [Tandem Tales](https://sgware.github.io/tt) agent
  that can play as the game master in *The Crown* story world.
- Agents should be submitted as [Docker Images](https://docker.com) in `tar`
  format.
- Agent image files will be made publically available via for future users.
  Participants are encouraged, but not required, to make their agents open
	source.
- An agent Docker image cannot be larger than 10 GB in `tar` format.
- Agents will be allotted 16 GB of memory when running.
- Agents will run on a 64 bit Intel Xeon Silver 4110 CPU which runs at 2.10 GHz.
- Agents will run firewalled and cannot access external resources or APIs,
  except for the approved external API.
- INCH organizers will provide each agent with an external API key at run time
  via an environment variable through Docker. Agents should not include API keys
	in their source code or image files.
- Agents may access the
  [`qwen/qwen3-embedding-8b`](https://openrouter.ai/qwen/qwen3-embedding-8b)
	text embedding model via the [OpenRouter API](https://openrouter.ai). An agent
	may not exceed 1 million text embedding input tokens in a single story
	session.
- Agents may access the
  [`deepseek/deepseek-v4-flash-0731`](https://openrouter.ai/deepseek/deepseek-v4-flash-0731)
	text completion model via the [OpenRouter API](https://openrouter.ai). An
	agent may not exceed 1 million text completion input tokens or 1 million text
	completion output tokens in a single story session.
- An agent will be disconnected without completing its session if it takes more
  than 3 minutes to make a choice.
- An agent will be disconnected without completing its session if it passes
  control to its partner 3 times without taking any other actions.

# Resources

- The official definition of [*The Crown* story world](resources/crown.json) is
  the Tandem Tales story world JSON file. The official code to run a Tandem
	Tales story world is part of the
	[Tandem Tales Server](https://github.com/sgware/tt-server).
- A detailed [narrative description](resources/the-crown.pdf) of *The Crown* is
  provided for human readers.
- [PDDL](https://en.wikipedia.org/wiki/Planning_Domain_Definition_Language)
  definitions of *The Crown* are available in
	[PDDL 1.2](resources/the-crown-pddl-1-2.zip) and
	[PDDL 2.1](resources/the-crown-pddl-2-1.zip).
- [TandemTalesEnv](https://github.com/Mira2778/tandemtales_gym) lets you model
  *The Crown* as a [Gymnasium](https://gymnasium.farama.org/) environment.
- This [story graph for *The Crown*](resources/crown7.zip) includes all states
  which can be reached via 7 or fewer actions from the initial state and from
	which it is possible to reach an ending (or terminal state). The format of the
	story graph is [documented here](https://github.com/sgware/story-graph).
- [100 example games of *The Crown*](resources/the-crown-training.zip) played by
  human players and human game masters are provided as examples and training
	data.
- Example Tandem Tales agents that make random choices are provided in
  [C++](https://github.com/gsbirch/tt-random-agent-cpp),
	[Java](https://github.com/sgware/tt-random-agent-java), and
	[Python](https://github.com/sgware/tt-random-agent-python).

# Metrics

Agents are judged according to many criteria, some calculated automatically and
some evaluated by human judges. INCH gives many awards to celebrate many kinds
of success and intentionally has no *Best in Show* award to avoid over-focusing
the research community on specific metrics.

# Participants

This list of participants will be updated as teams register their
[intent to participate](https://forms.gle/NhgM6j6QjwB7BPuP7). The competition
organizers reserve the right to limit the number of submissions per organization
and to accept only agents with unique and clearly defined strategies.

| Team Name       | Affiliation | Brief Description |
| ---             | ---         | --- |
| Random Baseline | n/a         | Makes random choices. |
| LLM Baseline    | n/a         | Describes the history, current state, and available choices to a Large Language Model which chooses the next action. |

# WINCH Workshop

The first Workshop for the Interactive Narrative Challenge (WINCH) will be held
at the 2027 AAAI AIIDE workshop in 2027.

# Results

The results for all agents will be announced at the 2027 AAAI AIIDE conference.
Many awards for many kinds of success will be given.

The records of each story session used to calculate metrics and judged by human
judges will be provided for anyone wanting to do their own analysis.