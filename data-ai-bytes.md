# Daily Data and AI Bytes

> As a data professional, a basic yet important thing to keep reminding ourselves everyday is that we are here to solve business problems.

> The very first question to ask is whether the business problem at hand really requires an ML/AI solution?

> If the business problem really requires an ML/AI solution, define the problem further and agree on the KPIs with business stakeholders.

> So you have analyzed if the ML/AI solution would be feasible for the business problem you are working on. <br />
> You have also defined the problem further and agreed on KPIs with the business. <br />
> What's next? <br />
> Where is the data? Is it available? Is it accessible? What is the format? Any privacy or other regulatory constraints? Can you legally use it?

> Two extreme ends of ML/AI project feasibility assessment:
> 1. If there are clear and evident patterns in data, why to go for ML/AI?
> 2. If there are no patterns in data, why to go for ML/AI?
> Everything in between is a candidate for evaluation.

> You need to almost always start with PoC (proof of concept) in ML/AI use cases, why?
> - it minimizes the risk
> - it validate the feasibility quickly
> - it generates immediate insights
> - it aligns project stakeholders' expectations

> During the PoC, keep the end-to-end solution or product in mind, keep the modeling part simple initially.

> As a general rule:
> - If the patterns in data are simple and static, ML/AI may not be required.
> - If the patterns in data are complex and dynamic, ML/AI may be useful there.

> Business domain is an important aspect of ML/AI use cases, <br />
> you may need to explicitly build features around the domain to guide ML/AI models if the patterns are not evident in the data itself. <br />
> That's where domain experts are required, the step is called feature engineering.

> Every ML/AI use case has different requirements, <br />
> don't reuse the same data across different ML/AI use cases. <br />
> Validate the scope for current ML/AI use case independently. <br />

> How frequent do you need the predictions? <br />
> Real-time? Near real-time? Every hour? Every day? <br />
> How frequent do you need to train your model? <br />
> Every day? Every week? Every month? Every quarter? <br />
> This is also an important aspect, given that it can also change over time. <br />
> A lot of design, infra and monitoring aspects depends on it.

> The model you build serves the users, <br />
> document and perform all the sanity checks after exporting and before serving the model, <br />
> to make sure exported model is fit for serving.

> Keep a tab on silent decay in model performance, <br />
> track the statistics of features and response at regular intervals, <br />
> watch out for concept and data drift over time.

> Document the features and their lineage from source systems, even assign the ownership for critical features. <br />
> Today everything may be working fine... <br />
> Tomorrow, if anything goes wrong, it will help immensely in the root cause analysis.

> Business KPIs are often too many, complex, and hard-to-measure, but keep your ML/AI objective single, simple, and easy-to-measure. <br />
> Yes, we use ML/AI to improve/optimize business KPIs, but choosing business KPIs directly as ML/AI objectives can make your project too complex, or sometimes it's not even feasible. <br />
> Remember, a business problem has to be translated into ML/AI problem first. <br />
> Hence start simple, choose a single, simple and easy-to-measure ML/AI objective that directly or indirectly represents all or some of your business KPIs. <br />

> Almost always you need to start with a simple and interpretable model,<br />
> it helps in building better understanding of data and how the target has a causal relationship with features,<br />
> and it also makes debugging easier if the performance is not good enough.<br />
> Gradually you can move towards complex models...

> In a complex ML/AI use case, try to keep the concerns separate, <br />
> what I mean by that is, for example, <br />
> in search functionality, filtering the relevance and ranking the relevance are two different tasks, handle them separately, <br />
> basically, the output of filtering will be an input to ranking. <br />
> This is relatively an easier example, but the idea holds the same for all similar scenarios, <br />
> I call it 'separation of concerns' in ML/AI.

> Your work doesn't stop once you launch your model in production, in fact, you will be launching the same or similar model again and again.  <br />
> This is because you may find new useful features, you may identify tuning opportunities, you may refine your objective further.  <br />
> So keep the modeling pipeline simple and flexible enough so that it doesn't slow down your iterations, adding/removing features, creating a fresh copy of the pipeline, etc should be easy enough. 
