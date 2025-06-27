---
layout: default
title: HBS D3 Machine Learning for Leaders 26 Oct 2022
parent: agora
---
# HBS D3 Machine Learning for Leaders 26 Oct 2022

HBS D3 Machine Learning for Leaders 26 Oct 2022

* AI versus ML (as definitions)
	* AI is a useful, informal term (no formal, precise definition in industry or academia at this time)
* ML has a precise meaning
	* technique that lets software learn behavior from sample data, rather than from pre-defined rules
* Example: rule-based programming vs ML for spam filtering
	* how do you filter bad email?
	* traditional approach:
		* rules (if email contains X + if email contains Y + if email contains Z + …)
	* ML:
		* model learns patterns from labeled example emails
		* classify by learning pattern
		* model: a mathematical representation of patterns and insights
		* model tries to classify new emails as spam or not spam
		* model is refined to reduce errors
		* the bigger (and more varied) the data set, the better the training
* How does a machine learn?
	* teachable machine at google
		* https://teachablemachine.withgoogle.com/v1/

	* exercise
		* create labeled image data from source based on pre-existing model
		* system will learn patterns and classify images
		* person face, orange, banana
	* what led to errors in model?
	* what examples would improve the model?
* ML development typically involves re-use
	* datasets
		* large data sets are expensive and time onsuming
		* often re-used
		* new datasets are created from scratch for specific use cases
	* ML models
		* could and on-device platforms offer AI products that may be used and re-used with no modification
		* DIY projects often start with pre-trained models
* From classification to generation
	* teachable machine did classification
		* given input predict 1 of 3 classes
	* some models can predict thousands of classes
		* example: given a snippet of text, predict the next workd
		* this enables generation of prose, software code, etc
	* may seem like dramatic different, capability, but underlying issues remain the same
		* training data drives performance
		* bias is an issue
		* results are often noisy
* generating text: why does it matter?
	* researchers realized that high-performance autocomplete can be used to tackle many different problems, controlled by a plain English interface
	* I saw the Red Sox play at (+ geographic knowledge)
	* 3 + 7 = (+ arithmetic)
	* GPT-3 (OpenAI, 2020) helped make this apparent
* global conversation about AI principles
	* organizations, companies, HigherEd, governments, etc.
* Google’s AI principles
	* AI should
		* be socially beneficial
		* avoid create or reinforce bias
		* built for safety
		* be accountable to people
		* privacy design
		* scientifici excellence
		* be made available for uses that accord w/ these principles
	* Google will not pursue AI projects that:
		* likely to cause harm
		* direct injury
		* surveillance violating international norms and laws
		* contravene international law and human rights
* Concrete action for accountability:
	* good documentation
	* data cards
		* dataset provenance
		* intended / suited able use cases
		* data-set make-up, distributions
	* model cards
		* model provenance
		* model usage
		* ethics-informed evaluation
* Explainability: can you explain the output of a ML system?
	* explanation for whom?
	* what do we mean by explain?
	* helps developers identity problems
	* id sources of error bias
	* empower users of ML
* Is ML a black box?
	* not inherently, but it IS complex
	* tools for developers to understand models
	* new ways to explain
	* can customize explanation to roles
	* some limitations
		* can’t always provide comprehensive explanations
		* research continues
* **Case Study on Diabetic Retinopathy (DR)**

	* fastest cause of preventable blindness
	* not always enough doctors to diagnose
		* India, for example (shortage of 127k eye doctors)
		* 45% of patients suffer vision loss before diagnosis
	* diagnosing DR is difficult
		* requires expertise
		* disagreements amongst experts
		* disagreements are resolved thru discussion
		* develop software linking data gathering and corresponding discussions
	* how do you train a model?
		* take an existing model and re-train it
		* Google started with an existing model that classified images of broccoli, fish, fire trucks etc
		* 130K images of eye scans provided and model re-trained
	* models CAN be retrained for a new task
	* incorporate privacy design principles
		* transparency
		* consent
		* access
	* health regulators have been thinking about automation for a long time
		* governance documentation by federal govt
	* avoid creating or reinforcing unfair bias?
		* what groups need to be well-represented in eye scan dataset?
		* age, sex, pupil size, image quality (in DR use case)
	* ARDA (Automated Retinal Disease Assessment) was developed
	* result to date
		* screened 5k patients
		* model performance is on par with eye speicalists
		* published 2 papers
		* did better than generalists, not quite as good as specialists
		* opened screening sites in Thailand
	* Observations
		* nurses required less specialists in remote facilities
		* wait times for referrals went from weeks to minutes
		* imagines readable by humans were often deemed too “low quality”
		* poor internet connectivity led to frustrating wait times
	* Dataset size
		* if you’re using a robust, pre-trained ML model, and re-training it for a more specific use case, the dataset used for re-training could be smaller
		* text prediction, in particular, seems to work well w/ these types of lower dataset sizes
		* more research being done on this
	* articles
		* Healthcare AI systems that put people at the center

		* https://dl.acm.org/doi/abs/10.1145/3313831.3376718

* Takeaways
	* data is critical across systems
		* wide range of systems, but for each one, training data is the driver for performance, bias, etc
	* we can explain some things, some of the time
		* very contextual, depends on specific application and systems
	* Human-AI interaction
		* evaluate beyond benchmarks, direct resources towards understanding people in the loop, societal consequences



