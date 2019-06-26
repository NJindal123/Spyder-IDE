---
Title: Marking Rubric - Project
Authors: Neil Ernst, Omar Elazhary
---

# Running Total (this will change each milestone):   

NB: for all milestones, clarity, legibility, and other good technical writing characteristics are vital and marks will be deducted if not followed.

# Milestone 1    7 / 10

## Marking Guide	
### Stakeholders and Goals 2 /5
- completeness and relevance of stakeholders
- table is well formatted and easily legible
- properly thought out business goals, referenced from empirical data (videos, blogs, project docs, tech pubs, etc.)
- at least 5 well developed business goals.

Marks deducted:
- lack of evidence for business goals 
- lack of evidence of effort in creating stakeholder table.

### Ethics report 5/5
- proper formatting and references supporting conclusions
- evidence of critical assessment of possible ethical dilemmas
- demonstrated understanding of ACM Ethical Code and how it applies to this project. 

## Notes
- the stakeholder table is pretty empty. It doesn't explain who any of these people are. If I haven't read the website, then I wouldn't know who Carlos Cordoba was. 
- some stakeholder groups are more interesting than others. For example, you should explain who the "users" are. Are there more important users than others? 
- suppliers should only be included to the extent they care about the architecture. I suspect the Debian maintainers of apt don't care too much about Spyder. It isn't big enough to influence them.
- references should point to specific sections or elements. E.g., what in "CONTRIBUTING.md" is important to the ethical report? 
- for business goals, you should refine the goals into something concrete. The bullet points you added is evidence for some higher business goal. For example, "Release Spyder 4 with new features" -> implies needing funding. The third goal is not really a project goal. Think about why the Spyder product exists, and what its purpose is. I think the second goal comes closest to what we should see in business goals.
- The ethical report was well done. I think a few other questions include "who is directing the project - the funders?" and how to ensure Spyder does not violate IDE privacy (e.g. by uploading your code to a server).
- I do think they are reasonably clear about how to contribute, not to use 3rd party code without asking, etc. 
- Good job identifying a lack of a code of conduct
-----

# Milestone 2   6 / 10

## Marking Guide	
- extensive list of ASRs, bullet form fine. Derived from business goals. (3)
- 7 scenarios in short form (3)
- 3 templated scenarios (of the 7), following the template in the notes (nb: not the full template) (2)
- Utility tree with (H,H) format for prioritization (prioritization should be reasonable but not necessarily referenced) (2)

Marks deducted:
- scenarios seem to have little to no connection with the project
- scenarios seem to have little connection to the previous milestone (business goals)
- poor technical writing 
- Quality of scenarios (clear analysis of stimulus, response, response measure)


