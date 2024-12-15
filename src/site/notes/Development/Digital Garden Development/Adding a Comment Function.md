---
{"dg-publish":true,"dg-path":"Development/Digital Garden/Adding a Comment Function.md","permalink":"/development/digital-garden/adding-a-comment-function/","title":"Adding a Comment Function to the Digital Garden page","tags":["type/tutorial"],"created":"2024-12-08T09:51:17.538+01:00","updated":"2024-12-15T23:16:52.958+01:00"}
---

# Adding a Comment Function to the Digital Garden page

Selected commenting platform option: Disqus

## Step1:  Create a Disqus account

You need to first create a Disqus account and configure it for your site. 
Follow the instruction at the official Disqus website. 

[Disqus tutorial](https://disqus.com/admin/universalcode/#configuration-variables)

## Step2: Add comment.njk file to the digital garden repository

You need to then add a file called `comment.njk` in your GitHub repository. 
The file must be placed to a folder following the namespace rule. For instance, the `comment.njk` must be located at `src/site/_includes/components/user/note/footer 
See [Namespaces](https://dg-docs.ole.dev/advanced/adding-custom-components/) for the namespace rules. 

### Other references:
Reddit Post: https://www.reddit.com/r/ObsidianMD/comments/10pokli/i_built_a_digital_garden_using_obsidian_for_free/

- Reddit post: [Digital Garden using Obsidian](https://www.reddit.com/r/ObsidianMD/comments/10pokli/i_built_a_digital_garden_using_obsidian_for_free/)
- Documentation: [Adding Custom Components](https://dg-docs.ole.dev/advanced/adding-custom-components/)
- uroybd’s repository Files:
    - `note.njk`: [View on GitHub](https://github.com/uroybd/topobon/blob/main/src/site/_includes/layouts/note.njk)
    - `comment.njk`: [View on GitHub](https://github.com/uroybd/topobon/blob/main/src/site/_includes/components/user/notes/footer/001-comment.njk)


---
# Identified Issues and Solutions

## Problem1: Width of the comment section

### Issue: 
When copying the default Disqus embed code, the width of the comment section may not align properly with the webpage layout.

![Adding comment section to Digital Garden.png](/img/user/Development/Digital%20Garden%20Development/_media/Adding%20comment%20section%20to%20Digital%20Garden.png)

### Solution

Modify the first line of the Disqus embed code as follows:

```
<div class="content"><div id="disqus_thread"></div></div>
```

![Adding comment section to Digital Garden2.png](/img/user/Development/Digital%20Garden%20Development/_media/Adding%20comment%20section%20to%20Digital%20Garden2.png)


## Problem 2: Turn off reaction buttons

### Issue: 
Reaction buttons may be enabled by default in Disqus. 

### Solution:

You can turn off reaction buttons via the Disqus dashboard:
1. Navigate to the **"Reactions"** settings.
2. Disable the reaction buttons as needed.

For further details, refer to the Disqus help documentation: [Reactions Guide](https://help.disqus.com/en/articles/2199501-reactions).

