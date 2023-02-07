---
layout: post
title: Modeling Generative Processing in Neural Networks
categories: Cognitive-Science
---

The paradigm of proceduralism has addressed how perceptual features are processed in the mind for encoding and retrieval. This includes several empirical accounts in the form of generation effect, levels of processing, transfer-appropriate processing, and testing. Generative processing generates predictions based on how humans generate perceptions that are concretely associated with their prior learning. However, this does not provide a thorough explanation of the underlying mechanism. Deep learning research on generative processing has largely focused on computer vision tasks using surrounding image context to conditionally generate predictions and using the generated output to update a latent variable to improve the model. Motivated to connect these modern frameworks to cognition, we propose a framework for conditional generation for text by creating a deep language model to predict tokens based on contexts. We use a replay approach, like pseudo-rehearsal to augment the training dataset – to better capture the distribution of previously encountered data. Noise is added to the weights of the network to simulate catastrophic forgetting. Using the proposed methodology, we aim to evaluate the benefits of generative processing on one of (1) experiments from Slamecka & Graf (1972) using an in-distribution classification task-network or (2) sentiment classification from the GLUE benchmark with a parallel user study measuring task performance.

### Paper

[Modeling Generative Processing in Neural Networks to Improve Retention](https://github.com/mscandlen/mscandlen/raw/master/docs/Scandlen_Sharma_Ramachandra_Sreermdass_2022.pdf)

### Examples

### Repository
