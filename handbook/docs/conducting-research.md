---
title: ""
---

As a computational researcher, it is easy to fill your days implementing many small ideas of how you could improve a given analysis. Without intentional and strategic planning, it's very difficult to ensure that months-to-years of this type of effort results in a coherent, high-impact paper.

## 1. Choose a topic that people care about

If you were able to answer your research question, solve your engineering challenge, or predict something, would it matter? Who would be excited about it? Get external feedback - do other people really care about it, and think that it's an important problem to solve? If people aren't very exicited about it even assuming complete success, you should probably pivot.

Once you've identified an important problem, do some literature searches. Are other people working on this problem or question, or on something similar? If yes, this isn't a bad thing - it's further evidence that this is a worthwhile research topic that is probably tractable with currently available data and tools. If the space is too crowded it can be difficult to differentiate yourself, so there is a balance here.

## 2. Know how to evaluate success

In research, 90% of ideas fail. Many computational researchers may feel that the conventional way of performing an analysis is deeply flawed, and that some alternative might be better. However, without a clear and quantitative metric of what "better" means, it will be difficult (or impossible) to evaluate whether the idea is a good one. If you have plans for how you will evaluate your hypothesis/performance, get feedback from others. Is your proposed metric biased in some way? Does it miss some important aspect of your problem?

You should also have some idea of what level of performance is good enough to effectively solve your problem, or what level of improvement will be exciting to others.

## 3. Critically assess the available data

Even if you have a great research question or machine learning task and a plan of how to measure success, you will still fail if the available data is not of an appropriate size and quality. You won't know exactly how much data you'll need before starting, but you can usually guess the order of magnitude based on the computational methods that you plan on using. For example, if you only have 100 samples worth of data, training a deep learning network from scratch is not going to work.

Your set of computational options is usually tied to your data size and quality, especially the state of the metadata. Keep this in mind when learning about new technology that allows scientists to measure new types of data or existing types but at greater scale - maybe the new technology enables investigations that you'd previouly dropped due to lack of data.

Also think creatively about how existing sources of data can be used for new things. Is there a large set of images or text that could be processed with deep learning to turn them into something structured and ML-ready? Usually we think about a project originating from a research question. However, sometimes a project starts by identifying a new source of data that no one is paying attention to and asking "what types of novel analyses are possible with data of this scale"? Being the first person to analyse a new source of data is the easiest way to boost the novelty of what you're doing.

## 4. Stay organised

Keep your code organised and reproducible in a GitHub repository, from day one. You are strongly encouraged to use a NextFlow pipeline. While there's a bit of overhead to learn, it makes it easy to try out different pipelines in an organised way. If you are trying out many different ideas, keep track of what you did, when you did it, why you did it, and whether it improved things according to your metrics, or if you learned something concrete about your research topic. Use sensible file and directory names, and add more documentation than you think is neccessary - future you will be grateful!

The best way to ensure that your code is organised and understandable is to collaborate with others. If you share your code, you will be embarrassed if its awful. Your collaborators will also give you feedback if something is confusing. See the [GitHub Guidelines](https://ewaldlab.org/handbook/site/git-repo/) page for more technical recommendations on how to structure your analysis.

## 5. Write early and regularly

Many new researchers think that research falls into two separate steps: 1) do the analysis, and 2) write up the results. This is nearly always false. When you write down the motivation for your work, the main objective, what you did, and what the results are, you often realise that you haven't asked the most important question or convincingly proved your main point, and that your analysis is only halfway done. Reviewing literature for the introduction or discussion may give you brilliant new ideas, or you may find that your idea isn't as novel as you thought. In all of these cases, it's better to find out as early as possible, when you still have the time and energy to backtrack, expand, or pivot your plans.

When you summarise and communicate your progress to someone else, you are forced to re-examine how your latest days/weeks of effort relate to your original objectives. Writing regularly helps avoid feature/objective-creep, and keeps you focused on the most important things. Write a proposal before you start working, work on an outline as soon as you start generating results, and keep track of literature that could go in your introduction/discussion. Accept any opportunity to present your work to others - making a set of slides isn't the same as writing a paper draft, but it helps to organise your overall ideas.

## 6. Wrap things up

There are always more ways to incrementally improve some aspect of your analysis. Sometimes, implementing more ideas will degrade the quality of your paper because there will be too many results to coherently pull together into a paper that others will enjoy reading. Once you've evaluated your main ideas and explored a few additional things that came up along the way, it is usually in your best interest to narrow your scope and finish the paper.

Often computational researchers procrastinate writing their first draft because they enjoy coding more than writing, and the thought of using a point-and-click reference manager and word processor makes them shudder. Stop it! Start writing the first complete draft! It's going to take longer than you think, and you're going to feel very good when you're done.

## Final thoughts

The more rigorous and critical you are during steps 1-4, the easier the writing process will be. It's really fun to write a paper on an important topic when you have clear, quantitative metrics that show success and an organised codebase that can reproduce all of your results with minimal effort. Trying to write a paper based on a disorganized set of scripts that produce 1000 figures and tables but do not correspond to a clear research objective is excrutiating.

For these reasons, Ewald Lab members are expected to write very short research proposals (~1 page) on steps 1-3 and discuss them with the lab (and ideally others) BEFORE they start analysing any data. This will turn into the outline for your paper, which will turn into your first draft.

It's also very easy to get lost down rabbit holes and obsess over small details that really don't matter very much to the big picture. Stacking multiple small improvements on top of each other can collectively make a significant improvement (see the AlphaFold papers), but this takes laser-sharp focus, discipline, and organisation. Clearly stating your task/objective, having quantitative metrics, and regularly commmunicating your progress to keep yourself accountable is essential to ensure that your many ideas build towards an impactful end product.
