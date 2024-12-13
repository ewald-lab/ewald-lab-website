---
---

## We identify and characterize chemical hazards to humans and ecosystems with cell profiling data, machine learning, and integrative data analysis.
{% include section.html %}


## The Big Problem

{% capture col1 %}
Environmental contaminants cause 16% of premature deaths worldwide, yet most chemicals in commercial use have never been assessed for their potential to cause harm to humans or ecosystems. Traditional toxicity testing methods that use live animals are too expensive, slow, and ethically concerning to assess chemical hazard at scale. 
{% endcapture %}

{% capture col2 %}
{%
  include plain-image.html
  image="images/1_chem_problem.svg"
  width="300px"
  caption="There are too many chemicals with unknown toxicity to assess with traditional methods."
%}
{% endcapture %}

{% include cols.html col1=col1 col2=col2 %}
{% include section.html %}


## A New Paradigm
{% capture col1 %}
{%
  include plain-image.html
  image="images/2_chem_prior.svg"
  width="500px"
  caption="There are too many chemicals with unknown toxicity to assess with traditional methods."
%}
{% endcapture %}

{% capture col2 %}
Drug discovery programs routinely screen thousands to millions of compounds in computational and cellular models for their potential to treat disease. What if we used this same technology to assess whether chemicals used in other sectors of society are dangerous? Scientists and government regulators are urgently working to implement high-throughput screening methods to prioritize resource-instensive testing for the most hazardous compounds. 
{% endcapture %}

{% include cols.html col1=col1 col2=col2 %}
{% include section.html %}


## Computational Biology Challenges

{% capture col1 %}
A brute-force approach of testing every compound in all cell types and species is impractical. Instead, scientists must develop computational approaches that leverage prior knowledge of taxonomic relationships, cell types, and cell state to design efficient chemical screens and extrapolate observed toxicity across biological space.
{% endcapture %}

{% capture col2 %}
{%
  include plain-image.html
  image="images/3_extrapolate.png"
  width="400px"
  caption="There are too many chemicals with unknown toxicity to assess with traditional methods."
%}
{% endcapture %}

{% include cols.html col1=col1 col2=col2 %}
{% include section.html %}


## Our Work

Omics data enables us to measure thousands of molecular and morphological features from cells after they are exposed to chemicals. When we measure these data from *in vitro* cellular assays, we call it “cell profiling”. Using cell profiling data, the Ewald Lab:

- Estimates the lowest chemical exposure that causes molecular and morphological perturbations in different tissues of living organisms (including humans!) for thousands of compounds

- Predicts how chemicals cause toxicity by analyzing images of exposed cells with machine learning, transfer learning, and multi-omics integration

- Creates user-friendly web-tools that connect cell profiles to toxicity data from diverse *in silico*, *in vitro*, and *in vivo* sources

We also value collaborating closely with stakeholders across government, industry, and academia to maximize the translational impact of our work.