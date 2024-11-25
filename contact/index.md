---
title: Contact
nav:
  order: 4
---

# Contact

We are always looking for enthusiastic and motivated individuals to join our lab! We welcome inquiries from students and researchers at all levels who are passionate about the intersection of computational biology and environmental toxicology. If you’re interested in joining the lab, please email Jess at the address below with a brief statement of your interests and your CV.

{%
  include button.html
  type="email"
  text="1jess.ewald@gmail.com"
  link="1jess.ewald@gmail.com"
%}
{%
  include button.html
  type="address"
  link="https://maps.app.goo.gl/XFsVs3CxMfyqV6idA"
%}

{% include section.html %}

{% capture col1 %}

{%
  include figure.html
  image="images/photo.jpg"
  caption="Lorem ipsum"
%}

{% endcapture %}

{% capture col2 %}

{%
  PhD students are recruited via the EMBL International PhD Programme (https://www.embl.de/training/eipp/application/index.html). For queries regarding the programme, please contact the EBI Research Office (roffice@ebi.ac.uk).
%}

{% endcapture %}

{% include cols.html col1=col1 col2=col2 %}

{% include section.html dark=true %}

{% capture col1 %}
  include plain-image.html
  image="images/campus.jpg"
{% endcapture %}

{% capture col2 %}
  Our lab is located at EMBL-EBI on the beautiful Wellcome Genome Campus in Hinxton, UK
{% endcapture %}

{% capture col3 %}
  include plain-image.html
  image="images/hinxton.jpg"
{% endcapture %}

{% include cols.html col1=col1 col2=col2 col3=col3 %}
