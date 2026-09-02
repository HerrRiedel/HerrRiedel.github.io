---
permalink: /CV/
title: "CVs"
excerpt: "Curriculum vitae"
author_profile: true
classes: wide
redirect_from:
  - /CV/
  - /CV.html
---

<div class="cv-switch" id="cv-switch">
  <button type="button" class="active"
          data-src="/assets/cv/Gabriel-Canedo-Riedel-Academic-CV.pdf">Academic CV</button>
  <button type="button"
          data-src="/assets/cv/Gabriel-Canedo-Riedel-CV.pdf">CV</button>
  <button type="button"
          data-src="/assets/cv/Gabriel-Canedo-Riedel-CV-Spanish.pdf">CV (Spanish)</button>
</div>

<div class="cv-viewer">
  <iframe id="cv-frame" title="Curriculum vitae"
          src="/assets/cv/Gabriel-Canedo-Riedel-Academic-CV.pdf#view=FitH&pagemode=none&navpanes=0"></iframe>
</div>

<p class="cv-fallback">
  If the viewer does not load,
  <a id="cv-open" href="/assets/cv/Gabriel-Canedo-Riedel-Academic-CV.pdf" target="_blank" rel="noopener">open it in a new tab</a>.
</p>

<script>
(function () {
  var VIEW = '#view=FitH&pagemode=none&navpanes=0';
  var wrap = document.getElementById('cv-switch');
  if (!wrap) return;
  var frame = document.getElementById('cv-frame');
  var open  = document.getElementById('cv-open');

  wrap.addEventListener('click', function (e) {
    var btn = e.target.closest('button[data-src]');
    if (!btn) return;
    var src = btn.getAttribute('data-src');

    wrap.querySelectorAll('button').forEach(function (b) {
      b.classList.toggle('active', b === btn);
    });

    /* view=FitH  - fit the page width
       pagemode=none - pdf.js (Firefox): start with the sidebar closed. Needed
                       because pdf.js remembers per-document view state, so a
                       sidebar opened once would reopen on every later visit.
       navpanes=0    - same intent for Chrome's viewer and Acrobat.
       Setting .src (not just the hash) forces an actual reload of the file. */
    frame.src = src + VIEW;
    open.href = src;
  });
})();
</script>
