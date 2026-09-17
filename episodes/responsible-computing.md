---
title: Responsible Computing Plans
teaching: 40
exercises: 35
---

::::::::::::::::::::::::::::::::::::: objectives

- Understand what a Responsible Computing Plan (RCP) is and why it is needed
- Know how to plan research projects to minimise environmental impact
- Learn how to develop a responsible computing plan for your own research
- Understand how to apply RCP principles throughout the project lifecycle

::::::::::::::::::::::::::::::::::::::::::::::::

:::::::::::::::::::::::::::::::::::::: questions

- What is a Responsible Computing Plan?
- Why are RCPs needed for research projects?
- How can I develop and use an RCP for my research?

::::::::::::::::::::::::::::::::::::::::::::::::

## What is a Responsible Computing Plan?

A Responsible Computing Plan (RCP) is a document that ensures positive environmental impacts are captured and plans the project lifecycle to achieve project goals with minimal emissions. It is a living document that reacts to changes in the project rather than being prescriptive.

### High-level RCP sections

A Responsible Computing Plan typically includes four main sections:

1. Describing the positive environmental impacts from the project
2. Planning and starting the project
3. Running the project
4. Finishing the project

## Why are RCPs useful/needed?

There is often a disconnect between use and awareness of resources used in research computing. The default position is frequently to use more resources to achieve progress rather than think carefully about the best way to achieve results. This is sometimes described as "reaching for the bigger hammer rather than the right tool."

RCPs help address this by:

- Providing the opportunity to think explicitly about the of the environmental impact of their computing choices
- Encouraging careful planning to minimise resource use
- Promoting efficient use of resources
- Ensuring environmental considerations are built into the project lifecycle

## Who are RCPs for and when should they be used?

While RCPs are framed for use in research projects but they can be used more widely as the aspects they cover are not usually specific to research projects. 

While they are most impactful if used before a project or activity starts and throughout its lifetime by the whole project team; they can be used at any point in a project or activity lifecycle and by subsets of people or even individuals to bring environmental benefits. 

## 1. Positive Environmental Impacts

The first section of your RCP should contain a **positive environmental impact statement**. This is a statement that describes the positive environmental impacts of the project – ideally quantitative but may need to be qualitative.

This statement helps justify the environmental cost of the computing resources used by highlighting the environmental benefits the project will deliver.

:::::::::::::::::::::::::::::::::::::  challenge

## Exercise 1: Positive Environmental Impact Statement

**Time: 10 minutes**

Choose a project you are (or have been) involved in, or make up a plausible project scenario.

1. Write up the project overview in 2-3 sentences
2. Produce a proposed environmental impact statement

The environmental impact statement should describe the positive environmental impacts of the project – ideally quantitative but may need to be qualitative.

:::::::::::::  solution

## Solution

Your project overview should clearly state what the project aims to achieve. Your environmental impact statement might include:

- Quantitative measures (e.g., "This project will reduce energy consumption in X process by Y%")
- Qualitative measures (e.g., "This project will enable better understanding of climate patterns")
- Direct impacts (e.g., reduced emissions from the research itself)
- Indirect impacts (e.g., enabling others to reduce their environmental footprint)

:::::::::::::::::::::::

::::::::::::::::::::::::::::::::::::::::::::::::

## 2. Planning Projects

Planning the project with environmental sustainability in mind is typically the time when you can have the **largest impact**. Planning to run the project in a responsible way almost always makes the project more impactful and robust from a non-environmental standpoint too.

### Responsible Compute Resource Use

**Reduction of consumption** is a central tenet of reducing environmental impact. Points to consider include:

- **Look for existing datasets** that you can use rather than repeating calculations
- This is not all or nothing – existing data may help you minimise your use to the most impactful use of resources
- **Ensure that all planned use will contribute meaningful data points**
- If the project involves sampling, select a sampling distribution that maximises information per point
  - For example, a regular sampling grid at finest resolution is unlikely to be the most efficient use – minimise data points in regions of little change
- When running parallel calculations – using the **smallest number of cores/nodes** that take a reasonable time is usually the most emissions efficient

### Testing Before Large-Scale Use

Test that the proposed methodologies will likely give viable results before embarking on large amounts of resource use:

- **Review literature carefully**
- **Discuss planned approach** with experienced researchers
- **Undertake pilot studies** before committing to large resource use

You often do not need to run at full scale to test if the selected method is viable – shorter runs, reduced datasets or other reductions can give confidence in the proposed resource consumption estimates.

### Selecting Appropriate Methods

Use methods proportionate to the project objectives rather than automatically choosing the most complex/advanced/higher resolution option:

