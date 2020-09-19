# Contributing

## Add a project by making a pull request

Please note we have a code of conduct, please follow it in all your interactions with the project.
To contribute to this project directly send in a pull request. Here are some guidelines for this:

### Forking

You should first fork a repository on GitHub. This step is needed only once.
See [complete help in GitHub](https://help.github.com/articles/fork-a-repo).

### Cloning

You should clone your fork. This step is needed only once.
Using [try](https://github.com/oscghana/docs) as example;

```
git clone git@github.com:YOUR-NAME/try.git
cd docs
git remote add upstream https://github.com/oscghana.git
git fetch upstream
```

### Branching

Create a branch per set of changes; e.g. to fix a problem or add a feature;

```
git checkout -b BRANCH-NAME
```

Your BRANCH-NAME can be anything, other than master.  The scope is your forked repository.  The branch name will be shown on pull-requests.

### Making commits

Change files, and commit.  Commit messages are kept by git, and are used later when problems are being solved.  When writing a commit message;

1. start with one line summary of the change;
2. leave a blank line after the summary;
3. explain the problem that is solved, unless the summary makes it obvious;
4. when the problem was introduced by a previous commit, mention the hash;
5. when the problem is in an issue or ticket, add "Fixes #34";
6. avoid mentioning GitHub or other pull-requests, as these are not kept in git;
7. avoid mentioning any tasks or irrelevant words ; use pull-request comments instead; and
8. make use of british english in spellings imperative mood

Make one or more commits and push the branch to your repository;

```
git push origin BRANCH-NAME
```

### Sending a pull-request

Send a pull-request for your branch.
Navigate to your repository page in GitHub, switch to the branch you made, and then press the **Pull Request** button.

When writing a pull-request message;

1. if there is only one commit, begin with the GitHub default of the commit message, otherwise write a summary of the series of commits;
2. link to any relevant pull-requests, issues, or tickets; and

A review will happen in the pull-request, and a reviewer will either;

1. merge, squash, or rebase your commits;
2. merge your commits with their own changes;
3. ask you to make changes; or
4. close and reject your pull-request giving reasons.

When they ask you for changes, you may have to change both files, commits or commit messages.

When squashing commits to different files, use interactive rebase.

```
git rebase -i master
```

After resolving any conflicts, push the changes to the same branch;

```
git push --force origin
```

Then respond on the pull-request.

### Keep your pull-request up to date

When there has been upstream commits while your pull-request was open, you should rebase your pull-request;

```
git pull --rebase upstream
```

Then push the changes to the same branch;

```
git push --force origin
```

The pull-request will be updated.

### Keep your fork up to date

When there has been upstream commits since your fork was made, you should bring these into your fork:

```
git checkout master
git pull upstream
git checkout BRANCH-NAME
```

### Review

We encourage testing before merging a pull-request.

So instead of merging directly with the "merge" button on GitHub, we may do a local merge, then test, then push.

See [GitHub help on merging a pull-request](https://help.github.com/articles/merging-a-pull-request).

The GitHub page for the pull-request will provide you the right commands to do the local merge, similar to the following.

Get the changes from that branch to a new local branch:

```
git checkout -b SOME-USER-topic1 master
git pull https://github.com/SOME-USER/doc.git topic1
```

Test! If everything is fine, merge:

```
git checkout master
git rebase SOME-USER-topic1
git push origin master

```
## Guidelines

1. The project should be an open source project. (Do well to have a well outlined contribution procedure to help others easily contribute)

2. Verify that the project yet to be added does not already exist in the project list.

    - You can easily verify from the  **[website](https://opensource.byafricans.org/)** by searching for the project name with additional filters if required.

    - Or open the **[projects.json](https://github.com/by-africans/open-source-projects/blob/master/projects.json)** and search through.

3. Ensure that you are the rightful owner/author of the project yet to be added. If you are a contributor/maintainer or any other, ensure you have been permitted to share the projet on this platform.

4. In **[projects.json](https://github.com/by-africans/open-source-projects/blob/master/projects.json)**, add a `JSON` entry of the project.

    - Your `JSON` entry should have :
        - Project name
        - URL to your Github project repository
        - Project description
        - Github Username
        - Author's country of origin (Must be African)
        - Twitter handle

    - Example of a `JSON` entry:

        ```json
        {
            "name": "made-in-africa",
            "github_url": "https://github.com/by-africans/open-source-projects",
            "description": "A list of projects by Africans",
            "github_username": "by-africans",
            "author_country": "Ghana",
            "twitter_handle": "by-africans"
        }
        ```

## Report bugs related to the website using Github's issues

We use GitHub issues to track public bugs related to byafricans.org . Report a bug by opening a new issue; it's that easy!

## List of African countries

Below is a list of African countries. Do well to make reference to the list to add up to you JSON entry.

### A

+ Algeria
+ Angola


### B
* Benin
* Botswana
* Burkina Faso
* Burundi


### C
* Cabo Verde
* Cameroon
* Central African Republic (CAR)
* Chad
* Comoros
* Congo, Democratic Republic of the
* Congo, Republic of the
* Cote d'Ivoire

### D
* Djibouti

### E
* Egypt
* Equatorial Guinea
* Eritrea
* Swaziland
* Ethiopia

### G
* Gabon
* Gambia
* Ghana
* Guinea
* Guinea-Bissau

### K
* Kenya

### L
* Lesotho
* Liberia
* Libya

### M
* Madagascar
* Malawi
* Mali
* Mauritania
* Mauritius
* Morocco
* Mozambique

### N
* Namibia
* Niger
* Nigeria

### R
* Rwanda

### S
* Sao Tome and Principe
* Senegal
* Seychelles
* Sierra Leone
* Somalia
* South Africa
* South Sudan
* Sudan

### T
* Tanzania
* Togo
* Tunisia

### U
* Uganda

### Z
* Zambia
* Zimbabwe

**NOTE**: _Pull requests are usually reviewed within 24 hours. Once your pull request is merged, you should see your project on the site a few minutes after._
