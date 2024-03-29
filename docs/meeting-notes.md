# Open!Next work package 2.2 (WP2.2) meeting notes

Note: Sometimes GitHub usernames are used instead of colloqiual names, e.g. @jbon instead of Jérémy.

## Minutes 2020-07-24

### Feature selection processing
- each of us four (Max, Pen, Rafaella and Jérémy) assess the relevance of each features in the "wish list" (dashboard features list) prior to next Wednesday. 
- Jérémy sends a mail in short to explain how to do this.
- UBA and WI have one voice each. That is, Rafaella's, Pen's and Jérémy's inputs will be averaged.
- each of us can freely add new features if relevant. The wish list is a "live document".
- next week we finalise the priorisation and "slice" the wish list and decide what goes in the M18 deliverable.
- Jérémy clarifies in the meantime when M18 actually is. 

### Organisation

We agreed on weekly meetings from now on, Fridays at 10 UK time. We did not discuss the length but I suggest 1.5h. Meeting frequency may be amended/reduced once we entered development, at best in combination with some other communication channel (e.g. element).

Share of responsibilities between WIF and UBA:
- WIF cares about visualisation and rendering on the WIF platform
- UBA delivers:
    - to WIF and the world an open source data processing module 
    - to the world some sort of visualisation and rendering that is hopefully looking like WIF's visualisation because we will aim to we use the same technologies as WIF

Misc:
- WIF has 7 developer and 2 manager months booked in for WP2, mostly for WP2.2
- Max in vacation after next week for two weeks

### Technologies