- When planning a project, think carefully about the tools and methods you will use
- Some newer tools are more efficient than older ones, but not always
- Some computationally intensive approaches, including some machine learning methods, may not improve enough on simpler methods to justify their extra cost
- Think about redundancy – are you planning to compute too many datapoints or look at too many similar problems which will not provide substantial new information?
- Build smaller scale benchmarking and testing into the project plan to ensure the correct scale setup is chosen for each step (or when plans change)

:::::::::::::::::::::::::::::::::::::  challenge

## Exercise 2: Planning for Environmental Sustainability

**Time: 10 minutes**

For the same project you worked on in Exercise 1:

Write brief bullet points covering how you could, from an environmental sustainability viewpoint, plan the project to:

1. Minimise resource use
2. Build testing into the project approach
3. Select appropriate methods and scales

:::::::::::::  solution

## Solution

Your answers might include:

**Minimise resource use:**
- Search for and use existing datasets where possible
- Reduce sampling frequency in regions of little change
- Use the minimum number of compute nodes that give acceptable turnaround time
- Plan to delete intermediate files that are not needed

**Build testing into the project approach:**
- Run pilot studies with reduced datasets
- Test methodology on smaller problems before scaling up
- Schedule regular reviews to assess if resource use is justified
- Benchmark different approaches to find the most efficient

**Select appropriate methods and scales:**
- Choose simpler methods where they are sufficient for the objectives
- Avoid unnecessary high-resolution calculations
- Plan benchmarking to determine optimal resource allocation
- Consider whether machine learning approaches justify their computational cost

:::::::::::::::::::::::

::::::::::::::::::::::::::::::::::::::::::::::::

### Responsible Data Resource Use

Many projects already produce data management plans, and these typically align well with responsible resource use. The questions that would be asked are similar to those for a data management plan:

- **Do we really need to keep all intermediate files?**
- **Does each collaborator need their own copy of the dataset?**
- **Can rarely used data be compressed or moved to archival storage?**
- **Have we planned time to review and tidy data during the project?**

Additionally, build plans to publish data using a **FAIR approach** throughout the project (more on this in the "Finishing the project" section).

### Selecting Resources

Projects often have choices of HPC facility to use for different parts of the project. With environmental sustainability in mind, the choice is often a balance of **hardware efficiency**, **energy efficiency** and **carbon awareness**.

Some high level notes:

- **Use existing resources where possible** – making use of existing resources is usually the most sustainable approach
- **Shared resources are often a more sustainable choice** as they usually achieve higher utilisation over their lifetimes

When selecting an HPC facility, consider:

- **Select a facility to minimise operational emissions**
  - Use HPC facilities in locations that have the lowest emissions from electricity generation
  - This usually corresponds to them being sited in locations with lowest national grid carbon intensities
  - Can also be that they have direct connections to renewable energy sources
  - In the UK, this means HPC resources located as far North as possible
  
- **Select a facility to maximise performance if embodied emissions are a significant fraction** of the facility lifetime emissions

- **Select a facility to maximise energy efficiency if operational emissions are the dominant factor** in lifetime emissions

:::::::::::::::::::::::::::::::::::::  challenge

## Exercise 3: Data and Resource Planning

**Time: 10 minutes**

For the same project you worked on in previous exercises:

Write brief bullet points covering how you could, from an environmental sustainability viewpoint, plan the project to:

1. Use data resources responsibly (during the project – we will discuss finalising the project later)
2. Select the right (HPC) resource for the project

:::::::::::::  solution

## Solution

**Use data resources responsibly:**
- Plan which intermediate files need to be kept and which can be deleted
- Arrange for shared access to datasets rather than multiple copies
- Identify data that can be compressed or moved to archival storage
- Schedule regular data review points during the project
- Plan to follow FAIR data principles from the start

**Select the right HPC resource:**
- Choose an HPC facility in a location with low carbon intensity (e.g., northern UK)
- Consider whether existing resources can be used before requesting new allocations
- Evaluate whether shared resources would be more sustainable than dedicated resources
- Balance embodied vs operational emissions in facility selection
- Consider the energy efficiency of different hardware options

:::::::::::::::::::::::

::::::::::::::::::::::::::::::::::::::::::::::::

## 3. Running the Project

Re-planning is often needed during research projects as objectives might change, new methods may need to be employed, or new data may become available. Principles for responsible computing can be built into a research project throughout its execution.

### Run Software Carefully

**Reducing waste of resources** is key to using HPC in a sustainable way. The disconnect between using resources and visible consumption makes it easier to waste resources.

Points to consider:

- **Plan testing of software and scripts on a smaller scale** before running in ways that can consume large amounts of resource
- **Plan to run appropriate benchmarking** before committing to large usage to ensure you are using resources efficiently (cores, memory, IO, etc.)
- **Smallest number of cores/nodes is almost always the most emissions efficient** – how fast do you really need results?
- **Plan to revisit this if the project plan changes** in terms of software, method, problem size, etc.
- **Consider using carbon intensity forecasts** to schedule work at a lower-carbon time
- **Before running work, ensure you are recording enough information** to avoid rerunning this work unnecessarily

