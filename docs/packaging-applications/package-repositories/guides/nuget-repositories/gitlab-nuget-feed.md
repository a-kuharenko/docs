---
title: GitLab NuGet repository
description: Configuring a GitLab NuGet repository as an Octopus feed.
position: 20
---
GitLab creates a NuGet Registry for each Project or Group.  To add the NuGet Registry to Octopus Deploy as an external feed, you will first need to get the Project or Group Id

Project Id

![GitLab Project Id](../images/gitlab-project-id.png)

Group Id

![GitLab Group Id](../images/gitlab-group-id.png)

## Adding a GitLab NuGet repository as an Octopus External Feed
Create a new Octopus Feed by navigating to **{{Library, External Feeds}}** and select the `NuGet Feed` Feed type. 

Give the feed a name and in the URL field, enter the HTTP/HTTPS URL of the feed for your GitLab Project or Group in the format:

Project:

`https://your.gitlab.url/api/v4/projects/[project id]/packages/nuget/index.json`

Group:

`https://your.gitlab.url/api/v4/groups/[group id]/-/packages/nuget/index.json`

Replace the URL from the examples above.

![GitLab NuGet Feed](images/gitlab-octopus-add-nuget-feed.png)

Optionally add Credentials if they are required.