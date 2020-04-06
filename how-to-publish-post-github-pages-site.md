# How to publish a post on Github Pages

1. On GitHub, navigate to your site's repository.

2. Navigate to the publishing source for your site.

3. Navigate to the `_posts` directory.

4. Create a new file called `YYYY-MM-DD-NAME-OF-POST.md`, replacing `YYYY-MM-DD` with the date of your post and `NAME-OF-POST` with the name of your post.

5. Add the following YAML frontmatter to the top of the file, replacing `POST TITLE` with the post's title, `YYYY-MM-DD hh:mm:ss +0100` with the date and time for the post, and CATEGORY with the category you want for your post.

    ```md
    ---
    layout: post
    title: "POST TITLE"
    date: YYYY-MM-DD hh:mm:ss +0100
    category: CATEGORY
    ---
    ```

6. Below the frontmatter, add content for your post.
  a. **Images**: Insert images (`my-image-1.png`) into your article by using the standard *markdown syntax* and by placing them into the `assets/images/...` folder.
  `![alt text](/assets/images/PROJECT-NAME/ARTICLE/my-image-1.png "Example alt text")`
  b. **Interactive graphs**: You can include interactive graphs (`interactive-graph.html`) too by placing them to the `_includes/plots/...` folder and using the *Liquid syntax* to include them into your article body.
  `{% include plots/PROJECT-NAME/ARTICLE/interactive-graph.html %}`
  *To keep things in order it is strongly advised to create a sub-folder for every project, and within that, other folders for each different article. The same folder structure should be applied for images and interactive graphs*.

7. Choose a meaningful commit message for your new article. If your current branch is `master`, you should choose to **create a new branch** for your commit and then **create a pull request**.

8. When your pull request is accepted, the branch containing the new article can be merged to the master branch and your article will be published.
