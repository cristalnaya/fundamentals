# Instructions:

1. **Repository Initialization**
* Create a new directory named `agronomy-advisory`.
* Navigate to this directory and initialize a new Git repository.

2. **Setting Up the Main Page**
* On the `master` branch, create an `index.html` file.
* Add a basic HTML structure: DOCTYPE, html, head, and body tags.
* Commit your changes with a message following the commit standards: `feat(index.html): set up basic HTML structure`.

3. **Feature Branching for Crop Tips**
* Create a branch named `crop-tips` from `master` branch.
* On this branch, in the index.html, add a section titled "Top Tips for Healthy Crops." Include 3-4 general agricultural tips.
* Commit your changes with a message like `feat(index.html): add top tips for healthy crops`.

4. **Modifying the Master Branch**
* Switch back to the `master` branch.
* In the same spot where you added the crop tips in the `crop-tips` branch, add a generic note like: "Remember to always consult with local agricultural experts."
* Commit this change with the message: `feat(index.html): add consultation reminder`.

5. **Rebasing and Resolving Conflicts**
* Switch to the `crop-tips` branch.
* Execute `git rebase master`.
* At this point, you should hit a merge conflict in `index.html` due to changes made in the same location on both branches.
* Resolve the conflict in `index.html`, keeping the content you feel is most relevant.
* Once resolved, continue the rebase process with `git rebase --continue`.

6. **Further Development and Merging**
* After resolving the rebase conflicts, feel free to make further changes or create additional branches as you see fit, following the previous steps as a template.
* When ready, merge your feature branches back into `master`.

7. **Pushing to GitHub**
* Create a new repository on GitHub.
* Link your local repository to this remote one.
* Push your changes to the GitHub repository.

8. **Pulling Updates**
* Directly on GitHub, edit the `index.html` to add a footer mentioning Yara.
* Pull these changes to your local machine to see how Git synchronizes local and remote changes.

## Conclusion:
This exercise is not only about enhancing Git skills but also learning to manage and structure commits in a consistent and professional manner, as practiced in real-world scenarios like at Yara.
