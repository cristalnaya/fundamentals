# Instructions:

1. **Repository Initialization**
* Create a new directory named agronomy-advisory.
* Navigate to this directory and initialize a new Git repository.

2. **Setting Up the Main Page**
* On the main branch, create an index.html file.
* Add a basic HTML structure: DOCTYPE, html, head, and body tags.
* Commit your changes with a message following the commit standards: feat(index.html): set up basic HTML structure.

3. **Feature Branching for Crop Tips**
* Create a branch named `crop-tips`.
* On this branch, in the index.html, add a section titled "Top Tips for Healthy Crops." Include 3-4 general agricultural tips.
* Commit your changes with a message like `feat(index.html): add top tips for healthy crops`.
* Still on the `crop-tips` branch, add a line at the end of the "Top Tips for Healthy Crops" section saying "Always water crops early in the morning."
* Commit your changes with a message like `feat(index.html): add watering tip to crop tips`.

4. **Fertilizer Recommendations and Conflict Introduction**
* Create a branch named `fertilizer-recs`.
* On this branch, in the same location where you just added the "Always water crops early in the morning" tip in the crop-tips branch, provide a conflicting tip or piece of advice, like "Avoid watering crops in the morning to prevent evaporation loss."
* Commit your changes with a message like `feat(index.html): add conflicting watering tip`.
* Continue on this branch: Add a section providing basic recommendations for fertilizer use for a specific crop like rice or maize.
* Commit your changes with a message: `feat(index.html): add fertilizer recommendations`.

5. **Styling the Content**
* Create another branch named add-styles.
* Add a styles.css file and link it in your index.html.
* Style the tips and recommendations, perhaps using a green color palette in line with agronomy.
* Commit the styling changes using: feat(styles.css): style tips and recommendations.

6. **Merging Content**
* Switch back to the main branch.
* Merge the crop-tips, fertilizer-recs, and add-styles branches into main.
* Resolve any merge conflicts if they arise.

7. **Local Weather Advisory**
* Create a new branch named weather-advisory.
* Add a section where users can input their location (a simple input box) and receive generic advice related to agronomy based on their weather (e.g., "It's rainy - Ensure proper drainage for your crops!").
* Commit your changes using: feat(index.html): add local weather advisory.

8. **Pushing to GitHub**
* Create a new repository on GitHub.
* Link your local repository to this remote one.
* Push your changes to the GitHub repository.

9. **Pulling Updates**
* Directly on GitHub, edit the index.html to add a footer mentioning Yara.
* Pull these changes to your local machine to see how Git synchronizes local and remote changes.

## Conclusion:
This exercise is not only about enhancing Git skills but also learning to manage and structure commits in a consistent and professional manner, as practiced in real-world scenarios like at Yara.
