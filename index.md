const mathBlocks = document.querySelectorAll('script[type^="math/tex"]');
Array.from(mathBlocks).forEach((el) => {
  const tex = el.textContent.replace("% <![CDATA[", "").replace("%]]>", "");
  el.outerHTML = window.katex.renderToString(tex, {
    displayMode: el.type === "math/tex; mode=display",
  });
});


When \(a \ne 0\), there are two solutions to \(ax^2 + bx + c = 0\) and they are
$$x = {-b \pm \sqrt{b^2-4ac} \over 2a}.$$
