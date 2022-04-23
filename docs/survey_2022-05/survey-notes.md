I'm taking some notes here for the dashboard survey to run in May 2022.

I used EUSurvey to draft the survey: https://ec.europa.eu/eusurvey/

## features list

Here are the features we have, and will be developing: 

1. Break down of **file types** - Classify files into "mechanical/electrical/software/documentation" and by proportion.
2. **Issue activity level** - Graph of issue activities (open/close/comments) over time.
3. **Commits over time** - Graph of commits over time..
4. **Project skill tags/profile** - Show skill-related tags for a project, probably from the ontology.
5. **User skill tags/profile** - Show skill-related tags for a project, probably from the ontology.
6. **Manufacturing metadata** - Display what’s needed for manufacture like “Need 3D printing, PCB fabrication”.
7. **Standards compliance metadata** - REUSE, Standard README, DIN-SPEC 3105-1, OKH, OSHWA, or technology readiness levels like OTRL/ODRL.
8. **LICENSE file and meanings** - Not just which license, but also what type (i.e. CC-licenses, software licenses, or hardware licenses), what it means for the hardware and if it meets certain standards. Info on if it’s a reciprocal or non-reciprocal license.
9. **Files editability** - Are editable are the files in this repository? E.g. “PDF vs editable CAD files”.
10. **Different views for different stakeholders** - For example, there could be a project owner view that shows a different set of metrics than a visitor view; or a view meant to be embedded on a Wikifactory page.

## survey structure

* Introductory text with aims
* Demographic information
  * Drawn from the needs analysis we did last year with goal of categorising the stakeholder type of the respondent
  * "Which one [or two] of the following roles do you most strongly identify as?"
  * Max: Include open-ended "other" option
* Show mock up of each feature one at a time
  * Short description: "This feature shows you x [something neutral and descriptive]"
  * "How useful do you think it is" (Likert scale 1-5 with 5 being most useful)
  * "How would this information help you"
  * "What do you think this is useful for?" select from list of needs from 2021 needs analysis
* Drag and drop to rank the 10 features
* "Explain your reasoning/tell us why?"
* "Do you have any other comments on what you think would be useful to do x" where x is the same aims communicated at the beginning of the survey
* "If you're interested in/willing to have further feedback/reviews on the dashboard/these features, please leave your contact information"
  * At least get name and email?

### introduction to survey

* Relevant excerpts from Open!Next proposal documents
  * Task 2.2: Creating a design process facilitation dashboard
    * "grasping what success in OSD means, what factors contribute to it, and how to provide a measure of these factors based on file versioning information"
    * "infer process models"
    * "Computing of project management indicators whose relative significance on project success will be determined through quantitative and qualitative procedures."
    * "OSD project evolution paths and success indicators in an original OSD process model delivering concrete recommendations derived from actual practices."
    * "status report dashboard developed as an add-on to the existing platform Wikifactory."
    * "Validation with selected practitioners from OSD projects hosted by Wikifactory."

## dashboard elements mockups

Wikifactory UI colors are in the SVG file.