<h1 align="center">Using GitHub Packages for publishing maven package</h1>

<p align="center">
  <a href="#mega-prerequisites">Prerequisites</a> •  
  <a href="#books-resources">Resources</a>
</p>

Sample repo to demonstrate working with the GitHub Maven registry

# Publishing
- For publishing via workflow, as added [here](https://github.com/GitHubConstellation2022/packages-maven/blob/main/.github/workflows/publish-maven.yml) it is very straight forward process, check out the workflow.
- For publishing manually, you will have to modify `~/.m2/settings.xml` for authentication, follow the steps [here](https://docs.github.com/en/packages/working-with-a-github-packages-registry/working-with-the-apache-maven-registry#authenticating-to-github-packages)

# Installing
- Add the package dependencies to the dependencies element of your project pom.xml file, replacing com.packages-maven:packages-maven with your package.

```
<dependencies>
  <dependency>
    <groupId>com.packages-maven</groupId>
    <artifactId>test</artifactId>
    <version>1.0.0-SNAPSHOT</version>
  </dependency>
</dependencies>
```
- Install the package.

`$ mvn install`


## :mega: Prerequisites

- A [GitHub.com account](https://github.com/join) with a [verified e-mail address](https://docs.github.com/en/free-pro-team@latest/github/getting-started-with-github/verifying-your-email-address)
- Basic understanding of `yaml` syntax
- Basic understanding of DevOps processes
- Basic understanding of software package registries (e.g. GitHub Packages, rubygems)
- Nice to have: experience with GitHub Actions or other automation servers such as Jenkins or TravisCI

## :books: Resources

- [Introduction to YAML: Learn YAML in 5 minutes](https://www.codeproject.com/Articles/1214409/Learn-YAML-in-five-minutes)
- [GitHub Docs: GitHub Actions](https://docs.github.com/actions)
- [GitHub Docs: Workflow syntax](https://docs.github.com/actions/reference/workflow-syntax-for-github-actions)
- [GitHub Docs: REST API](https://docs.github.com/rest)
- [GitHub Docs: GraphQL API](https://docs.github.com/graphql)
- [GitHub Docs: GitHub Packages](https://docs.github.com/packages)
