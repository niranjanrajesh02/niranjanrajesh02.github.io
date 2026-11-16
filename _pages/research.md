---
layout: page
title: research
permalink: /research/
description: Research interests and publications of Niranjan Rajesh — deep networks, biological vision and computational neuroscience at UC San Diego.
nav: true
nav_order: 2
---

## Research interests

I study how intelligent systems, both brains and machines, make sense of the visual world. How do patterns of light falling on the retina, or arrays of pixel values, give rise to structured representations of objects and scenes that a visual system can use to guide intelligent behavior? I currently pursue this question in three ways:

#### 1. Leveraging model–brain comparisons to gain mechanistic insight

Convolutional neural networks (CNNs), whose layered design was inspired by the visual cortex, are now among the best predictors of neural responses in the primate visual system <span class="cite">([Yamins et al., 2014](#ref-yamins2014))</span>. But predicting the brain is not the same as explaining it <span class="cite">([Cao & Yamins, 2021](#ref-cao2021))</span>. Most comparisons pit networks against each other that differ in many ways at once, so it is hard to say which design choice is responsible for a good match <span class="cite">([Conwell et al., 2024](#ref-conwell2024))</span>.

My approach is more controlled: change one architectural factor at a time, hold everything else as constant as possible, and measure how much each change improves a network's match to neural and behavioral data. The factors I study each embody a different hypothesis about the visual system, such as equivariance, recurrence, divisive normalization, and pooling. I look at how the gains vary across brain regions (V1, V4, IT) and across training, and whether the factors add up or interact. The goal is to move from asking which model best predicts the brain to asking which mechanisms account for that prediction.

<p class="read-more"><i class="fas fa-file-pdf"></i> For more on this project, see my <a href="{{ '/assets/pdf/Niranjan_Rajesh_2YP_Prospectus.pdf' | relative_url }}" target="_blank" rel="noopener noreferrer">second-year project prospectus</a>.</p>

#### 2. Designing encoding models of visual cortex activity from EEG data

I build image-encoding models <span class="cite">([Naselaris et al., 2011](#ref-naselaris2011))</span> that predict human EEG responses from the images a person is viewing. The aim is less about prediction itself than about using these models to ask what kind of information is represented in the brain data: which image features, and which combinations of them, are enough to reconstruct the signal? EEG records activity with millisecond resolution, so it lets us ask not just where but when visual information is computed <span class="cite">([Cichy et al., 2016](#ref-cichy2016))</span>. A particular focus is the canonical event-related potential (ERP) components, which are well-known signatures of visual processing, and the computations they reflect.

A promising next step is to study the encoding models themselves. Tools to synthesize images that maximally drive a model's predicted response <span class="cite">([Bashivan et al., 2019](#ref-bashivan2019))</span>, together with causal interventions on the model's features, can turn a predictive model into a source of testable hypotheses about what the brain is computing.

#### 3. Characterizing the nature of representational spaces

Deep networks embed images in high-dimensional representations, but how much of this capacity actually drives their behavior? There is reason to suspect that it is not much. Deep networks are vastly overparameterized in their weights, and sparse subnetworks within them can match the performance of the full network <span class="cite">([Frankle & Carbin, 2019](#ref-frankle2019))</span>. They are also far less data efficient than humans <span class="cite">([Lake et al., 2017](#ref-lake2017))</span> and can be fooled by perturbations to their inputs that are imperceptible to us <span class="cite">([Szegedy et al., 2014](#ref-szegedy2014))</span>. The visual system, on the other hand, learns from relatively few examples and is remarkably robust. Perhaps some of these differences are reflected in how the two use their representational capacity. If so, characterizing the redundancy in a network's representational space, and how it differs from the brain's, could help us understand how visual representations in the brain work and, in turn, help us build more brain-like vision systems.

In recent work, we introduced a framework for identifying the subspace of a network's representation that is functionally sensitive to its task, which we call its functional spine <span class="cite">([Rajesh & Khosla, 2026](#ref-rajesh2026))</span>. We found that the representations of pretrained vision networks are remarkably compressible: a small fraction of the task-sensitive subspace preserves most of the network's performance. This compressed representation is also more robust to adversarial attacks, and separates functionally distinct directions, like those sensitive to shape and to texture. Restricting representational comparisons to these subspaces also uncovers differences between networks that full-space similarity measures cannot detect. Another, more qualitative, way of identifying representational differences is to test whether networks exhibit emergent properties well known from perception and neuroscience. In earlier work, we tested deep networks for a range of such brain-like properties and found that architecture had the strongest impact on their emergence, compared to training data and training regime <span class="cite">([Rajesh, Jacob & Arun, 2024](#ref-rajesh2024))</span>.

<details class="references">
<summary>References</summary>
<ol>
  <li id="ref-yamins2014">Yamins, D. L. K., Hong, H., Cadieu, C. F., Solomon, E. A., Seibert, D., &amp; DiCarlo, J. J. (2014). Performance-optimized hierarchical models predict neural responses in higher visual cortex. <em>PNAS</em>, 111(23). <a href="https://doi.org/10.1073/pnas.1403112111" target="_blank" rel="noopener noreferrer">doi</a></li>
  <li id="ref-cao2021">Cao, R., &amp; Yamins, D. L. K. (2021). Forms of explanation and understanding for neuroscience and artificial intelligence. <em>Journal of Neurophysiology</em>. <a href="https://doi.org/10.1152/jn.00195.2021" target="_blank" rel="noopener noreferrer">doi</a></li>
  <li id="ref-conwell2024">Conwell, C., Prince, J. S., Kay, K. N., Alvarez, G. A., &amp; Konkle, T. (2024). A large-scale examination of inductive biases shaping high-level visual representation in brains and machines. <em>Nature Communications</em>, 15, 9383. <a href="https://doi.org/10.1038/s41467-024-53147-y" target="_blank" rel="noopener noreferrer">doi</a></li>
  <li id="ref-naselaris2011">Naselaris, T., Kay, K. N., Nishimoto, S., &amp; Gallant, J. L. (2011). Encoding and decoding in fMRI. <em>NeuroImage</em>, 56(2). <a href="https://doi.org/10.1016/j.neuroimage.2010.07.073" target="_blank" rel="noopener noreferrer">doi</a></li>
  <li id="ref-cichy2016">Cichy, R. M., Khosla, A., Pantazis, D., Torralba, A., &amp; Oliva, A. (2016). Comparison of deep neural networks to spatio-temporal cortical dynamics of human visual object recognition reveals hierarchical correspondence. <em>Scientific Reports</em>, 6, 27755. <a href="https://doi.org/10.1038/srep27755" target="_blank" rel="noopener noreferrer">doi</a></li>
  <li id="ref-bashivan2019">Bashivan, P., Kar, K., &amp; DiCarlo, J. J. (2019). Neural population control via deep image synthesis. <em>Science</em>, 364(6439). <a href="https://doi.org/10.1126/science.aav9436" target="_blank" rel="noopener noreferrer">doi</a></li>
  <li id="ref-frankle2019">Frankle, J., &amp; Carbin, M. (2019). The lottery ticket hypothesis: Finding sparse, trainable neural networks. <em>ICLR</em>. <a href="https://arxiv.org/abs/1803.03635" target="_blank" rel="noopener noreferrer">arXiv</a></li>
  <li id="ref-lake2017">Lake, B. M., Ullman, T. D., Tenenbaum, J. B., &amp; Gershman, S. J. (2017). Building machines that learn and think like people. <em>Behavioral and Brain Sciences</em>, 40, e253. <a href="https://doi.org/10.1017/S0140525X16001837" target="_blank" rel="noopener noreferrer">doi</a></li>
  <li id="ref-szegedy2014">Szegedy, C., Zaremba, W., Sutskever, I., Bruna, J., Erhan, D., Goodfellow, I., &amp; Fergus, R. (2014). Intriguing properties of neural networks. <em>ICLR</em>. <a href="https://arxiv.org/abs/1312.6199" target="_blank" rel="noopener noreferrer">arXiv</a></li>
  <li id="ref-rajesh2026"><strong>Rajesh, N.</strong>, &amp; Khosla, M. (2026). Compressible representations: Functional spines in deep neural networks. <em>NeurIPS</em>. <a href="https://openreview.net/forum?id=El13WPr9FG" target="_blank" rel="noopener noreferrer">paper</a></li>
  <li id="ref-rajesh2024"><strong>Rajesh, N.</strong>, Jacob, G., &amp; Arun, S. P. (2024). Brain-like emergent properties in deep networks. <em>Preprint</em>. <a href="https://arxiv.org/abs/2411.16326" target="_blank" rel="noopener noreferrer">arXiv</a></li>
</ol>
</details>

## Publications

{% include publication_list.html items=site.data.publications.papers %}

### Theses & presentations

{% include publication_list.html items=site.data.publications.theses_and_talks %}

<script>
  // Open the references list when a citation is clicked, then jump to the entry.
  document.querySelectorAll('.cite a[href^="#ref-"]').forEach(function (a) {
    a.addEventListener('click', function () {
      var refs = document.querySelector('details.references');
      if (refs) refs.open = true;
    });
  });
</script>