WIF uses the following technologies:
- [Flask](https://www.fullstackpython.com/flask.html) backend to build project features
- [postgres](https://www.postgresql.org/) and [Dgraph](https://dgraph.io/) databases (but this may not be relevant since we have the GraphQL API)
- [react](https://fr.reactjs.org/) for UI rendering
- [MobX](https://mobx.js.org/README.html) for state management 
- generally: python/javascript 

Architecture decision to take: will the data processing module happen through
- a fairly contained python module/lib
- a server?

Developing a python module/library would make more sense because:
- UBA does not have the funds to maintain a server indefinitely
- it would create a dependency for WIF
- it is more interesting for UBA to develop an open source contained module

However the decision should be discussed at WIF internally. Decision on technologies are generally pending. The wish list needs to be refined first.

## Minutes 2020-07-31

We had a look at the assessment of the feature's relevance and decided on the following:
- We implement a base of low hanging fruits for the M18 deadline. M18 is Feb 28th but due to the internal review process in OpenNext, a pre-release should be planned for Jan 31st.
- A second wave of development will be dedicated to original features. The expert system-like features seemed to be more original than the graph-like ones, but are also more risky. 

Consequently, until M18, we dedicate:
- approx. 80% of our time in the development of the M18 release
- approx. 20% refining concepts of original features, their feasibiltiy and getting a better idea of user requirements

To-do's for mext meeting:
- Based on the assesment of features relatively to relevance and developent effort, JB develops a new dashboard design mockup
- MK asks community team at WIF for a list of a few projects that represent differnt types of projects, so UBA has a few reference data to play with the GraphQL API

About software architecture:
- we go for an open source package, not for a separated server. 
- consequently, we will need interface requirements from WIF at some point. This is pending for now, the time for the M18 mockup to be agreed upon.

## Inter-WP meeting notes 2020-08-12

At 11:00 CEST with Sonika, @jbon, @moedn, and @penyuan.

For this meeting, work package (WP) 2.2 gave a summary of progress on dashboard development followed by discussions about how our respective WPs can inform each other's efforts.

* @jbon's summary of dashboard mock ups
    * We're getting lots of data from OSH projects, it is a pity not to make use of it
    * We doing this as an opportunistic technology push, i.e.:
        * In parallel to other WPs asking what practitioners want, we are creating a demonstration of what we *can* do in the form of an interactive dashboard
        * This is inspired by the Ford Motors saying "if you ask people what they want, they'll tell you they want a faster horse",  i.e. there's value is just doing things sometimes
    * @penyuan and @rafaellaantoniou have been looking at existing communities (such as [CHAOSS](https://chaoss.community/)) to see what metrics we might use    
    * Summary of ["low hanging fruit" mockup](https://github.com/OPEN-NEXT/wp2.2_dev/blob/docs/docs/mockups/low_hanging_fruits.svg)
        * This shows quantifiable metrics that we often see implemented on other platform such as GitHub
        * Already kind of useful to get a sense of which programming languages or CAD software are used by a project and the intensity of their activities
    * Mentioned achievement badges -> Which can include things like # of commits, number of contributors, etc.
    * Network visualisation ("mid-hanging fruit") mockup
        * Community graph/network of participants, which you can compute metrics like centrality or modularity of the team or the bus/elephant factor
        * Idea of core-mutant-external contributors
            * Core are the main and direct contributors to the repository
            * Mutant are contributions from forks
            * External are other people submitting contributions
        * A more advanced thing is replay button for you to watch how the network changes over time
    * Archetypes ("high-hanging fruit")
        * Define project archetypes
            * Highest activity
            * Few committers
            * etc.
            * The challenge is how do we define project archetypes and which metrics inform them?
    * We've wrapped the above into [the spreadsheet](https://github.com/OPEN-NEXT/wp2.2_dev/blob/docs/docs/mockups/Dashboard_Features.csv) to prioritise which ones we want to work on more for first month-18 deliverable in 2020-02 and what comes after
* Sonika had a couple questions:
    * Are you developing the code right now?
        * @jbon Yes, and we want something other people can take and use
    * What about programming language/tools?
        * JB: We'll try to make something suitable for WF, and since Python is almost everywhere so hopefully easier for others to adapt and adopt. Right now we're more focused on the data-mining and data analyses backend.
* @moedn:
    * I think this should connect well to results from project Open!
    * Maybe integrate into the Wikibase instance?
        * The Wikibase instance is being set up right now, will probably end up being hosted by Open Source Ecology Germany
        * We'll need what data you can provide and questions you want to answer (e.g. how active the project is, is documentation complete, which data formats are used, what software I need, Sonika: e.g. what queries you make of the data) to help be design ontology of the Wikibase instance
            * @jbon: As an example, we could give you a list of file types per repo and number of each file
    * Also talked about crawlers for a bit
        * @moedn's group might have resources to develop one, but what would it actually crawl for?
            * File type and/or license to identity an open source hardware project? Both can be challenging
        * Or have the crawler look for manifest files, which also implies that a project wants to be found
        * @jbon: Of course there's the risk at the DIN SPEC effort might fail
* Would be good to hear from Sonika too at next meeting so let's plan that, @penyuan will email everyone (let me know if I missed someone!)

## Preparation notes 2020/08/21

Agenda:
 - look at the [new mockup](mockups/M18.svg) and decide on a list of features for M18
 - review to-do-s from last meeting
 - discuss the propositions below
 - AOB

Process of selecting features for mockup M18:
  - converted relevance rankings high, medium, low into 3, 2, 1. 
  - computed relevance ranking (averaged ranking from WIF and UBA with 1:1 weighing)
  - computed an overall ranking relevance * easiness to implement
  - filtered all features ranked >= 6

Propositions to discuss:
- Involvement of WIF for M18 deliverable: implement the prototype in their platform already, so they frontload the efforts they will have to do later to implement the software developed by UoB and will have more chances to participate and give feedback.
- From now on, PYH takes over the responsibility of organizing the weekly meetings with WIF, including keeping trace of the decisions and leading the agenda and discussions.

## Meeting notes 2020/08/21

Process of agreeing on the features to be implemented for M18:
- We had a look at the [new mockup](mockups/M18.svg) resulting from the feature selection process described in the preparation notes above
- Features were discussed one by one. Some features were eventually amended and some other related features added as "nice to have"
  - For example, nice to haves include a view of how metrics change over time, graph visualisation, or metrics based on Sonika and Wikifactory's discussions outlined below in "Inter-WP meeting notes 2020-08-21T13:00+02:00" below.
- We had a veto round where each of us could remove a feature that finally seems not so relevant. We removed the component showing number of CAD files in the repository, because it is not so useful on its own, and can be incorporated into the language bar.
- We had a look at features which were on the edge of the arbitrary selection threshold. Each of us had the possibility to reintegrate these borderline features in the dashboard.

Final agreement:
- We agree on the dashboard features as described in [new mockup](mockups/M18.svg) as of commit 3b25c3c and in [the list of selected features for M18](mockups/selectedFeaturesM18.csv)
- We agree that what we deliver in M18 is a functional dashboard prototype implemented in WIF.

Remaining action items from last meeting: 
- MK asks community team at WIF for a list of a few projects that represent differnt types of projects, so UBA has a few reference data to play with the GraphQL API

## Inter-WP meeting notes 2020-08-21T13:00+02:00

With Sonika, @jbon, and @penyuan.

Today Sonika talked about their discussions with Wikifactory. They are planning to work on four main things:

* Community management - It is hard to find and attract collaborators and motivate them to contribute.
    * Develop skill based ontology in Wikibase (which will be open source) for matching contributors to projects, will be implemented by Wikifactory
    * Wikifactory can already consider a new contributor's interests in matching with tags e.g. Arduino, robotics, etc.
* Documentation and guidelines for product development
    * Will work with Grenoble people to develop good practices as part of those guidelines
    * Wikifactory has template for new projects, so maybe add documentation and development guidelines to those templates
    * With these guidelines, make projects aware of open source tools during PLM process
* Interoperability
    * It is currently hard to work with other platforms like GitLab, GitHub or Google Drive
    * So we want to develop import/export tools to aid interoperability
    * @penyuan: I suggest making these tools independent/stand-alone
* Collaborative production engineering & manufacturing
    * Develop a Manufacturer List with archetypes, capabilities, and location so that open source hardware developers can be referred to them
    * Product Metadata Information (like tolerances, material, etc.) in CAD files will be used to recommend manufacturers
* @moe is developing Wikibase ontology based on Open Know How and preparing to set up the instance
* Sonika: We came up with 15 points to work on based on most mentioned issues from user stories
* @penyuan: We are meeting with Wikifactory today, and will try to narrow down which features we want to implement for the first dashboard draft.
    * Once we have this draft, we will circulate it among Sonika and Moe for feedback.

## Dashboard meeting 2020-09-04T11:00+02:00

With Elies, @mkampik, and @penyuan

* @jbon couldn't make it today
* Update on month-18 (M18) dashboard
    * The rationales for the design are:
        * Features prioritised (a combination of user-need and technical low-hanging fruits) by @jbon, @mkampik, @rafaellaantoniou, and @penyuan
            * Spreadsheet of feature selection process can be seen [here](https://github.com/OPEN-NEXT/wp2.2_dev/tree/docs/docs/mockups)
        * They tie at least partially into needs identified from Sonika's user stories
        * They can be built as a demonstrator tied into Wikifactory project
* As for finding representative projects on Wikifactory, @mkampik suggested that we use the Wikifactory [Discover page](https://wikifactory.com/discover) to filter for projects with many contributions. In particular, [Project CAROLA](http://viralresponse.io/+carola/project-carola-alpha) is likely the most decentralised one where 12 contributors have made contributions (in contrast with centralised projects with only 1-2 contributors). The rest can come from the Wikifactory API.
* We discussed the challenges around version control when dealing with large binary files such as CAD files.
    * This is one reason Wikifactory didn't just use git
    * Instead, Wikifactory adds an abstraction around the binary files such as a tree history of file changes, but you don't pull the actual files all the time when handling the data/metadata (Wikifactory still keeps all versions of binary files)
    * There is a system called Git-LFS designed to solve the problem of version-controlling large files, but so far it seems to be mainly used for handling large data science datasets, and the barrier to adoption seems to be bandwidth costs. @mkampik found [this relevant article](https://medium.com/@megastep/github-s-large-file-storage-is-no-panacea-for-open-source-quite-the-opposite-12c0e16a9a91).
* Summary of previous meeting with Sonika, i.e. the four things they derived from user stories:
    * Community management - i.e. contributor attraction, retention, and motivation
        * It's focused on defining an open source hardware skills ontology in Wikibase to aid skill-based matching on Wikifactory
        * Both Elies and @penyuan mentioned that a contributor is often more motivated by the topic of the project rather than matching skills
    * Documentation and guidelines for new projects
        * Wikifactory will develop new templates for new projects at different stages with appropriate guides
        * The folks are Grenoble are involved since their research focus is on design re-use
    * Interoperability
        * To overcome vendor lock-in of proprietary platforms such as GitHub, Google Docs, etc.
        * Wikifactory will help implement a modular solution beginning with file import/export, and eventually issues and user mapping, and ideally sync and mirror functions
    * Collaborative production engineering & manufacturing
        * Implement in Wikibase a list of willing and able fablabs and manufacturers along with their capabilities and locations so they can be suggested to projects on e.g. Wikifactory

Next meeting(s):

* @penyuan is setting up a meeting with @moedn and Sonika to look at technical aspects of hooking dashboard up to the Wikibase instance
* Between Elies, @mkampik, @jbon, and @penyuan: 2020-09-18 at 09:00 BST/10:00 CEST
* With Elies, @jbon, and @penyuan: 2020-09-11 afternoon (@penyuan will find a time)

## Inter-WP Wikibase meeting notes 2020-09-16T14:00+01:00

With @moedn (Moe), @GoSFhg (Sonika), and @penyuan (Pen). We started with a great update on the state of the new Wikibase instance by @moedn. Some points discussed: 

* The Wikibase instance will host information on open source hardware (OSH) project, which form the "base unit" of organisation in the database.
  * In the past, they've had to manually feed information into the database, the new implementation will be much more automated.
  * The Wikibase set up as currently envisioned, can be interacted with an API to which you feed JSON-formatted data, meaning it shouldn't be too hard to hook it up to the WP2.2 dashboard.
* @moedn noted that even the [month-18 (M18) mockup](https://github.com/OPEN-NEXT/wp2.2_dev/blob/docs/docs/mockups/M18.svg) of the dashboard is valuable, and worth being part of a OSH projects' entries in the Wikibase instance.
* We also briefly looked at other versions of the mockup, such as the one with the network visualisation of user interactions. A problem @moedn discovered is that even though the visualisation (and associated analyses) might be based on publicly available information such as usernames, scraping that information might not be OK in terms of privacy and the GDPR. @GoSFhh ran into similar problems when developing the platform import/export tool.
  * @moedn kindly suggested asking Mehera about this since she's very knowledgeable on these matters.
  * A compromise solution that might work is to still collect (and anonymise) the minimum amount of data to produce the graph, but the nodes (which represent people) do not provide any information on the people behind them, i.e. you can't link a node to a username, for instance.
  * Another thing that might work is to ask for permission. Those who grant it will have their username (or equivalent) be associated with a node in the network.
  * We need to think about the above also with regards to the identify-mapping (in order to remove duplicate identities) that @jbon has worked on a lot.
* @penyuan observed that the Wikibase effort on OPEN-NEXT/OSHI (WP 3.3) and the dashboard work of OPEN-NEXT/wp2.2_dev (WP 2.2) with regards to data crawling might overlap. For example, they will both pull metadata from the GitHub API.
  * Actually, not so much. The focus on pulling version control histories, issue interactions, and possibly user activities (including data for making a network visualisation) of the dashboard won't overlap with the Wikibase crawler.
  * The dashboard's backend, which scrapes these metadata from (at least) GitHub and Wikifactory, can feed the data into the associated OSH projects' data entries in the Wikibase instance via the data loading & parsing API that is developed as a layer on top of the database.
  * The discussion on the design of this ontology is being done in [this document](https://github.com/OPEN-NEXT/OSHI/blob/master/tmp_requirements-crawler.md). **TODO:** @penyuan could provide feedback on that document in terms of where the version control and issues histories would fit in.
  * @moedn noted that it would be ideal if an end user selects a file in an OSH repository and see all the commits associated with that file, whether in the original repository or in forks, which can show/demonstrate design reuse.
* Since there are difference data sources such as, but not limited to, GitHub and Wikifactory, which represents very similar information (e.g. version control history) in different ways, @penyuan suggested the need of a data abstraction layer to which data from these platforms are translated into, *then* fed into the Wikibase instance.
  * Dealing with this could also be discussed in the documented linked to above?
* In the [month-18 (M18) mockup](https://github.com/OPEN-NEXT/wp2.2_dev/blob/docs/docs/mockups/M18.svg) of the dashboard, the lower-left section is a series of "achievement" badges for the project.
  * The badges could be split into two types: auto-generated and self-reported. The former category could be based on thresholds such as a certain number of contributors, having certaing files in the repository such as a LICENSE file. The latter could be self-reporting on things like "we've reached prototype stage". Interestingly, there could be different levels of the same badge. For example, there can be a silver DIN SPEC 3105 badge where you self-report to be spec-compliant, and a gold level one once you are official certified.
  * A lot of @GoSFhg's work on user stories and deriving the four categories of tasks might usefully inform the design of these badges.
  * [Issue #14](https://github.com/OPEN-NEXT/OSHI/issues/14) in OPEN-NEXT/OSHI is related to this.
  * **TODO:** @penyuan will draft an intial, relatively short list of possible badges and circulate to everyone for input.
* BTW, using [Plotly/Dash](https://plotly.com/) for the dashboard frontend sounded OK to everyone at this meeting (at least with no major objections!).
* Going forward, we should keep an eye on the developments in OPEN-NEXT/OSHI so that our efforts are coordinated.

## Dashboard meeting 2020-09-18T11:00+02:00

With @elies30, @mkampik, and @penyuan. @penyuan gave an update on dashboard work including a summary of the recent meeting with @moedn and @GoSFhg on 2020-09-16. This entry refers to those notes.

* @mkampik mentioned that the [RDF data model](https://en.wikipedia.org/wiki/Resource_Description_Framework) will be used in the Wikibase instance. Need to keep this in mind.
* @mkampik: Rather than keeping the dashboard's data mining code for e.g. version controls histories and issues separate, could we contribute that into the OSHI crawler?
  * @penyuan has opened an issue here: https://github.com/OPEN-NEXT/OSHI/issues/25
* We also discussed the important point @moedn made regarding mining user data to build the network graph and personal data/GDPR concerns. @elies30 noted that a compromise version where the nodes do not reveal identifiable user information, some important user-facing functionality would be lost such as identifying the important players in the project, though, of course, you can still get a sense of how a project is organised via a visual inspection of the graph. I've emailed @meherahassan about this, and will be sure to keep everyone updated on this issue.
* I deployed a tiny, back-of-the-envelope demo of using the Python Dash library to show interactive metrics from a GitHub repository using the beginner, gratis tier of PythonAnywhere (any suggestions of other/better hosting providers?): https://psaltyi.pythonanywhere.com/
* From what I've read, Dash web apps such as this can be embedded into other webpages via iframes. See these two discussions:
  * https://community.plotly.com/t/embedding-dash-into-webpage/10645/11
  * https://community.plotly.com/t/embed-dash-plot-into-web-page/5337
  * **UPDATE:** According to @moedn embedding via iframes should be just fine.
* @penyuan mentioned that we need to figure out a permanent way of hosting the dashboard once a production version is made. Though this was towards the end of the meeting and we didn't really get to discuss it.
* People seem generally receptive to brainstorming a list of badges.
  * **UPDATE:** An issue has been opened for this, please chime in: https://github.com/OPEN-NEXT/wp2.2_dev/issues/39

## dashboard meeting 2020-10-23T10:00+01

With @elies30, @jbon, @mkampik, and @penyuan, and Andres from Wikifactory.

* Not all of us were present in recent meetings, so quick recap first: 
    * Architectural diagram of how @penyuan proposed fitting the WP2.2 dashboard into WP3.3's work with Franhofer/Wikimedia on the OSH data crawler and Wikibase instance: https://picat.drycat.fr/gallery#zsta3v3z/DkP25p6J.png,CcMPnIKK/Yx6Rw35P.svg (link expires 2020-11-29)
        * @penyuan would like to keep the dashboard's frontend and backend separate, especially considering that Wikifactory will develop their own frontend.
        * Backend would be things like mining metadata via GitHub and Wikifactory's APIs and two-way communication of data with the Wikibase instance (which stores other data on each OSH project)
          * Andres can help with ensuring good API support from Wikifactory.
        * Frontend is the user-facing web-based dashboard per the month 18 (M18) mockup that is currently being implemented using the Python-based Dash library. A tiny demo is up using PythonAnywere's free of charge beginner plan: https://psaltyi.pythonanywhere.com/
            * Note that even if the frontend might look simple, it's partly because lots of work is going into the backend plumbing
            * The frontend would be purely presentation with little to no data-mining or processing (that's what the backend would do)
        * A Dash dashboard can be embedded into a Mediawiki page via iframes which @moedn says should be fine.
    * There is a GitHub issue for coming up with an initial set of badges for the M18 dashboard: https://github.com/OPEN-NEXT/wp2.2_dev/issues/39
* @moedn has just shared lots of information on the Wikibase ontology (did everyone get the announcement email? Tell @penyuan if you'd like to see it)
    * There is now a (relatively) complete draft of the whole ontology with a reserved section for the dashboard's metadata
    * An OSHI GitHub issue has been opened where discussion started with @moedn on exactly which metadata items would be needed in the ontology
        * https://github.com/OPEN-NEXT/OSHI/issues/33
    * @moedn also raised the possibility of combining our backend efforts with the OSH crawler as suggested by @mkampik last time
        * https://github.com/OPEN-NEXT/OSHI/issues/25
    * @penyuan will meet individually with @moedn possibly followed by another with Wikimedia DE engineers to work out more details
        * First meeting next Tuesday 2020-11-03 -> @mkampik will also join
* WP3.3 will have someone develop a "skills ontology" to classify the types of skills typically seen in an open source hardware project.
  * @Elies30 made the great point that we should thoughtfully design how this knowledge would be applied. For example, skill-based matching might or might not be useful unless that's truly something a prospective contributor desires. Maybe they are picking projects to work on based on topic or skills they want to learn instead of skills they already have, etc.
* @moedn previously mentioned the need to consider the GDPR
    * @penyuan has met with @meherahassan about this
        * @meherahassan's work is focused on the context of interviewing people, but neither of us sees an obvious problem
        * @meherahassan also briefly spoke to @MIE5R0 about this and again there doesn't seem to be a super-obvious concern
        * @mkampik will reach out to their legal person about this pending @penyuan providing a short blurb describing the concerns. (*update*: @penyuan sent it on 2020-11-05)
* @penyuan discovered that some data science projects hosted on GitHub uses GitHub's continuous integration (CI) service - called [GitHub Actions](https://github.com/features/actions) - to periodically scrape data and commit them into their respective repositories
    * Here is a discussion thread about this technique: https://news.ycombinator.com/item?id=24732943
    * Equivalent available on GitLab, too.
    * This doesn't look overly complicated since it (naively) looks like a "simple" matter of telling GitHub Actions to regularly run our data-mining script?
    * Are @mkampik or @jbon familiar with this? Any feedback on how easy/hard this is and its feasibility?
    * Will probably need to run the script once to get initial, large set of data (which might take a long time to run), then have GitHub Actions take care of incremental updates (hopefully this would mean the CI runs would be individually quicker???)
    * I'll discuss this with @moedn to see if this is a good idea and if it can work as part of or in conjunction with the crawler. What do you think?
    * @jbon asked a great question about storage limits for GitHub repositories -> We took a look and it shouldn't be a problem for a long time
* Question for @jbon: Was there a plan for hosting the dashboard when conceiving of Open!Next?
  * Answer: Not really. Though we might be able to host with WP3.3/Open Source Ecology.
  * @mkampik: And Wikifactory will host their own implementation of the dashboard. And who knows, maybe hosting customised instances of the dashboard can be another thing for Wikifactory to offer!
* Glad @jbon will still remain with Open!Next as an advisory board member! Looking forward to @jbon's input going forward.

## Dashboard "statements" ideation meeting 2021-07-28T12:30Z

With @moedn (Moe), @rafaellaantoniou (Rafaella), and @penyuan (Pen)

* Today's meeting is about the concept of adding "statements to the dashboard" derived from raw data, e.g. "The last commit to this repository was 5 months ago" or "This project averaged 3.2 issue posts per day for the last month"; and second order inferences like "Over the last 12 months, the commit rate to this repository (e.g. # commits per week) has gone up by x" or "More people have contributed to this project this month than the previous 6 months combined!"
* Moe kindly created a Markdown pad with our brainstorming here: https://md.opensourceecology.de/FStnpjBKToeIjneyUb8yWA?both
* @moedn : What's question we want to resolve anyway?
    * As a user, would I want to engage with the data? Design reuse?
    * E.g. for a contribution/design reuse purpose, if there's active issue discussions then that might indicate a healthier project that I can be confident in reusing
* @rafaellaantoniou:
    * I think first step is defining strategy and purpose of doing this
    * I feel like the statements should fit the goal e.g. want to help contributors decide whether to contribute, or to decide if they want to reuse
    * Suggest coming up with a few user profiles first
    * Also broader strategies
        * E.g. linking gamification with these statements
            * E.g. if you're a user of Wikifactory, you contribute to project. What if we have a system where you collected trophies for doing things, e.g. contribute to a project that has been inactive for three months
                *  And for the project, the "statement" on the project goes from "inactive in 3 months" to "active" which might be an incentive for projects to say active
                *  @moedn: Kind of like Stackoverflow's hot questions
            *  E.g. if a goal is to learn skill
                *  Filter project for "if you contribute to this project, you can get x badge"
* Acknowledge that we're now more focused on serving an audience rather than just a general research question
* Let's start with coming up with **user profiles**, the first first two below don't need commits/contributions data
    * **Design reuse** -> "I want to develop my hardware, see if someone has solved this or a partial solution that I can reuse or get inspiration from, in the best case I can just replicate"
    * **Replication** -> Just to buy or make a copy when you might not have the actual engineering skills
    * **Help people find projects to contribute to**
        * E.g. once people find some projects, the dashboard's info for each one help you evaluate your choices
    * **Help people get recognition**
        * E.g. gamification and badges, which can be tied to the other profiles above
* @moedn: There's a decentralised digital CV conceived by Makernet Alliance, by Andrew Lamb
    * Who was inspired by someone who walks into a fablab and asks "I'm looking for someone who knows x"
    * @rafaellaantoniou:We can expand on this decentralised CV concept
        * @penyuan: Erik's skills ontology certainly comes into play here
* @rafaellaantoniou: As a term, "project health" is more accurate than "community health" and is more specific, @penyuan agrees
* What we do should make distinction between dead project, done/mature, or inactive, or active
* @moedn: On the topic of commits
    * Mostly applicable to software
    * But for hardware, might be harder to use use this as data because: 
        * E.g. many mechanical engineering people don't even use version control
        * E.g. there's a robot prokect that's highly reused with derivatives, but this is not reflected in their GitHub repository since people just don't use the GitHub features
    * @penyuan: What if we focus on just a small list of projects that do lots of best practices?
        * @moedn: Actually, don't need to do that because even without that there's already lots of useful data that the dashboard can try to detect, like: 
            * SPDX license information
            * Contributor guide(s)
            * maintainers
            * communication channels
            * @rafaellaantoniou: # of downloads
            * @rafaellaantoniou: how of often it is accessed
            * @rafaellaantoniou: documentation completeness
            * @rafaellaantoniou: measures for replicability
* @moedn: Analogy for buying a car -> you don't know what questions to ask even if you have lots of data about the car
    * E.g. dashboard could have tooltips or explanations for each indicator on the dashboard
    * @penyuan: Great point, we should definitely include explanations for each indicator on the dashboard
* There should be some way for a project to flag they're looking for people
    * Or to tag an issue

We need some concrete ideas, so we used the Markdown pad @moedn created for brainstorming: 

https://md.opensourceecology.de/FStnpjBKToeIjneyUb8yWA?both

We'll need to have more deeper discussion within WP2.2 on all this, and don't forget the gamification side of things.

## Dashboard prioritisation meeting 2021-09-01T11:15Z

With @GoSFhg (Sonika), @moedn (Moe), Erik, @Elies30 (Elies), and @penyuan (Pen). Today's meeting is a follow up from the one on 2021-07-28 with @moedn @rafaellaantoniou (Rafaella), and @penyuan.

* @penyuan gave summary of the previous meeting, plus another where @Elies30 suggested summarising what we've learned into a spreadsheet that is valuable as a higher-level look at how to prioritise what to develop for the WP2.2 dashboard. There are two tables in the document, one that relates stakeholders to information needs, and another that links a long list of specific, possible features in the dashboard to those information needs.
    * @Elies30: The tables in the spreadsheet look comprehensive.
        * At some point we should decide prioritisation and write specification for what we'll do.
        * Knowing things like gamification or matchmaking are happening, what's missing in this sheet?
        * Start a process to prioritise what can help with the four tools.
        * Get @GoSFhg's feedback on stakeholder types to be better integrated with her work.
        * Also, with @moedn's track record, get his eyes on the features and indicators and statements perhaps some evaluation on difficulty of each.
        * As for Erik, hopefully can see how this is consistent with what you're doing.
* @penyuan showed everyone what the table looks like right now.
    * Feedback: 
        * @moedn: Different dashboard presentation modes for the stakeholders
            * E.g. manufacture and read-only replicator are similar -> they share very similar info needs and could be merged into one stakeholder?
            * What's the use case of the board for owners and direct contributors -> they would know repo pretty well anyway i.e. they're info providers rather than consumer
                * @penyuan: Yes, but they also have info needs such as monitoring how well the community is doing
            * Regarding market researcher -> Suggest expanding to researchers in general
        * @GoSFhg: 
            * We also had discussion about stakeholders in WP3
            * Since each stakeholder type can wear multiple hats
            * We had "project owner" -> turned to "project core team" who have different roles and responsibilities
            * Like direct vs indirect developers
            * We had "community member" -> but looks like this is covered in other stakeholders
            * I like this to establish common definitions -> consider standardising this in Open!Next! Especially WP6 including a page on the website about stakeholders and terminology.
* Going over information needs (info needs) list: 
    * @moedn: Info needs list looks good.
        * My intuition is to merge "skills" with "contributor profiles"
    * @GoSFhg: 
        * Looks good. And makes sense in terms of her knowledge of interviews and user stories. E.g. collaborative manufacturing makes sense with this list of stakeholders and info needs.
    * Erik: 
        * As you may recall, I introduced skills ontology with it's skills actions and entities.
            * E.g. operating a 3D printer, machine tools, 
            * Rather than specific "skills" which is more user-side
            * It's actually kind hard to define since it's topic-specific e.g. what do you mean when you say "this project needs CAD design" i.e. high level "skills" might change depending on context
            * @penyuan: So, in other words, sometimes a "skill" is actually a context-dependent bundle of fine-grained skills/attributes that are defined in the ontology.
* @moedn: If we can fulfill the needs of "project owners", "direct contributor", and "researchers" then looks like we can cover other stakeholders, too.
    * Important to consider things stakeholders can't get right now through existing platforms.
* Went through feature list
    * @moedn: 
        * Looks useful, but some look hard to implement
        * To prioritise, I suggest working from statements, come up with more then decide on feature that feed into the statements
        * Badges idea: Other than legal part, people want to know about documentation and maturity of project -> self-assessed badge for tech level which @moedn is working on (e.g. has been successfully independently replicated) and documentation readiness.
    * Erik: 
        * Think about motivation of contributors
        * Business models
    * @GoSFhg: I was thinking we have seven information needs. What about selecting top 3 or 4 to focus on.
    * Erik: 
        * Dashboard could help with matchmaking because I'm developing ontology, but WIF implements it, so dashboard could show -> Ask WIF about this next week, rather than prioritising it now.
    * @penyuan: What about prioritising needs as activity level, documentation, and newcomer friendliness, the last of which might be helpful for WIF (ask them next week)
        * @GoSFhg: Newcomer friendliness makes sense which also works with Eriks work
* @Elies30 is back after having to step out for a while
    * @penyuan recapped meeting so far
      * We didn't get to gamification
          * It's a lense with which to look at data
      * Plan to get Max et al.'s WIF input on this at next Tuesday's meeting instead of giving them a full proposal
* @Elies30: Feedback from anyone?
    * @GoSFhg: Great if we can agree on a standardised set of definitions for Open!Next
    * @Elies30: What features WIF chooses will be specific to them, but of course we have a bigger view today for a generic dashboard which is also important
    * Erik: Sounds good, looking forward to it. Open source landscape is messy, and great to get some guidance in the form of dashboard.
    * @Elies30: Material produced today is comprehensive and useful for a concise/short report in the end of the project.
* @penyuan: **Can you explain how you made your top picks in the last step?**
    * @GoSFhg: My perspective is benefit to stakeholders rather than particular role. Looking for which feature set would give most info. Choose factors that are important and cover the most things. Show if a project is alive and it's working well with others.
    * Erik: I was more on the perspective of a user, someone who is looking to contribute or replicate. If so, what info would I need to evaluate the project? This includes the editability of files.
    * @moedn: Those items are what I look for when scanning repos, or new information that's valuable like file types which is essential for me which also includes editability (but with work on my own I can figure out from file types). "I" means "replicator" or "indirect developer" in table.
      * @moedn also opened an issue [here](https://github.com/OPEN-NEXT/wp2.2_docs/issues/1) that summarises his thoughts/suggestions. Thank you @moedn!
* @Elies30: Open!Next is focused on SMEs who might to engage in OSH develop in their businesses
    * They're like the "project owner" stakeholder in the table, so just remember to keep this in mind.
    * @Elies30: What about approaching a real project owner like Stykka?
        * @GoSFhg: They're very time limited, could even approach all of them for feedback. But it has to be a 30-minutes or less task.
        * @Elies30: Another way of course if for WIF's input to represent a lot of project owners.
* @Elies30: Does anything from today mesh well with Moe's work?
    * @moedn: I'm working on metadata standard and search engine.

Main points from the meeting: 

* WP2.2 will meet next Monday (2021-09-06) to discuss this in preparation for the meeting with WIF the following afternoon.
    * **TODO** Ask WIF whether they think the dashboard can specifically help with their implementation of the skills ontology and skills-based matchmaking. Because at today's meeting, we've focused on the "Activity level", "Documentation", and "Newcomer friendliness" information needs for now instead of "Contributor profiles".
    * @penyuan asked the others what they based their prioritisation on above.
* Since the dashboard is defining some terms for stakeholders and information needs, consider putting the rest of Open!Next in the loop (especially WP6) so we use the same terminology.
* Suggested changes to the spreadsheet: 
    * Merge "Manufacturer" and "Replicator" stakeholders.
    * Expand "Market researcher" to "Researcher"(s) in general.
    * The current "Skills" information need can likely be merged into "Contributor profile".
* Some things to keep in mind: 
    * Great to fit what WIF is working on while ensuring the dashboard remains a generic tool that has wider value beyond WIF (such as integration with the WP3 Wikibase instance).
    * Be mindful of what features are already present in WIF and GitHub.
    * WIF is a good representative of the many SME projects hosted on their platform.

## dashboard meeting 2021-10-05T14:30+01:00

With @elies30 (Elies), @rafaellaantoniou (Rafaella), and @penyuan (Pen)

* We had brief catch-up about the Open!Next book meeting earlier today
* @penyuan plans to take leave 2021-11-01 to 2021-11-05
  * Our regular WP2.2 meeting that week has been rescheduled to 2021-11-09T15:30Z
* **Wikibase work with @moedn (Moe)**
  * @penyuan is in continuing conversation with @moedn about embedding the dashboard into the upcoming Wikibase instance
  * We need to communicate with Wikimedia Germany (WMDE) who not only provides the underlying Wikibase technology, but also development work on the instance's user-facing frontend, since they're part of who needs to make the commitment for the dashboard to be part of it
  * We talked about the Venn diagram between WMDE, Open Source Ecology Germany, the Open Hardware Observatory, and the Fraunhofer Institute as they relate to WP3 and the Wikibase instance
  * @moedn is busy working through 2021-10-15 on D3.3 which is the first demonstrator deliverable for the Wikibase instance, and @penyuan will be a reviewer for this deliverable
    * This is great, since it will give us a good understanding of which parts there are in the Wikibase deliverable, who's responsible for what, how things fit together, plus better idea of their timeline
  * After that *there is a scheduled meeting with @moedn on 2021-10-18 to come up with dashboard requirements specification for the purposes of the Wikibase instance*.
  * **TODO** *@penyuan will reach out to @GoSFhg (Sonika) and @moedn to secure commitment (including agreement from WMDE) for the dashboard integration this month*.
* **Wikifactory (WIF) planning**
  * **TODO** *@penyuan will soon circulate an email to find a time for the first dashboard technical meeting with Wikifactory (WIF)*
    * @elies30 and @rafaellaantoniou are invited since this first meeting should be pretty high-level
    * Some items to discuss at the first meeting: 
      * Timeline (see below for details)
      * Best way for them to collaborate and stay in sync
* **Project timeline**
  * @penyuan drafted a rough timeline for the rest of our project here: https://md.opensourceecology.de/SD7DrNOcTGuOscPBqSHAbg?both#
  * This timeline is a bit tight, but is this way for an important reason: 
    * The WP3 validation period (i.e. for deliverables like the import/export tool, collaborative manufacturing, WIF's Cad Rooms, etc.) is February-March 2022
    * It would be ideal if the dashboard can "piggyback" on the validation, which would also serve as a mutual commitment between WIF and WP2.2 on implementing and deploying the dashboard
    * The development work will serve both WIF and the Wikibase instance, where the latter will lead to the more generic dashboard for the final WP2.2 deliverable in month 36
  * **TODO** *@penyuan will confirm with @GoSFhg the following things*: 
    * Exact dates for the validation, since every second matters for development, and so we can plan accordingly
    * Better understand the validation methodology so that we at WP2.2 can do additional research/get feedback as necessary for our purposes
* **Planning for report(s) and paper(s)**
  * @elies30 reminded that it's a good idea to start writing things up now while still fresh in minds
  * For a paper, potential tiles from specific/obscure to more general, e.g.: 
    * "Defining key stakeholders in open source projects and capturing their requirements for a dashboard displaying metrics for their repositories"
    * "Defining different stakeholders and their information needs when searching for open source hardware projects"
    * "Identifying different types of stakeholders in open source hardware projects and their information needs"
  * For the Open!Next report, we will obviously describe who worked together, and how, to come up with the big spreadsheet of stakeholders and informatin needs
  * We recognised the somewhat ad-hoc nature of coming up with the spreadsheet in that it was compiled from meetings, notes, and partically from @GoSFhg's user stories, which is in contrast with a more formal "scientific" approach
  * @elies30: What we could do is review past literature on doing this, which presumably uses some formal methods, then compare that against the Open!Next story of how our diverse range of backgrounds and experience was the resource from which we captured these stakeholders and information needs
    * Need to think about the audience for this paper, perhaps one that isn't too focused on the scientific methods employed
    * Perhaps at least find a conference in 2022 at which to present this
* **Bath Impact Acceleration fund**
  * @rafaellaantoniou gave an update on possibly applying for this money (GBP 1000) to help promote the open source hardware work at Bath