---
layout: page
title: Illustrations
permalink: /images/
nav_order: 4
---
## I really enjoy creating my own figures for presentations and publications! Here are some of my illustrations.

### Notes on usage:
Feel free to use these images under the **Creative Commons Attribution–NonCommercial 4.0 International License (CC BY-NC 4.0)**.
[Read the full license](https://creativecommons.org/licenses/by-nc/4.0/)

---
<style>
.pdf-gallery {
  display: flex;
  flex-wrap: wrap;
  gap: 1rem;
  justify-content: center;
  margin-top: 2rem;
}

.pdf-gallery-item {
  text-align: center;
  width: 200px;
  cursor: pointer;
}

.pdf-gallery-item img {
  width: 100%;
  border: 1px solid #ccc;
  border-radius: 4px;
  transition: transform 0.2s;
}

.pdf-gallery-item img:hover {
  transform: scale(1.05);
}

.pdf-viewer {
  margin-top: 2rem;
  text-align: center;
}

.pdf-viewer iframe {
  width: 100%;
  height: 600px;
  border: none;
}
</style>

<div class="pdf-gallery">
  <div class="pdf-gallery-item" onclick="loadPDF('{{ 'assets/illustrations/genetic_tools.pdf' | relative_url }}')">
    <img src="{{ 'assets/illustrations/genetic_tools_thumb.png' | relative_url }}" alt="Genetic Tools PDF">
    <p>Genetic Tools</p>
  </div>
  <div class="pdf-gallery-item" onclick="loadPDF('{{ 'assets/illustrations/transformation.pdf' | relative_url }}')">
    <img src="{{ 'assets/illustrations/transformation_thumb.png' | relative_url }}" alt="Transformation PDF">
    <p>Transformation</p>
  </div>
  <div class="pdf-gallery-item" onclick="loadPDF('{{ 'assets/illustrations/microbiome.pdf' | relative_url }}')">
    <img src="{{ 'assets/illustrations/microbiome_thumb.png' | relative_url }}" alt="Microbiome PDF">
    <p>Microbiome</p>
  </div>
</div>

<div class="pdf-viewer" id="pdfViewer">
  <!-- PDF will load here when clicked -->
</div>

<script>
function loadPDF(pdfPath) {
  document.getElementById('pdfViewer').innerHTML = `
    <iframe src="${pdfPath}" allowfullscreen></iframe>
  `;
  window.scrollTo({
    top: document.getElementById('pdfViewer').offsetTop - 20,
    behavior: 'smooth'
  });
}
</script>
