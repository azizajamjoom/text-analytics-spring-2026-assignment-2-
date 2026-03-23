## Step 7: Evaluation & Reflection

Out of the 20 custom examples, the model correctly classified **17 out of 20**, resulting in a custom inference accuracy of **85%**. This indicates that the model performs well not only on the test dataset but also on new, unseen examples.

The model performed **very well on the easy examples**, correctly classifying nearly all clearly positive or negative reviews. For instance, strongly worded reviews such as *“This movie was absolutely amazing”* and *“This was one of the worst films I have ever seen”* were correctly predicted. This shows that the model effectively captures clear sentiment signals.

However, the model showed weaknesses on **tricky examples involving mixed sentiment or ambiguity**. For example, in *Example 10* (“The acting was great, but the story was weak”), the model predicted a positive label despite the overall negative sentiment. Similarly, in *Example 12*, where the sentiment was uncertain and mixed, the model again predicted incorrectly. These errors occur because the model tends to focus on strong positive keywords (e.g., “great”) and struggles to weigh contrasting phrases.

The model also faced challenges with **out-of-domain examples**, such as *Example 16* involving a documentary and *Example 19* involving a podcast. While it still performed reasonably well overall, it occasionally misclassified these examples because they differ from the movie-review style of the training data. This indicates that the model is somewhat sensitive to domain shifts.

Overall, these results suggest that the model has **strong generalization ability for standard inputs**, but its performance decreases when handling nuanced language or unfamiliar contexts. It is reliable for clear sentiment classification but less robust for sarcasm, mixed sentiment, or non-movie content.

Based on this evaluation, I would **partially trust this model in production**, particularly for large-scale sentiment analysis tasks where most inputs are straightforward. However, for high-stakes applications, improvements such as more diverse training data or advanced models (e.g., transformer-based models) would be necessary to handle complex language more effectively.
