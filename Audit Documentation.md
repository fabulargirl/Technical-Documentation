Alyabeva Kristina

**For the audit, I chose the documentation of the** [csv library in python](https://docs.python.org/3/library/csv.html).
## Identify outdated sections or missing information

This documentation does not say what version of python it is for (presumably the latest version).
There is no specific versioning. For some functions there is an example of what has been changed in a particular version. 
Also for added functions, the version in which they were added is labeled.
Example:
![[Ex.png]]

It would be better to see information for individual versions of python. Some projects may be written in a particular version of python and it is easier to select a particular version when referring to the documentation.

For some functions there is an example of using them in code, it is not clear why this example is present only in selected functions. It would be good to add an example for all functions from the library. Examples from code with outputs better demonstrate the work than descriptions.

There is no information about compatibility with external libraries. It may be useful to include examples of working with popular libraries, such as pandas, to integrate with CSV files.

Also the documentation should include more detailed information on handling errors such as incorrect data in CSV, corrupted files or encoding problems.

## Propose an update schedule and assign owners

**Update Schedule**
The documentation should be updated when a new version of Python is released. This will allow you to take into account changes in library functionality and incorporate new recommendations.

**Schedule to update current missing information**

| Tack                                               | Description                                                                                                                                                   | Timing  | Owners                         | Reviewer                       |
| -------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------- | ------------------------------ | ------------------------------ |
| Updating Python version information                | Adding separate items for each python version. Adding function descriptions to each version in which they are supported and their peculiarity in each version | 1 month | Technical writer               | Developer                      |
| Adding code examples for all functions             | Add a sample code using for each function in with correct operation for each python version                                                                   | 1 month | Developer                      | QA developer                   |
| Adding information about compatibility with pandas | Add a description of how the library works in conjunction with pandas and an additional code sample.                                                          | 2 weeks | Technical writer, Developer    | Technical writer, Developer    |
| Adding an error handling section                   | Adding a section on error handling with incorrect csv files                                                                                                   | 2 weeks | QA developer, Technical writer | QA developer, Technical writer |


**Assign owners**
Technical writer and csv library developer should be responsible for analyzing changes to the library and updating the functionality-related sections of the documentation in a timely manner.
The developer will write out the use cases code examples and peculiarity of how to use the feature. And the technical writer will describe it in an understandable way for users.

## Track changes

**Versioned tags**
It is important that all changes in the documentation are linked to the tag of the corresponding Python version, so that, if necessary, you can quickly find the old version. 

All python documentation is also stored on github, so it can also be tracked via pull requests. Each PR should contain a description of the changes and links to the corresponding changes in the library.


# 3. Automate a Documentation Check

- If you use Git-based docs, set up a simple CI script (GitHub Actions, GitLab CI, or similar) to run a linter or link checker. 
- Demonstrate how the pipeline fails when a broken link is detected or if a document is missing crucial metadata (e.g., version number).

# 4. Create a Dashboard or Report

- Suggest 2–3 metrics (page views, doc coverage, document update frequency) that your team could track. 
- Sketch a mock dashboard to visualize these metrics over time. This dashboard could be a Confluence page or a simple spreadsheet.