## Notes M2
(explaining why marks were deducted)
- a few ASRs were fairly functional in nature, and it was hard to see why they would be architecturally significant. E.g., 6,8,12 are fairly obvious to support, and I don't see this changing the project's design (unlike, say, #5)
- maintainability is not really about support for old versions. It refers to the need to make the codebase itself easy to maintain, e.g. by reducing the number of dependencies, having good comments, managing libraries. 
- the purpose of the utility tree is to find the QAS that will change how we design or re-design the software. So for example, adding a checksum to the downloaded software is pretty routine and easy to support regardless of the design. This likely does not need to be called out. 
- overall, I would say there is a misplaced focus on the tool (Spyder) itself, and not the design of that tool. What about the performance goal? How does Spyder handle different languages, or plugins? These seem more likely to change the design. 
- Response measures should make the measure clear (instead of Time, give specifics--the runtime error can be identified within 30s)
-----

# Milestone 3   19 / 20

## Marking Guide	
- all required sections are present and well-organized. Include a table of contents. (2)
- view's primary presentation (diagram) is thorough and understandable. This means key elements are labeled, relations are typed, color is used appropriately. Use of UML or other diagram notations is not mandatory. (5)
- view and element catalog answers key analysis questions implied by QAS (M2). (5)
- behavior diagram is appropriate and clearly answers important questions from the QAS. (5)
- rationale is well-reasoned and any obvious assumptions are documented. (3)

Potential deductions:
- diagram missing key details and hard to understand in isolation
- no connection to project QA and previous milestones
- disconnect between Github code and your understanding.
- poor technical writing 

## Notes M3
(explaining why marks were deducted)
-1 I think the diagram could be a bit simpler, e.g. with one arrow pointing to the nested package. 
-1 You likely don't need to include Qt libraries - this could be in the context diagram.
-1 the sequence diagrams for behavior are pretty complex but don't seem to capture all the interactions. For instance, where does the autosave actually write to disk? Can you explain the interactions a bit more? 

+2 The interface section is fine, but a bit confused. E.g. the QA description does not make a lot of sense to me. Semantics do not mean "how it works" but rather, what changes in the 'world' after we use the interface.
-----

# Milestone 4    17 / 20

## Marking Guide	
- all required sections are present and well-organized. Include a table of contents. (/2)
- view’s primary presentation (diagram) is thorough and understandable. This means key elements are labeled, relations are typed, color is used appropriately. Use of UML or other diagram notations is not mandatory. (/5)
- view and element catalog answers key analysis questions implied by QAS (M2). (/5)
- behavior diagram is appropriate and clearly answers important questions from the QAS. (/5)
- rationale is well-reasoned and any obvious assumptions are documented. (/3)

Potential deductions:

- diagram missing key details and hard to understand in isolation
- no connection to project QA and previous milestones
- disconnect between Github code and your understanding.
- poor technical writing 
- no evidence of reflection and response to comments in M3

## Notes M4
(explaining why marks were deducted)
- you just leap into the view, with no connection with the QAS -1
- interface syntax should be more than just the code snippet. For example, what type is run_cell? how do I pass it in? `connect(self.run_cell)` -2
- the context diagram is good.
- the Rationale section does not need to critique the design. 
- PP was great, nice work.

# Milestone 5  16 / 15  

## Marking Guide
- Analytics: you ran tools and identified problems or positive parts of the codebase
- Evidence of tool use. 
- Report meets tech writing criteria. 
- Connection of analysis to other aspects of the project, if any.
- Technical debt is plausible and not merely the simplest rule violation.
- 2% project bonus for using SonarQube and pointing me to a Sonarqube instance

## Notes M5

+2 for SQ/Codescene
- the codescene analysis is a bit shallow. How did its hotspots relate to what you thought were problems? 
- in general, assume that I know what TD, the various rules etc are about. Write the specific implications for that part of the codebase. 
- JQuery: JQuery is a library. Why should IPython care about the library quality? -1
- the last few sections do a great job explaining and linking the various analyses.
-----

# Milestone 6. 3 /5

## Marking Guide
- **5** marks for presentation, **5** for Gitbook formatted PR with final chapter material
- Presentation organization adequate
- Presentation competently run
- Presentation on time.
- Presentation: questions answered, evidence of in depth knowledge
- Presentation: slides attractive and clear
- Presentation: speaking style clear and evidence of rehearsal

- Report compiles to PDF/Gitbook with no bugs
- Report has all necessary sections.
- Report has fixed comments from previous submissions.
- Report meets tech writing criteria. 
- Report has introduction and organization is consistent

## Notes M6
- the images are not appearing in your final submission
- 
- - @ Anna: Reading off the slides loses you your audience.
- No need to list the whole utility tree. Just include the two scenarios you’re planning on demo-ing.
- Both scenarios on the same slides makes it hard to read.
- The primary presentation (module view) is way too large on a slide. I get you want to show everything you did, but we can’t - read the contents.
- The same applies to your context diagram.
- Too much text on your slides (code quality and technical debt).
- Screenshot was nice
- Module view indecipherable
- Good detail view
- Technical: struggled to answer "where does list of options come from ZeroMQ"

-----

# Milestone 7. 18/20

## Marking Guide
- pull request is interesting and demonstrates knowledge of project architecture. 
- PR meets project standards; e.g., not a lot of changes needed by maintainer.
- marks off for triviality or simplicity

## Notes M7
- nice work! the Spyder team seems happy with your help. My only quibble would be the lack of tests for the feature. 