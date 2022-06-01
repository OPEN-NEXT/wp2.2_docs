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

## ethical requirements

We will need to follow the procedures described in deliverables 7.1 and 7.2 from work package 7.

### D7.1

Section 3 is about "Recruitment of participants", I think we're good on this. But can refer to the language here when writing report(s).

Section 4 is about the GDPR, also looks fine.

Section 5 is "Informed consent procedure". Again, should be OK but follow this language in report(s). **Remember to get and archive signed consent forms**.

### D7.2

Looks fine here, too.

I think the meat of what we have to do are: 

1. Incorporate the consent form into the survey.
2. Once the data is gathered, have management procedure in place. The key is carefully handling the emails that respondents might give.

I talked to Robert on 2022-05-05 about this, and he said I can model the survey consent form to be like this: 

https://forms.office.com/r/vFrtszbJDG (archived on archive.org)

And "A PDF attachement and a general information for informed consent in the web form may be totally fine".

#### consent form

Here's what I think could go into the survey to obtain consent: 

This informed consent form is for respondents to a survey operated by the research project Open!Next.

Contact person: 
Dr Pen-Yuan HSING - University of Bath, United Kingdom (email: pyh27 [at] bath.ac.uk)

Survey title: Improving Wikifactory and open source development with a project dashboard

Introduction and background: ...

Purpose of this survey: ...

Selection of respondents: We want to include stakeholders of open source hardware projects, including - but not limited to - users with activity within the past 12 months on the Wikifactory platform.

Voluntary participation: Your participation is completely voluntary. You can stop your participation at any time.

Procedure: We respectfully ask you to complete the questions in this survey to help us understand which measures could guage the status and health of an open source hardware project.

Benefits: The information collected may eventually inform improvements to platforms such as Wikifactory to improve your user experience.

Terms and confidentiality

Reimbursements: You will not be given any payment to take part in the project activities.

Confidentiality:  We will not be sharing information about you outside of the project team. The information that we collect from this project will be kept confidential. Information about you that will be collected from the research and innovation activities will be put away and no one but the  project team members will be able to see it. At the conclusion of this study, the project team members may publish their findings. Information will be presented in summary format and you will not be identified in any publications or presentations. Any published data and metadata will be archived at Zenodo.
    
Sharing of Research Findings:  We will be sharing what we have learnt with Wikifactory. We will do this by providing a written report. Nothing that you will tell us today will be shared with anybody outside the project team and Wikifactory, and nothing will be attributed to you by name. We might also publish the results in academic outlets so that other interested people may learn from our research. Data will only be included in these publications in aggregated and anonymized form.

GDPR Provisions
Collection of personal data: Your personal data will be collected following standard rule of law to which we are subject, in particular the General Data Protection Regulation (EU 2016/679)[1] (GDPR). Capture and use of personal data of contacts in OPEN.MAKE will be done in compliance with the GDPR which grants you the following rights: 

(a) The right to request access,
(b) the right to rectification, 
(c) the right to erasure, 
(d) the right to restriction of processing of personal data to consist only of storage, 
(e) the right to data portability, 
(f) the right to withdraw consent,
(g) and the right to lodge a complaint.

[1] General Data Protection Regulation – Regulation (EU) 2016/679 of the European Parliament and of the Council of 27 April 2016 on the protection of natural persons with regard to the processing of personal data and on the free movement of such data, and repealing Directive 95/46/EC. URL: http://eur-lex.europa.eu/eli/reg/2016/679/oj (last accessed on the 31.10.2019).

All personal data collected from you will be used for the research- and innovation-related purposes stated above. Your personal data will therefore be stored only until the end of the project.

Right to refuse or withdraw: You may choose to opt out and stop your participation at any time.
  
Who to Contact: If you have any questions you are free to ask them now or at any time, even after your participation. Questions you wish to ask later, may be directed to the following main contact person / project team member: Dr Pen-Yuan HSING - University of Bath, United Kingdom (email: pyh27 [at] bath.ac.uk)

Where to complain: In case of complaints, we would like to kindly ask you to first approach the above-mentioned contact persons. In any case, you of course have the right to complain to the supervisory authority: 
Berliner Beauftragte für Datenschutz und Informationsfreiheit
E-Mail: mailbox@datenschutz-berlin.de
Address: Friedrichstr. 219 / Besuchereingang über Puttkamerstr. 16 -18, 10969 Berlin.

Name: 

Certificate of Consent

I have read the foregoing information, or it has been explained to me. I have had the opportunity to ask questions about it and any questions that I have asked have been answered to my satisfaction.

I hereby give consent for my data to be conveyed and documented for the purpose stated above. I confirm that I have been informed of the nature of OPEN.MAKE and that my participation is voluntary. I am aware that I may withdraw my consent at any time.

yes/no

## survey deployment

### via Wikifactory

### at D3.5 validation day

Scheduled for the afternoon of 2022-05-27.

For details, see notes Moe circulated to Pen on 2022-05-03T16:55+01:00.