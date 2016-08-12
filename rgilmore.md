
---
AuthorName: Rick Gilmore  
Affiliation: Penn State University  
WorkflowTitle: Developing R Code for the Processing and Analysis of Optic Flow Data    WorkflowDiagramURL:
Discipline: Psychology  
Software: R  
DOI_URL:
---

##### Introduction
*Please answer these introductory questions for your case study in a few sentences.*

1) Who are you and what is your research field? Include your name, affiliation, discipline, and the background or context of your overall research that is necessary specifically to introduce your specific case study.

2) Define what the term "reproducibility" means to you generally and/or in the particular context of your case study.

Reproducibility means that the processing of a dataset can be created multiple times by many users using the same workflow/code and get the same results. It also means that as I collect more data a few commands can be run to update the results based on the increased number of data sets.

##### Workflow diagram

The core of your case study is a diagrammatic workflow sketch, which depicts your the entire pipeline of your workflow. Think of this like a circuit diagram: boxes represent steps, tools, or other disjoint components, and arrows show how outputs of particular steps feed as inputs to others. This diagram will be complemented by a textual narrative.

We recommend the site [http://draw.io](http://draw.io) for creating this diagram. Please draw your diagram so that it reads from left to right, and fills no more than half a standard US letter page. Use Helvetica font with at least 10 or 11pt size.

While creating your diagram, be sure to consider:

* specialized tools and where they enter your workflow
* the "state" of the data at each stage
* collaborators
* version control repos
* products produced at various stages (graphics, summaries, etc)
* databases
* whitepapers
* customers

Each of the two example case studies include a workflow diagram you can also use for guidance.

Please save your diagram alongside this completed case study template.

##### Workflow narrative

This study examined whether the detection of optic flow in child observers varies by pattern and speed in similar ways to adults. Data were collected utilizing Matlab and PsychToolbox to generate the stimuli displays consisting of two side-by-side, time varying annular shaped optic flow displays. One display depicted random (0% coherent) motion while the other depicted radial or translational motion at one of two coherence level profiles (20, 40, 60, 80%) or (15,30,45,60%). The participant indicated their choice of which display consisted of coherent motion by pointing to the monitor. A speed of 2 or 8 deg/s was used for a single run. Four separate output (csv) files, from 4 blocks of data, were generated for each participant. The csv file includes pattern type and coherency level of the stimuli, and reaction time and accuracy of the participant responses.

All output data files were transferred from the data collection computer manually to Databrary (for sharability) and Box (for analysis). Metadata for all participants was entered into a .csv file for all participants and also placed on Box. Once enough data was collected for analysis, R code was designed to process the data and produce plots for data analyses.

The R code was written in a few steps. The first step was to clean (remove duplicate, unnecessary, and PII) and merge all participant session output information and associated metadata into a single file making it easily indexable for further analyses (import-clean-export.R). The second step was to take this single datafile and generate aggregate plots for the reaction time and percent correct vs. coherence, pattern and speed.

It takes much longer to generate the code, but the resulting ease of generating data usable for publication much easier.


All data files are shared on Databrary (https://nyu.databrary.org/volume/218) including the output data files, video files, and participant metadata. Analysis files are shared on a GitHub repository.

A similar workflow is utilized for multiple studies in this lab including EEG and other behavioral studies. R makes it easy to create a workflow for a type of data and reproduce it as more data are collected. This makes data analyses an on going process and not something that is saved up until the end which makes writing abstracts and papers less cumbersome.





Referring to your diagram, describe your workflow for this specific project, from soup to nuts. Imagine walking a friend or a colleague through the basic steps, paying particular attention to links between steps. Don't forget to include "messy parts", loops, aborted efforts, and failures.

It may be helpful to consider the following questions, where interesting, applicable, and non-obvious from context. For each part of your workflow:

* **Frequency:** How often does the step happen and how long does it take?
* **Who:** Which members of your team participate (or not)?
* **Manual/Automated:** Is the step automated or does it involve human intervention (if so, is it recorded)?
* **Tools:** Which software or online tools are used in the step? How are they used?

In addition to detailing the steps of the workflow, you may wish to consider the following questions about the workflow as a whole:

* **Data:** Is your raw data online?
   * Is it citeable?
   * Does the license allow external researchers to publish a replication/confirmation of your published work?
* **Software:** Is the software online?
   * Is there documentation?
   * Are there tests?
   * Are there example input files alongside the code?
* **Processing:** Is your data processing workflow online?
   * Are the scripts documented?
   * Would an external researcher know what order to run them in?
   * Would they know what parameters to use?

*(500-800 words)*

##### Pain points
*Describe in detail the steps of a reproducible workflow which you consider to be particularly painful. How do you handle these? How do you avoid them? (200-400 words)*

The data transfer and updating of the participant metadata file need to be made more automated.

##### Key benefits
*Discuss one or several sections of your workflow that you feel makes your approach better than the "normal" non-reproducible workflow that others might use in your field. What does your workflow do better than the one used by your lesser-skilled colleagues and students, and why? What would you want them to learn from your example? (200-400 words)*

##### Key tools
*If applicable, provide a detailed description of a particular specialized tool that plays a key role in making your workflow reproducible, if you think that the tool might be of broader interest or relevance to a general audience. (200-400 words)*

##### General questions about reproducibility

*Please provide short answers (a few sentences each) to these general questions about reproducibility and scientific research. Rough ideas are appropriate here, as these will not be published with the case study. Please feel free to answer all or only some of these questions.*

1) Why do you think that reproducibility in your domain is important?

2) How or where did you learn the reproducible practices described in your case study? Mentors, classes, workshops, etc.

3) What do you see as the major pitfalls to doing reproducible research in your domain, and do you have any suggestions for working around these? Examples could include legal, logistical, human, or technical challenges.

4) What do you view as the major incentives for doing reproducible research?

5) Are there any broad reproducibility best practices that you'd recommend for researchers in your field?

Automate as much as possible.
Documentation, Documentation, Documentation!

6) Would you recommend any specific websites, training courses, or books for learning more about reproducibility?

