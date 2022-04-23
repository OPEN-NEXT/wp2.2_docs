# Top Wikifactory (WIF) projects

The spreadsheet `WIF top projects.ods` contains my attempt at figuring out the "top" projects on Wikifactory (a project here is defined by it's unique URL in the form of `https://wikifactory.com/+elektricworks/pikon-telescope`). This is part of the effort to (relatively) systematically come up with a list of Wikifactory projects to contact/survey for feedback about the WP2.2 dashboard in development. Here I will try to explain the methodology.

## data collection

At time of writing, a sample was collected on 2022-03-31 at approximately 14:10 UTC from the Wikifactory projects page: https://wikifactory.com/contribute/projects

The projects page has three "featured" projects on the top. Below that is a list of projects which you can sort in descending order by "Recent", "Followers", "Contributions", and "Views". I sorted the page by all four measures and copy-pasted the top 50 for each into the spreadsheet.

I then colour-coded those projects by: 

* Grey - The project appears in two of the four sort categories and the featured projects list.
* Blue - The project appears in three of the four sort categories and the featured projects list.
* Yellow - The project appears in four sort categories and the featured projects list.

## observations

There are 37 grey projects (74 grey cells), 2 blue projects (`https://wikifactory.com/+OttoDIY/otto-diy` and `http://viralresponse.io/+carola/project-carola-alpha`), and 1 yellow project (`https://wikifactory.com/+OttoDIY/otto-diy-plus`).

With two exceptions (`https://wikifactory.com/+OttoDIY/otto-turtle-drawing-robot` and `https://wikifactory.com/@prusalab/prusahive`), all the grey projects are in the top 50 "Followers" and "Views" lists. There were no projects in the "Recent" list that showed up in any other lists.

Many projects actually belong to the same user. For example, there are multiple projects belonging to `https://wikifactory.com/+OttoDIY`. So once this aspect has been de-duplicated, there should be fewer than the 37 grey projects that need to be contacted.

## projects recently active or with many contributions

None of the projects in the top 50 most recently active list show up in the other lists. The top 50 projects by number of contributions is similar. To me this suggests that - in the case of recent projects - they may simply not have had the time to accumulate followers, views, and contributions. As for projects with many contributions, maybe for some reason they just haven't been really actively recently, though I'm not sure why they don't have many followers and/or views.

To have them represented in the list of projects we reach out to, I suggest grouping the two lists ("Recent" and "Contributions") by user (e.g. `https://wikifactory.com/+uboopenfactory`) to see which users have the most projects represented. For example, `+uboopenfactory` has 19 projects in the 50 most recently active projects. This suggest `+uboopenfactory` is actively using Wikifactory and consciously organising their development across many projects. Then, for each list, identify the top two users and add them to the list of projects to contact.

## project owners to contact

Caroline suggested they are in touch with and handful of specific OSH projects using Wikifactory. This spreadsheet can add to that list by adding I think ~20 to contact. This would be good, because there will almost certainly be a funnel effect where only a small fraction will respond to the survey, and only a small number out of those would indicate any interest in talking more.

Also, keep in mind that we might want to do this twice. Once now (March/April 2022) when most dashboard components are still under development, and again later once more features are complete.

## exclusion criteria

Lorem ipsum.

License - determined by README, license file, project metadata, or a one-minute search in the repository's files. If not then it's not considered open source hardware.

## top projects from two "groups"

After the discussion with @elies30 on 2022-04-01, we decided to group the projects in the spreadsheet into two groups: 

* Top projects in the "Followers" and "Views" categories, since the two overlap so much
* Top projects in the "Contributions" category

De-duplicate projects among the two groups (which shouldn't be many since there's very little overlap), apply the exclusion criteria, and use what's left as the list of projects to contact. To be more specific, there are two grey projects (`https://wikifactory.com/+OttoDIY/otto-turtle-drawing-robot` and `https://wikifactory.com/@prusalab/prusahive`), two blue projects, and one yellow project, in the "Contributions" column, they are included as well in addition to projects in the two "groups".

Also, [one project](https://wikifactory.com/+wikifactory/mayku-challenge-template) is actually just a template for the Mayku design challenge by Wikifactory, I will exclude it.

Also ask Caroline if they can add specific projects to this list.

## so, which projects did we end up with?

There are 18 projects meeting the criteria above that have activity in the past 6 months, 27 if we include those with activity in the past 12 months (`WIF users to survey` sheet). In both cases, I excluded one project which is just a documentation template for an event run by Wikifactory (the [Mayky challenge template](https://wikifactory.com/+wikifactory/mayku-challenge-template)).