### Optimise Where it Matters

Many projects waste time optimising workflows in areas that will make a negligible impact on reducing environmental impact (or even performance) or optimise inefficiently due to lack of specialist support.

- **Find the locations where optimisation will likely have the largest impact**
- Remember, you may get a larger impact from running carefully without ever needing to get involved with programming
- **Make sure you have some plan to measure the impact of any changes** (e.g., using HPC-CI, covered in the Measurement episode)
- **Enlist the support of specialists** to analyse and optimise your workflow
- Many institutions have a local **Research Software Engineering team** who are well placed to help

## 4. Finishing the Project

In environmental sustainability terms, planning how a project will be finalised means:

- Ensuring that calculations do not need to be needlessly re-run for outcomes related to the project
- Ensuring that the right data is kept in a useful form
- Deleting data that is no longer needed
- Ensuring work can be re-used effectively in future work

For example, the following points could be considered:

- **Which data genuinely need to be retained and what can be deleted?**
- **Could publishing this data or code reduce duplicated work elsewhere?**
- **Have I left enough documentation for others to reuse what has been done?**

Finishing a project well typically corresponds to applying **FAIR principles**.

### FAIR Data Principles

The FAIR data principles provide a framework for ensuring data is:

1. **Findable** – Easy to find by both humans and computer systems and based on mandatory description of the metadata that allow the discovery of interesting datasets

2. **Accessible** – Stored for long term such that they can be easily accessed and/or downloaded with well-defined license and access conditions (Open Access when possible), whether at the level of metadata, or at the level of the actual data content

3. **Interoperable** – Ready to be combined with other datasets by humans as well as computer systems

4. **Re-usable** – Ready to be used for future research and to be processed further using computational methods

![FAIR data principles diagram](./fig/FAIR_data_principles.jpg "FAIR data principles: Findable, Accessible, Interoperable, Re-usable")

*Source: [https://www.go-fair.org/how-to-go-fair/](https://www.go-fair.org/how-to-go-fair/)*

By following FAIR principles, you ensure that:
- Your data can be found and used by others (and your future self)
- Work does not need to be duplicated
- The environmental cost of data generation is amortized over maximum reuse
- Research is more impactful and efficient overall

:::::::::::::::::::::::::::::::::::::  challenge

## Exercise 4: Finishing the Project Well

**Time: 5 minutes**

For the same project you worked on in previous exercises:

Write brief bullet points covering how you could, from an environmental sustainability viewpoint, plan to end the project in as good a way as possible.

:::::::::::::  solution

## Solution

Your answers might include:

- Review all data and identify what genuinely needs to be retained vs what can be deleted
- Publish datasets in a recognized repository with appropriate metadata (making them FAIR)
- Publish code with documentation to enable others to build on your work
- Write clear documentation explaining methods and results
- Consider writing up negative results to prevent others repeating the same unsuccessful approaches
- Ensure data is in standard, interoperable formats
- Apply appropriate licenses to enable reuse
- Archive project materials in long-term storage
- Share lessons learned about efficient resource use with the community

:::::::::::::::::::::::

::::::::::::::::::::::::::::::::::::::::::::::::

## Summary: Responsible Computing Plan

A Responsible Computing Plan with an HPC focus should cover:

### Before the project starts
- Write a positive environmental impact statement
- Plan to minimize resource consumption
- Build testing and benchmarking into the project plan
- Select appropriate methods and scales
- Plan responsible data management
- Choose HPC resources based on carbon intensity and efficiency

### During the project
- Test at small scale before large runs
- Benchmark to ensure efficient resource use
- Use the minimum resources needed
- Consider carbon intensity when scheduling
- Record enough information to avoid reruns
- Optimise where it will have the most impact
- Seek specialist support when needed

### At the end of the project
- Delete unnecessary data
- Publish data and code following FAIR principles
- Document work for future reuse
- Ensure calculations don't need to be rerun

Remember: an RCP is a **living document** that should evolve as your project develops, not a prescriptive checklist to be completed once and forgotten.

:::::::::::::::::::::::::::::::::::::: keypoints

- A Responsible Computing Plan (RCP) helps plan research projects to minimize environmental impact while achieving project goals
- RCPs are living documents that should be developed during project planning and updated throughout the project lifecycle
- Key planning considerations include: minimizing resource use, building in testing, selecting appropriate methods, and choosing sustainable HPC resources
- During project execution: test at small scale, benchmark, use minimum resources, and consider carbon intensity
- Finishing a project well involves applying FAIR data principles to enable reuse and prevent duplication
- The four main sections of an RCP are: positive environmental impacts, planning, running, and finishing the project

::::::::::::::::::::::::::::::::::::::::::::::::
