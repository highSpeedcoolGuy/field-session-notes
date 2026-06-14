Blocking with GPU/CPU
Optimize model with time

 - [ ] Conduct EDAs for more data
 - [ ] Add another target feature: Total Time
 - [ ] Do team catme review
 - [ ] Look at implementing single predictions and see if that is better (or other models that utilize joint prediction)


## Notes
> "Okay, let's look at this on a higher level right now. My models are doing very bad. -R^2 values, fitted lines don't make sense on accuracy. What major changes can I do to accomplish an atleast okay predictions. I'm also wanting to add another feature to predict: total_memory_utilized. Is it a better approach to do singular feature predictions, or are there other frameworks/architectures out there that are much more robust that can do my predictions well?"

Here's the new approach:

1.  Look at improving the XGBoost even more
2.  Other models: 
	- LightGBM is highly recommended.
	- CatBoost is also another tree-based model that requires almost zero hyperparameter tuning to get stell
3. Creating an ensemble of models