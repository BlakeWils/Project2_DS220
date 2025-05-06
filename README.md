<div id="b9e8e3c3" class="cell markdown">
<h3
id="6-analyze-the-distribution-of-played_until--year-career-span-and-see-how-its-evolved-eg-longer-careers-today">6.
Analyze the distribution of “played_until – year” (career span) and see
how it’s evolved (e.g. longer careers today?).</h3>
</div>
<div id="894e236c" class="cell code">
<div class="sourceCode" id="cb25"><pre
class="sourceCode python"><code class="sourceCode python"><span id="cb25-1"><a href="#cb25-1" aria-hidden="true" tabindex="-1"></a><span class="co">#6:</span></span>
<span id="cb25-2"><a href="#cb25-2" aria-hidden="true" tabindex="-1"></a>df[<span class="st">&#39;career_span&#39;</span>] <span class="op">=</span> df[<span class="st">&#39;played_until&#39;</span>] <span class="op">-</span> df[<span class="st">&#39;year&#39;</span>]</span>
<span id="cb25-3"><a href="#cb25-3" aria-hidden="true" tabindex="-1"></a>df <span class="op">=</span> df[df[<span class="st">&#39;career_span&#39;</span>].between(<span class="dv">0</span>, <span class="dv">30</span>)]</span>
<span id="cb25-4"><a href="#cb25-4" aria-hidden="true" tabindex="-1"></a></span>
<span id="cb25-5"><a href="#cb25-5" aria-hidden="true" tabindex="-1"></a><span class="co"># Box Plot</span></span>
<span id="cb25-6"><a href="#cb25-6" aria-hidden="true" tabindex="-1"></a>plt.figure(figsize<span class="op">=</span>(<span class="dv">12</span>,<span class="dv">6</span>))</span>
<span id="cb25-7"><a href="#cb25-7" aria-hidden="true" tabindex="-1"></a>df.boxplot(column<span class="op">=</span><span class="st">&#39;career_span&#39;</span>, by<span class="op">=</span><span class="st">&#39;decade&#39;</span>)</span>
<span id="cb25-8"><a href="#cb25-8" aria-hidden="true" tabindex="-1"></a>plt.suptitle(<span class="st">&#39;&#39;</span>)</span>
<span id="cb25-9"><a href="#cb25-9" aria-hidden="true" tabindex="-1"></a>plt.title(<span class="st">&#39;Career Span (Years) by Draft Decade&#39;</span>)</span>
<span id="cb25-10"><a href="#cb25-10" aria-hidden="true" tabindex="-1"></a>plt.xlabel(<span class="st">&#39;Draft Decade&#39;</span>)</span>
<span id="cb25-11"><a href="#cb25-11" aria-hidden="true" tabindex="-1"></a>plt.ylabel(<span class="st">&#39;Career Span (Years)&#39;</span>)</span>
<span id="cb25-12"><a href="#cb25-12" aria-hidden="true" tabindex="-1"></a>plt.show()</span></code></pre></div>
<div class="output display_data">
<pre><code>&lt;Figure size 1200x600 with 0 Axes&gt;</code></pre>
</div>
<div class="output display_data">
<p><img
src="vertopal_fddae5917a2a416ebbc3cfcc49b3aabf/7ddc16645dab8434d01f9d98ef8dad77f84c3156.png" /></p>
</div>
</div>
<div id="1aac81ce" class="cell markdown">
<p><strong>Insights for Question 6:</strong></p>
<ul>
<li>The median for each decade is right around 5 except for 2010 and
2020 because the data only goes to 2021, so the average NFL career is
about 4-5 years, looking only from 1970 - 2000.</li>
<li>The player with the longest career played 25 seasons, with only 2
others also above 20 years.</li>
<li>From 1970s to 2000s, the graphs are very similar with the exception
of outliers. So, this shows the average length of an NFL career has had
little-to-no change</li>
</ul>
</div>
</body>
</html>
