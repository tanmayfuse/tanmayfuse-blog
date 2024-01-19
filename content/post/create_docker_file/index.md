---
title: "Write docker file" # Title of the blog post.
date: 2023-12-31T18:47:44+05:30 # Date of post creation.
description: "Article description." # Description used for search engine.
featured: false # Sets if post is a featured post, making it appear on the sidebar. A featured post won't be listed on the sidebar if it's the current page
draft: false # Sets whether to render this page. Draft of true will not be rendered.
showShare: false
toc: false # Controls if a table of contents should be generated for first-level links automatically.
# menu: main
usePageBundles: false # Set to true to group assets like images in the same folder as this post.
featureImage: "/images/path/file.jpg" # Sets featured image on blog post.
featureImageAlt: 'Description of image' # Alternative text for featured image.
featureImageCap: 'This is the featured image.' # Caption (optional).
thumbnail: "/images/path/thumbnail.png" # Sets thumbnail image appearing inside card on homepage.
shareImage: "/images/path/share.png" # Designate a separate image for social media sharing.
codeMaxLines: 10 # Override global value for how many lines within a code block before auto-collapsing.
codeLineNumbers: false # Override global value for showing of line numbers within code block.
figurePositionShow: true # Override global value for showing the figure label.
showRelatedInArticle: false # Override global value for showing related posts in this series at the end of the content.
categories:
  - Technology
tags:
  - Docker
  - tools
---
Docker can build images automatically by reading the instructions from a Dockerfile. A Dockerfile is a text document that contains all the commands a user could call on the command line to assemble an image. This page describes the commands you can use in a Dockerfile.

## Overview
The dockerfile support the following instructions:
| Instruction    | Description                                               |
| -------------: | --------------------------------------------------------- |
| Add            | add local or remote files and directories.                |
| ARG            | Use build-time variables.                                 |
| CMD            | Specify default commands.                                 |
| COPY           | Copy files and directories.                               |
| ENTRYPOINT     | Specify default executable.                               |
| ENV            | Set environment variables.                                |
| EXPOSE         | Describe which ports your application is listening on.    |
| FROM           | Create a new build stage from a base image.               |
| HEATHCHECK     | Check a container's health on startup.                    |
| LABEL          | Add metadata to an image.                                 |
| MAINTAINER     | Specify the author of an image.                           |
| ONBUILD        | Specify instructions for when the image is used a build   |
| RUN            | Execute build commands.                                   |
| SHELL          | Set the default shell of an image.                        |
| STOPSIGNAL     | Specify the system call signal for exiting a container.   |
| USER           | Set user and group ID.                                    |
| VOLUME         | Create volume mounts.                                     |
| WORKDIR        | Change working directory.                                 |

## Format
Here is the formet of the Dockerfile:
```
# Comment
INSTRUCTION arguments
```
The instruction is not case-sensitive. However, convention is for them to be UPPERCASE to distinguish them from arguments more easily.

Docker runs instructions in a Dockerfile in order. A Dockerfile **must begin with a `FROM` instruction**. This may be after **parser directives, commands,** and globally scoped **ARGs**. The `FROM` instruction specifies the **parent image** from which you are building. `FROM` may only be preceded by one or more `ARG` instructions, which declare arguments that are used in `FROM` lines in the Dockerfile.

BuildKit treats lines that begin with `#` as a comment, unless the line is a valid **parser directive**. A `#` marker anywhere else in a line is treated as an argument. This allows statements like:
```
# Comment
RUN echo 'we are running some # of cool things'
```

Comment lines are removed before the Dockerfile instructions are executed. The comment in the following example is removed before the shell executed the `echo` command.

```
RUN echo hello \
# comment
world
```

The following examples in equivalent.

```
RUN echo hello \
world
```
Comments don't support line continuation characters.
