# Dashboard features list

This document consolidates @penyuan's notes on all the brainstormed features we've come up with for the Open!Next work package (WP) 2.2 dashboard as of August 2021. It also tries to group these features into different types of information needs that could be satisfied by the dashboard.

## relevant documents

* Brainstorming document started on 2021-07-28: https://md.opensourceecology.de/FStnpjBKToeIjneyUb8yWA?both
## list of features

* File types in a repository
  * Classify into "mech/hardware/software/doc", etc.
  * Software and hardware languages
  * How much of each in absolute and relative terms
* Types of contributions
  * E.g. documentation, CAD, or software
  * Relative share of contribution types by contributors
* Number of open/closed issues
  * Time to first response/triage of new issues
  * Time to close
  * Number of open/closed issues
  * Distribution of the age of issues
  * Is there active discussion on issues, such as: 
    * How many issues have responses
    * How frequent are responses in issue threads
  * Time series
* Number of active/inactive contributors
  * Need to define "active", perhaps show as "x contributors have been active in the past y months"
  * Proportions of active/inactive users
  * Time series
* Number of commits
  * Absolute number
  * Rate
  * Rate of change
  * But for hardware, might be harder to use use this as data because: 
    * E.g. many mechanical engineering people don't even use version control
    * E.g. there's a robot project that's highly reused with derivatives, but this is not reflected in their GitHub repository since people just don't use the GitHub features
  * Time series
* Network graphs and adjacency matrices
  * E.g. each node is a user with links representing interactions between users
  * Nodes can theoretically also be files in a project, but this might be hard for hardware files which are mostly in binary format
    * There's some work (Gopsill et al.) using the temporal proximity of file edits to infer directional dependency relationships. However, git commits mean files are often edited "simultaneously" within the same commit, so no directionality can be derived. Or can it?
  * Animated playback of how the graph changes over time
  * Suggest other projects with similar graph characteristics
* Centrality and modularity indices
  * As defined in Jeremy's paper
    * Centrality indicates the relative importance of all nodes in a graph. High index indicates the project is centered around one or few central people.
    * Clustering index indicates the degree to which nodes tend to cluster
together. An average clustering coefficient indicates contributors are clustered in subgroups of three or more people directly working on the same files. 
  * Possibly with "core/external/mutants" concept
    * Core are the main and direct contributors to the repository
    * Mutant are contributions from forks
    * External are other people submitting contributions
    * Proportions of each
* Bus factor
  * Or a measure like "x% of commits can from y users"
* Tags
  * Such as skills provided or wanted
  * Project development stage
* Badges and achievements
  * For projects and people
  * Active and Inactive badge for projects and people
  * Badges for skills that can be provided, want to learn, needed by a project, etc.
    * One scenario is to be able to answer, if someone walks into a fablab: "Is there someone here that can help me do x?"
  * Badges representing amount of work that has been put into a project or by a user
  * Ali from Sonos Motors mentioned their community members would like to get recognition for their work
    * @moedn mentioned the decentralised CV concept first proposed by Makernet Alliance's' Andrew Lamb
  * Need to come up with specific badges
  * This is related to gamification
* Interoperability with WP3 Wikibase instance and LOSH crawler
  * Will need to use JSON-LD as data interchange format
* An embedded "card" view of the dashboard
  * Similar to these software examples: 
    * https://github.com/carbon-app/carbon#license
    * https://www.openhub.net/p/cytopia
* Display what's needed to manufacture a project
  * E.g. "need 3D printer", "need ability to make PCB", etc.
  * We might be able to utilise collaborative manufacturing work done by WP3
* Compliance status with international standards and certifications
  * REUSE
  * DIN-SPEC
  * OKH
  * OSHWA
* Documentation status
  * CONTRIBUTORS file
  * GOVERNANCE file
  * README file
  * Code of conduct
  * Has WP3 documentation guidelines/templates been used?
* Manufacturing information/metadata
  * I'm guessing WIF already implements some of this as part of WP3's collaborative manufacturing tool
* Types of communications channels
* Number of downloads or its rate
* Number of forks
* Number of followers
* Number of citations?
* Measures for replicability
  * Need to flesh this out more
* Rather than pre-mining all the data, maybe make on-demand requests to the relevant APIs only when a visitor clicks on a "more info/data" button
* Who are the main maintainers?
* Project and user age
* Releases
  * Number of releases
    * Over time
* Statements derived from raw data, such as: 
  * "The last commit to this repository was 5 months ago"
  * "This project averaged 3.2 issue posts per day for the last month"
  * and second order inferences like
    * "Over the last 12 months, the commit rate to this repository (e.g. # commits per week) has gone up by x"
    * "More people have contributed to this project this month than the previous 6 months combined!"
    * "this project seem to be heavily centred on one person"
    * "there has been a steady increase in contributions over time"
    * "Individuals other than originators have modified it"
    * "if you contribute to this project, you can get x badge"
* Tooltips and pop up explanations for different aspects of the dashboard
* Way for a project/user to flag if they're actively looking for contributors/projects to contribute to
* Are files editable?
* Use of open file formats vs proprietary ones
* How often is documentation updated/maintained?
* Number of users who have built this hardware
* "Typical skills of users"
  * profile of file types edited by the user (e.g. 75% SolidWorks, 20% python and 5% markdown)

## types of needs

Of the all the features listed above, how to map them into different information needs to be satisfied by the dashboard?

* Activity level
* Community organisation
* Contributor profiles
  * Such as the skills contributors have demonstrated or want to learn/practice
* Documentation completeness
* General popularity
* New contributor friendliness
* Skills
  * Such as skills wanted or used by a project
