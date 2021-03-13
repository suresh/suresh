### Hi there 👋 I'm Suresh. 

🔭 I am a Data Science Director working on Machine Learning problems. I'm currently working on Natural Language Processing, Text Mining, and Time Series Analysis areas. My work relies heavily on crunching a ton of data and implementing efficient program algorithms, Monte Carlo modeling, and performing statistical inference. In the past, I have worked on several firms in financial services, manufacturing & retail industries.

### 🌱 Skills
My preferred tools for machine learning (scikit, xgboost), data visualization (D3.js), big data (Spark), deep learning (Theano, Keras, TensorFlow).

  * Python [pandas, scikit-learn, numpy, pyspark]
  * R [ggplot, caret, data.table, dplyr/tidyr]
  * Scala, Spark [MLlib, GraphX, DataFrames]
  * SQL [Hive, PostgreSQL, MySQL]
  * Linux & MacOS, Git [GitHub], AWS [EMR, S3, EC2]

### 📫 How to reach me
Drop me a line at suresh.shanmugam@icloud.com about anything or your project if you’re interested in working with me.

### Latest Blog Posts on www.sureshshanmugam.com
<!--START_SECTION:feed-->
#### [Writing with less friction. Case for iPad](https:&#x2F;&#x2F;sureshshanmugam.com&#x2F;articles&#x2F;ipad-writing&#x2F;) 
*Writing requires focus
Writing is one of the most cogent ways to communicate with others. It requires work from the author to do critical thinking and come up with an engaging story line. Topics need to be looked from various angles and be considered carefully before coming with a certain points of view.
Writing needs focus and emphasis on clarity of thought from the author. Words left out are not essential to the main arc. Writing is akin to gardening. Gardens need great deal of planning and understanding before first seeds are sown. But the real work starts after the first shoots appear. These need to be tended to with deft hands and any weed or excess growth needs to be removed. Gardening is as much as about thinking and following a rigorous routine over many days to get the desired results.
iPad in my case along with apps like Working Copy and IA are essential to how I create these posts. Simplicity of this setups removes all the distractions and makes me focus on the task at hand. Critically think about what words I want to say to convey the thought I hold now.
Tools have come along way and we have not changed our approach to include these in our ways. Digital tools are seen as distractions with big access to addictive outlets like social feeds and unlimited videos. But with them they bring these incredible creative tools when wielded well can make nearly everyone a creator. You don’t need a large setup or team to write and share your insights to this world. Often I’m far to distracted by next shiny thing that I fail to pay attention to the hard grind of writing and coming up with original thoughts than can turn into words. We all need more time to cultivate our writing gardens. Start in a small way and keep at it until it becomes a second nature to me.*
#### [Altair Sample Viz](https:&#x2F;&#x2F;sureshshanmugam.com&#x2F;articles&#x2F;altair-notebook-sample&#x2F;) 
*Faceted Scatter Plot with Linked Brushing
This is an example of using an interval selection to control the color of points across multiple facets.




1
2
3
4

import altair as alt
from vega_datasets import data

cars &#x3D; data.cars()








1
2
3
4
5
6
7
8
9
10
11
12
13
14
15

brush &#x3D; alt.selection(type&#x3D;&#39;interval&#39;, resolve&#x3D;&#39;global&#39;)

base &#x3D; alt.Chart(cars).mark_point().encode(
    y&#x3D;&#39;Miles_per_Gallon&#39;,
    color&#x3D;alt.condition(brush, &#39;Origin&#39;, alt.ColorValue(&#39;gray&#39;))
).add_selection(
    brush
).properties(
    width&#x3D;250,
    height&#x3D;250
)

print(&quot;Select a region in the chart below to try this out!&quot;)

base.encode(x&#x3D;&#39;Horsepower&#39;) | base.encode(x&#x3D;&#39;Acceleration&#39;)








1

Select a region in the chart below to try this out!






  (function(spec, embedOpt){
    let outputDiv &#x3D; document.currentScript.previousElementSibling;
    if (outputDiv.id !&#x3D;&#x3D; &quot;altair-viz-c9cb2c7a41d44eeaa497f0ffc46218c6&quot;) {
      outputDiv &#x3D; document.getElementById(&quot;altair-viz-c9cb2c7a41d44eeaa497f0ffc46218c6&quot;);
    }
    const paths &#x3D; {
      &quot;vega&quot;: &quot;https:&#x2F;&#x2F;cdn.jsdelivr.net&#x2F;npm&#x2F;&#x2F;vega@5?noext&quot;,
      &quot;vega-lib&quot;: &quot;https:&#x2F;&#x2F;cdn.jsdelivr.net&#x2F;npm&#x2F;&#x2F;vega-lib?noext&quot;,
      &quot;vega-lite&quot;: &quot;https:&#x2F;&#x2F;cdn.jsdelivr.net&#x2F;npm&#x2F;&#x2F;vega-lite@4.8.1?noext&quot;,
      &quot;vega-embed&quot;: &quot;https:&#x2F;&#x2F;cdn.jsdelivr.net&#x2F;npm&#x2F;&#x2F;vega-embed@6?noext&quot;,
    };

    function loadScript(lib) {
      return new Promise(function(resolve, reject) {
        var s &#x3D; document.createElement(&#39;script&#39;);
        s.src &#x3D; paths[lib];
        s.async &#x3D; true;
        s.onload &#x3D; () &#x3D;&gt; resolve(paths[lib]);
        s.onerror &#x3D; () &#x3D;&gt; reject(&#x60;Error loading script: ${paths[lib]}&#x60;);
        document.getElementsByTagName(&quot;head&quot;)[0].appendChild(s);
      });
    }

    function showError(err) {
      outputDiv.innerHTML &#x3D; &#x60;
${err}
&#x60;;
      throw err;
    }

    function displayChart(vegaEmbed) {
      vegaEmbed(outputDiv, spec, embedOpt)
        .catch(err &#x3D;&gt; showError(&#x60;Javascript Error: ${err.message}
This usually means there&#39;s a typo in your chart specification. See the javascript console for the full traceback.&#x60;));
    }

    if(typeof define &#x3D;&#x3D;&#x3D; &quot;function&quot; &amp;&amp; define.amd) {
      requirejs.config({paths});
      require([&quot;vega-embed&quot;], displayChart, err &#x3D;&gt; showError(&#x60;Error loading script: ${err.message}&#x60;));
    } else if (typeof vegaEmbed &#x3D;&#x3D;&#x3D; &quot;function&quot;) {
      displayChart(vegaEmbed);
    } else {
      loadScript(&quot;vega&quot;)
        .then(() &#x3D;&gt; loadScript(&quot;vega-lite&quot;))
        .then(() &#x3D;&gt; loadScript(&quot;vega-embed&quot;))
        .catch(showError)
        .then(() &#x3D;&gt; displayChart(vegaEmbed));
    }
  })({&quot;config&quot;: {&quot;view&quot;: {&quot;continuousWidth&quot;: 400, &quot;continuousHeight&quot;: 300}}, &quot;hconcat&quot;: [{&quot;mark&quot;: &quot;point&quot;, &quot;encoding&quot;: {&quot;color&quot;: {&quot;condition&quot;: {&quot;type&quot;: &quot;nominal&quot;, &quot;field&quot;: &quot;Origin&quot;, &quot;selection&quot;: &quot;selector001&quot;}, &quot;value&quot;: &quot;gray&quot;}, &quot;x&quot;: {&quot;type&quot;: &quot;quantitative&quot;, &quot;field&quot;: &quot;Horsepower&quot;}, &quot;y&quot;: {&quot;type&quot;: &quot;quantitative&quot;, &quot;field&quot;: &quot;Miles_per_Gallon&quot;}}, &quot;height&quot;: 250, &quot;selection&quot;: {&quot;selector001&quot;: {&quot;type&quot;: &quot;interval&quot;, &quot;resolve&quot;: &quot;global&quot;}}, &quot;width&quot;: 250}, {&quot;mark&quot;: &quot;point&quot;, &quot;encoding&quot;: {&quot;color&quot;: {&quot;condition&quot;: {&quot;type&quot;: &quot;nominal&quot;, &quot;field&quot;: &quot;Origin&quot;, &quot;selection&quot;: &quot;selector001&quot;}, &quot;value&quot;: &quot;gray&quot;}, &quot;x&quot;: {&quot;type&quot;: &quot;quantitative&quot;, &quot;field&quot;: &quot;Acceleration&quot;}, &quot;y&quot;: {&quot;type&quot;: &quot;quantitative&quot;, &quot;field&quot;: &quot;Miles_per_Gallon&quot;}}, &quot;height&quot;: 250, &quot;selection&quot;: {&quot;selector001&quot;: {&quot;type&quot;: &quot;interval&quot;, &quot;resolve&quot;: &quot;global&quot;}}, &quot;width&quot;: 250}], &quot;data&quot;: {&quot;name&quot;: &quot;data-f02450ab61490a1363517a0190416235&quot;}, &quot;$schema&quot;: &quot;https:&#x2F;&#x2F;vega.github.io&#x2F;schema&#x2F;vega-lite&#x2F;v4.8.1.json&quot;, &quot;datasets&quot;: {&quot;data-f02450ab61490a1363517a0190416235&quot;: [{&quot;Name&quot;: &quot;chevrolet chevelle malibu&quot;, &quot;Miles_per_Gallon&quot;: 18.0, &quot;Cylinders&quot;: 8, &quot;Displacement&quot;: 307.0, &quot;Horsepower&quot;: 130.0, &quot;Weight_in_lbs&quot;: 3504, &quot;Acceleration&quot;: 12.0, &quot;Year&quot;: &quot;1970-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;USA&quot;}, {&quot;Name&quot;: &quot;buick skylark 320&quot;, &quot;Miles_per_Gallon&quot;: 15.0, &quot;Cylinders&quot;: 8, &quot;Displacement&quot;: 350.0, &quot;Horsepower&quot;: 165.0, &quot;Weight_in_lbs&quot;: 3693, &quot;Acceleration&quot;: 11.5, &quot;Year&quot;: &quot;1970-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;USA&quot;}, {&quot;Name&quot;: &quot;plymouth satellite&quot;, &quot;Miles_per_Gallon&quot;: 18.0, &quot;Cylinders&quot;: 8, &quot;Displacement&quot;: 318.0, &quot;Horsepower&quot;: 150.0, &quot;Weight_in_lbs&quot;: 3436, &quot;Acceleration&quot;: 11.0, &quot;Year&quot;: &quot;1970-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;USA&quot;}, {&quot;Name&quot;: &quot;amc rebel sst&quot;, &quot;Miles_per_Gallon&quot;: 16.0, &quot;Cylinders&quot;: 8, &quot;Displacement&quot;: 304.0, &quot;Horsepower&quot;: 150.0, &quot;Weight_in_lbs&quot;: 3433, &quot;Acceleration&quot;: 12.0, &quot;Year&quot;: &quot;1970-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;USA&quot;}, {&quot;Name&quot;: &quot;ford torino&quot;, &quot;Miles_per_Gallon&quot;: 17.0, &quot;Cylinders&quot;: 8, &quot;Displacement&quot;: 302.0, &quot;Horsepower&quot;: 140.0, &quot;Weight_in_lbs&quot;: 3449, &quot;Acceleration&quot;: 10.5, &quot;Year&quot;: &quot;1970-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;USA&quot;}, {&quot;Name&quot;: &quot;ford galaxie 500&quot;, &quot;Miles_per_Gallon&quot;: 15.0, &quot;Cylinders&quot;: 8, &quot;Displacement&quot;: 429.0, &quot;Horsepower&quot;: 198.0, &quot;Weight_in_lbs&quot;: 4341, &quot;Acceleration&quot;: 10.0, &quot;Year&quot;: &quot;1970-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;USA&quot;}, {&quot;Name&quot;: &quot;chevrolet impala&quot;, &quot;Miles_per_Gallon&quot;: 14.0, &quot;Cylinders&quot;: 8, &quot;Displacement&quot;: 454.0, &quot;Horsepower&quot;: 220.0, &quot;Weight_in_lbs&quot;: 4354, &quot;Acceleration&quot;: 9.0, &quot;Year&quot;: &quot;1970-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;USA&quot;}, {&quot;Name&quot;: &quot;plymouth fury iii&quot;, &quot;Miles_per_Gallon&quot;: 14.0, &quot;Cylinders&quot;: 8, &quot;Displacement&quot;: 440.0, &quot;Horsepower&quot;: 215.0, &quot;Weight_in_lbs&quot;: 4312, &quot;Acceleration&quot;: 8.5, &quot;Year&quot;: &quot;1970-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;USA&quot;}, {&quot;Name&quot;: &quot;pontiac catalina&quot;, &quot;Miles_per_Gallon&quot;: 14.0, &quot;Cylinders&quot;: 8, &quot;Displacement&quot;: 455.0, &quot;Horsepower&quot;: 225.0, &quot;Weight_in_lbs&quot;: 4425, &quot;Acceleration&quot;: 10.0, &quot;Year&quot;: &quot;1970-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;USA&quot;}, {&quot;Name&quot;: &quot;amc ambassador dpl&quot;, &quot;Miles_per_Gallon&quot;: 15.0, &quot;Cylinders&quot;: 8, &quot;Displacement&quot;: 390.0, &quot;Horsepower&quot;: 190.0, &quot;Weight_in_lbs&quot;: 3850, &quot;Acceleration&quot;: 8.5, &quot;Year&quot;: &quot;1970-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;USA&quot;}, {&quot;Name&quot;: &quot;citroen ds-21 pallas&quot;, &quot;Miles_per_Gallon&quot;: null, &quot;Cylinders&quot;: 4, &quot;Displacement&quot;: 133.0, &quot;Horsepower&quot;: 115.0, &quot;Weight_in_lbs&quot;: 3090, &quot;Acceleration&quot;: 17.5, &quot;Year&quot;: &quot;1970-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;Europe&quot;}, {&quot;Name&quot;: &quot;chevrolet chevelle concours (sw)&quot;, &quot;Miles_per_Gallon&quot;: null, &quot;Cylinders&quot;: 8, &quot;Displacement&quot;: 350.0, &quot;Horsepower&quot;: 165.0, &quot;Weight_in_lbs&quot;: 4142, &quot;Acceleration&quot;: 11.5, &quot;Year&quot;: &quot;1970-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;USA&quot;}, {&quot;Name&quot;: &quot;ford torino (sw)&quot;, &quot;Miles_per_Gallon&quot;: null, &quot;Cylinders&quot;: 8, &quot;Displacement&quot;: 351.0, &quot;Horsepower&quot;: 153.0, &quot;Weight_in_lbs&quot;: 4034, &quot;Acceleration&quot;: 11.0, &quot;Year&quot;: &quot;1970-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;USA&quot;}, {&quot;Name&quot;: &quot;plymouth satellite (sw)&quot;, &quot;Miles_per_Gallon&quot;: null, &quot;Cylinders&quot;: 8, &quot;Displacement&quot;: 383.0, &quot;Horsepower&quot;: 175.0, &quot;Weight_in_lbs&quot;: 4166, &quot;Acceleration&quot;: 10.5, &quot;Year&quot;: &quot;1970-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;USA&quot;}, {&quot;Name&quot;: &quot;amc rebel sst (sw)&quot;, &quot;Miles_per_Gallon&quot;: null, &quot;Cylinders&quot;: 8, &quot;Displacement&quot;: 360.0, &quot;Horsepower&quot;: 175.0, &quot;Weight_in_lbs&quot;: 3850, &quot;Acceleration&quot;: 11.0, &quot;Year&quot;: &quot;1970-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;USA&quot;}, {&quot;Name&quot;: &quot;dodge challenger se&quot;, &quot;Miles_per_Gallon&quot;: 15.0, &quot;Cylinders&quot;: 8, &quot;Displacement&quot;: 383.0, &quot;Horsepower&quot;: 170.0, &quot;Weight_in_lbs&quot;: 3563, &quot;Acceleration&quot;: 10.0, &quot;Year&quot;: &quot;1970-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;USA&quot;}, {&quot;Name&quot;: &quot;plymouth &#39;cuda 340&quot;, &quot;Miles_per_Gallon&quot;: 14.0, &quot;Cylinders&quot;: 8, &quot;Displacement&quot;: 340.0, &quot;Horsepower&quot;: 160.0, &quot;Weight_in_lbs&quot;: 3609, &quot;Acceleration&quot;: 8.0, &quot;Year&quot;: &quot;1970-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;USA&quot;}, {&quot;Name&quot;: &quot;ford mustang boss 302&quot;, &quot;Miles_per_Gallon&quot;: null, &quot;Cylinders&quot;: 8, &quot;Displacement&quot;: 302.0, &quot;Horsepower&quot;: 140.0, &quot;Weight_in_lbs&quot;: 3353, &quot;Acceleration&quot;: 8.0, &quot;Year&quot;: &quot;1970-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;USA&quot;}, {&quot;Name&quot;: &quot;chevrolet monte carlo&quot;, &quot;Miles_per_Gallon&quot;: 15.0, &quot;Cylinders&quot;: 8, &quot;Displacement&quot;: 400.0, &quot;Horsepower&quot;: 150.0, &quot;Weight_in_lbs&quot;: 3761, &quot;Acceleration&quot;: 9.5, &quot;Year&quot;: &quot;1970-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;USA&quot;}, {&quot;Name&quot;: &quot;buick estate wagon (sw)&quot;, &quot;Miles_per_Gallon&quot;: 14.0, &quot;Cylinders&quot;: 8, &quot;Displacement&quot;: 455.0, &quot;Horsepower&quot;: 225.0, &quot;Weight_in_lbs&quot;: 3086, &quot;Acceleration&quot;: 10.0, &quot;Year&quot;: &quot;1970-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;USA&quot;}, {&quot;Name&quot;: &quot;toyota corona mark ii&quot;, &quot;Miles_per_Gallon&quot;: 24.0, &quot;Cylinders&quot;: 4, &quot;Displacement&quot;: 113.0, &quot;Horsepower&quot;: 95.0, &quot;Weight_in_lbs&quot;: 2372, &quot;Acceleration&quot;: 15.0, &quot;Year&quot;: &quot;1970-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;Japan&quot;}, {&quot;Name&quot;: &quot;plymouth duster&quot;, &quot;Miles_per_Gallon&quot;: 22.0, &quot;Cylinders&quot;: 6, &quot;Displacement&quot;: 198.0, &quot;Horsepower&quot;: 95.0, &quot;Weight_in_lbs&quot;: 2833, &quot;Acceleration&quot;: 15.5, &quot;Year&quot;: &quot;1970-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;USA&quot;}, {&quot;Name&quot;: &quot;amc hornet&quot;, &quot;Miles_per_Gallon&quot;: 18.0, &quot;Cylinders&quot;: 6, &quot;Displacement&quot;: 199.0, &quot;Horsepower&quot;: 97.0, &quot;Weight_in_lbs&quot;: 2774, &quot;Acceleration&quot;: 15.5, &quot;Year&quot;: &quot;1970-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;USA&quot;}, {&quot;Name&quot;: &quot;ford maverick&quot;, &quot;Miles_per_Gallon&quot;: 21.0, &quot;Cylinders&quot;: 6, &quot;Displacement&quot;: 200.0, &quot;Horsepower&quot;: 85.0, &quot;Weight_in_lbs&quot;: 2587, &quot;Acceleration&quot;: 16.0, &quot;Year&quot;: &quot;1970-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;USA&quot;}, {&quot;Name&quot;: &quot;datsun pl510&quot;, &quot;Miles_per_Gallon&quot;: 27.0, &quot;Cylinders&quot;: 4, &quot;Displacement&quot;: 97.0, &quot;Horsepower&quot;: 88.0, &quot;Weight_in_lbs&quot;: 2130, &quot;Acceleration&quot;: 14.5, &quot;Year&quot;: &quot;1970-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;Japan&quot;}, {&quot;Name&quot;: &quot;volkswagen 1131 deluxe sedan&quot;, &quot;Miles_per_Gallon&quot;: 26.0, &quot;Cylinders&quot;: 4, &quot;Displacement&quot;: 97.0, &quot;Horsepower&quot;: 46.0, &quot;Weight_in_lbs&quot;: 1835, &quot;Acceleration&quot;: 20.5, &quot;Year&quot;: &quot;1970-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;Europe&quot;}, {&quot;Name&quot;: &quot;peugeot 504&quot;, &quot;Miles_per_Gallon&quot;: 25.0, &quot;Cylinders&quot;: 4, &quot;Displacement&quot;: 110.0, &quot;Horsepower&quot;: 87.0, &quot;Weight_in_lbs&quot;: 2672, &quot;Acceleration&quot;: 17.5, &quot;Year&quot;: &quot;1970-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;Europe&quot;}, {&quot;Name&quot;: &quot;audi 100 ls&quot;, &quot;Miles_per_Gallon&quot;: 24.0, &quot;Cylinders&quot;: 4, &quot;Displacement&quot;: 107.0, &quot;Horsepower&quot;: 90.0, &quot;Weight_in_lbs&quot;: 2430, &quot;Acceleration&quot;: 14.5, &quot;Year&quot;: &quot;1970-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;Europe&quot;}, {&quot;Name&quot;: &quot;saab 99e&quot;, &quot;Miles_per_Gallon&quot;: 25.0, &quot;Cylinders&quot;: 4, &quot;Displacement&quot;: 104.0, &quot;Horsepower&quot;: 95.0, &quot;Weight_in_lbs&quot;: 2375, &quot;Acceleration&quot;: 17.5, &quot;Year&quot;: &quot;1970-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;Europe&quot;}, {&quot;Name&quot;: &quot;bmw 2002&quot;, &quot;Miles_per_Gallon&quot;: 26.0, &quot;Cylinders&quot;: 4, &quot;Displacement&quot;: 121.0, &quot;Horsepower&quot;: 113.0, &quot;Weight_in_lbs&quot;: 2234, &quot;Acceleration&quot;: 12.5, &quot;Year&quot;: &quot;1970-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;Europe&quot;}, {&quot;Name&quot;: &quot;amc gremlin&quot;, &quot;Miles_per_Gallon&quot;: 21.0, &quot;Cylinders&quot;: 6, &quot;Displacement&quot;: 199.0, &quot;Horsepower&quot;: 90.0, &quot;Weight_in_lbs&quot;: 2648, &quot;Acceleration&quot;: 15.0, &quot;Year&quot;: &quot;1970-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;USA&quot;}, {&quot;Name&quot;: &quot;ford f250&quot;, &quot;Miles_per_Gallon&quot;: 10.0, &quot;Cylinders&quot;: 8, &quot;Displacement&quot;: 360.0, &quot;Horsepower&quot;: 215.0, &quot;Weight_in_lbs&quot;: 4615, &quot;Acceleration&quot;: 14.0, &quot;Year&quot;: &quot;1970-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;USA&quot;}, {&quot;Name&quot;: &quot;chevy c20&quot;, &quot;Miles_per_Gallon&quot;: 10.0, &quot;Cylinders&quot;: 8, &quot;Displacement&quot;: 307.0, &quot;Horsepower&quot;: 200.0, &quot;Weight_in_lbs&quot;: 4376, &quot;Acceleration&quot;: 15.0, &quot;Year&quot;: &quot;1970-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;USA&quot;}, {&quot;Name&quot;: &quot;dodge d200&quot;, &quot;Miles_per_Gallon&quot;: 11.0, &quot;Cylinders&quot;: 8, &quot;Displacement&quot;: 318.0, &quot;Horsepower&quot;: 210.0, &quot;Weight_in_lbs&quot;: 4382, &quot;Acceleration&quot;: 13.5, &quot;Year&quot;: &quot;1970-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;USA&quot;}, {&quot;Name&quot;: &quot;hi 1200d&quot;, &quot;Miles_per_Gallon&quot;: 9.0, &quot;Cylinders&quot;: 8, &quot;Displacement&quot;: 304.0, &quot;Horsepower&quot;: 193.0, &quot;Weight_in_lbs&quot;: 4732, &quot;Acceleration&quot;: 18.5, &quot;Year&quot;: &quot;1970-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;USA&quot;}, {&quot;Name&quot;: &quot;datsun pl510&quot;, &quot;Miles_per_Gallon&quot;: 27.0, &quot;Cylinders&quot;: 4, &quot;Displacement&quot;: 97.0, &quot;Horsepower&quot;: 88.0, &quot;Weight_in_lbs&quot;: 2130, &quot;Acceleration&quot;: 14.5, &quot;Year&quot;: &quot;1971-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;Japan&quot;}, {&quot;Name&quot;: &quot;chevrolet vega 2300&quot;, &quot;Miles_per_Gallon&quot;: 28.0, &quot;Cylinders&quot;: 4, &quot;Displacement&quot;: 140.0, &quot;Horsepower&quot;: 90.0, &quot;Weight_in_lbs&quot;: 2264, &quot;Acceleration&quot;: 15.5, &quot;Year&quot;: &quot;1971-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;USA&quot;}, {&quot;Name&quot;: &quot;toyota corona&quot;, &quot;Miles_per_Gallon&quot;: 25.0, &quot;Cylinders&quot;: 4, &quot;Displacement&quot;: 113.0, &quot;Horsepower&quot;: 95.0, &quot;Weight_in_lbs&quot;: 2228, &quot;Acceleration&quot;: 14.0, &quot;Year&quot;: &quot;1971-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;Japan&quot;}, {&quot;Name&quot;: &quot;ford pinto&quot;, &quot;Miles_per_Gallon&quot;: 25.0, &quot;Cylinders&quot;: 4, &quot;Displacement&quot;: 98.0, &quot;Horsepower&quot;: null, &quot;Weight_in_lbs&quot;: 2046, &quot;Acceleration&quot;: 19.0, &quot;Year&quot;: &quot;1971-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;USA&quot;}, {&quot;Name&quot;: &quot;volkswagen super beetle 117&quot;, &quot;Miles_per_Gallon&quot;: null, &quot;Cylinders&quot;: 4, &quot;Displacement&quot;: 97.0, &quot;Horsepower&quot;: 48.0, &quot;Weight_in_lbs&quot;: 1978, &quot;Acceleration&quot;: 20.0, &quot;Year&quot;: &quot;1971-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;Europe&quot;}, {&quot;Name&quot;: &quot;amc gremlin&quot;, &quot;Miles_per_Gallon&quot;: 19.0, &quot;Cylinders&quot;: 6, &quot;Displacement&quot;: 232.0, &quot;Horsepower&quot;: 100.0, &quot;Weight_in_lbs&quot;: 2634, &quot;Acceleration&quot;: 13.0, &quot;Year&quot;: &quot;1971-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;USA&quot;}, {&quot;Name&quot;: &quot;plymouth satellite custom&quot;, &quot;Miles_per_Gallon&quot;: 16.0, &quot;Cylinders&quot;: 6, &quot;Displacement&quot;: 225.0, &quot;Horsepower&quot;: 105.0, &quot;Weight_in_lbs&quot;: 3439, &quot;Acceleration&quot;: 15.5, &quot;Year&quot;: &quot;1971-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;USA&quot;}, {&quot;Name&quot;: &quot;chevrolet chevelle malibu&quot;, &quot;Miles_per_Gallon&quot;: 17.0, &quot;Cylinders&quot;: 6, &quot;Displacement&quot;: 250.0, &quot;Horsepower&quot;: 100.0, &quot;Weight_in_lbs&quot;: 3329, &quot;Acceleration&quot;: 15.5, &quot;Year&quot;: &quot;1971-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;USA&quot;}, {&quot;Name&quot;: &quot;ford torino 500&quot;, &quot;Miles_per_Gallon&quot;: 19.0, &quot;Cylinders&quot;: 6, &quot;Displacement&quot;: 250.0, &quot;Horsepower&quot;: 88.0, &quot;Weight_in_lbs&quot;: 3302, &quot;Acceleration&quot;: 15.5, &quot;Year&quot;: &quot;1971-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;USA&quot;}, {&quot;Name&quot;: &quot;amc matador&quot;, &quot;Miles_per_Gallon&quot;: 18.0, &quot;Cylinders&quot;: 6, &quot;Displacement&quot;: 232.0, &quot;Horsepower&quot;: 100.0, &quot;Weight_in_lbs&quot;: 3288, &quot;Acceleration&quot;: 15.5, &quot;Year&quot;: &quot;1971-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;USA&quot;}, {&quot;Name&quot;: &quot;chevrolet impala&quot;, &quot;Miles_per_Gallon&quot;: 14.0, &quot;Cylinders&quot;: 8, &quot;Displacement&quot;: 350.0, &quot;Horsepower&quot;: 165.0, &quot;Weight_in_lbs&quot;: 4209, &quot;Acceleration&quot;: 12.0, &quot;Year&quot;: &quot;1971-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;USA&quot;}, {&quot;Name&quot;: &quot;pontiac catalina brougham&quot;, &quot;Miles_per_Gallon&quot;: 14.0, &quot;Cylinders&quot;: 8, &quot;Displacement&quot;: 400.0, &quot;Horsepower&quot;: 175.0, &quot;Weight_in_lbs&quot;: 4464, &quot;Acceleration&quot;: 11.5, &quot;Year&quot;: &quot;1971-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;USA&quot;}, {&quot;Name&quot;: &quot;ford galaxie 500&quot;, &quot;Miles_per_Gallon&quot;: 14.0, &quot;Cylinders&quot;: 8, &quot;Displacement&quot;: 351.0, &quot;Horsepower&quot;: 153.0, &quot;Weight_in_lbs&quot;: 4154, &quot;Acceleration&quot;: 13.5, &quot;Year&quot;: &quot;1971-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;USA&quot;}, {&quot;Name&quot;: &quot;plymouth fury iii&quot;, &quot;Miles_per_Gallon&quot;: 14.0, &quot;Cylinders&quot;: 8, &quot;Displacement&quot;: 318.0, &quot;Horsepower&quot;: 150.0, &quot;Weight_in_lbs&quot;: 4096, &quot;Acceleration&quot;: 13.0, &quot;Year&quot;: &quot;1971-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;USA&quot;}, {&quot;Name&quot;: &quot;dodge monaco (sw)&quot;, &quot;Miles_per_Gallon&quot;: 12.0, &quot;Cylinders&quot;: 8, &quot;Displacement&quot;: 383.0, &quot;Horsepower&quot;: 180.0, &quot;Weight_in_lbs&quot;: 4955, &quot;Acceleration&quot;: 11.5, &quot;Year&quot;: &quot;1971-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;USA&quot;}, {&quot;Name&quot;: &quot;ford country squire (sw)&quot;, &quot;Miles_per_Gallon&quot;: 13.0, &quot;Cylinders&quot;: 8, &quot;Displacement&quot;: 400.0, &quot;Horsepower&quot;: 170.0, &quot;Weight_in_lbs&quot;: 4746, &quot;Acceleration&quot;: 12.0, &quot;Year&quot;: &quot;1971-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;USA&quot;}, {&quot;Name&quot;: &quot;pontiac safari (sw)&quot;, &quot;Miles_per_Gallon&quot;: 13.0, &quot;Cylinders&quot;: 8, &quot;Displacement&quot;: 400.0, &quot;Horsepower&quot;: 175.0, &quot;Weight_in_lbs&quot;: 5140, &quot;Acceleration&quot;: 12.0, &quot;Year&quot;: &quot;1971-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;USA&quot;}, {&quot;Name&quot;: &quot;amc hornet sportabout (sw)&quot;, &quot;Miles_per_Gallon&quot;: 18.0, &quot;Cylinders&quot;: 6, &quot;Displacement&quot;: 258.0, &quot;Horsepower&quot;: 110.0, &quot;Weight_in_lbs&quot;: 2962, &quot;Acceleration&quot;: 13.5, &quot;Year&quot;: &quot;1971-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;USA&quot;}, {&quot;Name&quot;: &quot;chevrolet vega (sw)&quot;, &quot;Miles_per_Gallon&quot;: 22.0, &quot;Cylinders&quot;: 4, &quot;Displacement&quot;: 140.0, &quot;Horsepower&quot;: 72.0, &quot;Weight_in_lbs&quot;: 2408, &quot;Acceleration&quot;: 19.0, &quot;Year&quot;: &quot;1971-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;USA&quot;}, {&quot;Name&quot;: &quot;pontiac firebird&quot;, &quot;Miles_per_Gallon&quot;: 19.0, &quot;Cylinders&quot;: 6, &quot;Displacement&quot;: 250.0, &quot;Horsepower&quot;: 100.0, &quot;Weight_in_lbs&quot;: 3282, &quot;Acceleration&quot;: 15.0, &quot;Year&quot;: &quot;1971-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;USA&quot;}, {&quot;Name&quot;: &quot;ford mustang&quot;, &quot;Miles_per_Gallon&quot;: 18.0, &quot;Cylinders&quot;: 6, &quot;Displacement&quot;: 250.0, &quot;Horsepower&quot;: 88.0, &quot;Weight_in_lbs&quot;: 3139, &quot;Acceleration&quot;: 14.5, &quot;Year&quot;: &quot;1971-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;USA&quot;}, {&quot;Name&quot;: &quot;mercury capri 2000&quot;, &quot;Miles_per_Gallon&quot;: 23.0, &quot;Cylinders&quot;: 4, &quot;Displacement&quot;: 122.0, &quot;Horsepower&quot;: 86.0, &quot;Weight_in_lbs&quot;: 2220, &quot;Acceleration&quot;: 14.0, &quot;Year&quot;: &quot;1971-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;USA&quot;}, {&quot;Name&quot;: &quot;opel 1900&quot;, &quot;Miles_per_Gallon&quot;: 28.0, &quot;Cylinders&quot;: 4, &quot;Displacement&quot;: 116.0, &quot;Horsepower&quot;: 90.0, &quot;Weight_in_lbs&quot;: 2123, &quot;Acceleration&quot;: 14.0, &quot;Year&quot;: &quot;1971-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;Europe&quot;}, {&quot;Name&quot;: &quot;peugeot 304&quot;, &quot;Miles_per_Gallon&quot;: 30.0, &quot;Cylinders&quot;: 4, &quot;Displacement&quot;: 79.0, &quot;Horsepower&quot;: 70.0, &quot;Weight_in_lbs&quot;: 2074, &quot;Acceleration&quot;: 19.5, &quot;Year&quot;: &quot;1971-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;Europe&quot;}, {&quot;Name&quot;: &quot;fiat 124b&quot;, &quot;Miles_per_Gallon&quot;: 30.0, &quot;Cylinders&quot;: 4, &quot;Displacement&quot;: 88.0, &quot;Horsepower&quot;: 76.0, &quot;Weight_in_lbs&quot;: 2065, &quot;Acceleration&quot;: 14.5, &quot;Year&quot;: &quot;1971-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;Europe&quot;}, {&quot;Name&quot;: &quot;toyota corolla 1200&quot;, &quot;Miles_per_Gallon&quot;: 31.0, &quot;Cylinders&quot;: 4, &quot;Displacement&quot;: 71.0, &quot;Horsepower&quot;: 65.0, &quot;Weight_in_lbs&quot;: 1773, &quot;Acceleration&quot;: 19.0, &quot;Year&quot;: &quot;1971-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;Japan&quot;}, {&quot;Name&quot;: &quot;datsun 1200&quot;, &quot;Miles_per_Gallon&quot;: 35.0, &quot;Cylinders&quot;: 4, &quot;Displacement&quot;: 72.0, &quot;Horsepower&quot;: 69.0, &quot;Weight_in_lbs&quot;: 1613, &quot;Acceleration&quot;: 18.0, &quot;Year&quot;: &quot;1971-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;Japan&quot;}, {&quot;Name&quot;: &quot;volkswagen model 111&quot;, &quot;Miles_per_Gallon&quot;: 27.0, &quot;Cylinders&quot;: 4, &quot;Displacement&quot;: 97.0, &quot;Horsepower&quot;: 60.0, &quot;Weight_in_lbs&quot;: 1834, &quot;Acceleration&quot;: 19.0, &quot;Year&quot;: &quot;1971-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;Europe&quot;}, {&quot;Name&quot;: &quot;plymouth cricket&quot;, &quot;Miles_per_Gallon&quot;: 26.0, &quot;Cylinders&quot;: 4, &quot;Displacement&quot;: 91.0, &quot;Horsepower&quot;: 70.0, &quot;Weight_in_lbs&quot;: 1955, &quot;Acceleration&quot;: 20.5, &quot;Year&quot;: &quot;1971-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;USA&quot;}, {&quot;Name&quot;: &quot;toyota corona hardtop&quot;, &quot;Miles_per_Gallon&quot;: 24.0, &quot;Cylinders&quot;: 4, &quot;Displacement&quot;: 113.0, &quot;Horsepower&quot;: 95.0, &quot;Weight_in_lbs&quot;: 2278, &quot;Acceleration&quot;: 15.5, &quot;Year&quot;: &quot;1972-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;Japan&quot;}, {&quot;Name&quot;: &quot;dodge colt hardtop&quot;, &quot;Miles_per_Gallon&quot;: 25.0, &quot;Cylinders&quot;: 4, &quot;Displacement&quot;: 97.5, &quot;Horsepower&quot;: 80.0, &quot;Weight_in_lbs&quot;: 2126, &quot;Acceleration&quot;: 17.0, &quot;Year&quot;: &quot;1972-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;USA&quot;}, {&quot;Name&quot;: &quot;volkswagen type 3&quot;, &quot;Miles_per_Gallon&quot;: 23.0, &quot;Cylinders&quot;: 4, &quot;Displacement&quot;: 97.0, &quot;Horsepower&quot;: 54.0, &quot;Weight_in_lbs&quot;: 2254, &quot;Acceleration&quot;: 23.5, &quot;Year&quot;: &quot;1972-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;Europe&quot;}, {&quot;Name&quot;: &quot;chevrolet vega&quot;, &quot;Miles_per_Gallon&quot;: 20.0, &quot;Cylinders&quot;: 4, &quot;Displacement&quot;: 140.0, &quot;Horsepower&quot;: 90.0, &quot;Weight_in_lbs&quot;: 2408, &quot;Acceleration&quot;: 19.5, &quot;Year&quot;: &quot;1972-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;USA&quot;}, {&quot;Name&quot;: &quot;ford pinto runabout&quot;, &quot;Miles_per_Gallon&quot;: 21.0, &quot;Cylinders&quot;: 4, &quot;Displacement&quot;: 122.0, &quot;Horsepower&quot;: 86.0, &quot;Weight_in_lbs&quot;: 2226, &quot;Acceleration&quot;: 16.5, &quot;Year&quot;: &quot;1972-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;USA&quot;}, {&quot;Name&quot;: &quot;chevrolet impala&quot;, &quot;Miles_per_Gallon&quot;: 13.0, &quot;Cylinders&quot;: 8, &quot;Displacement&quot;: 350.0, &quot;Horsepower&quot;: 165.0, &quot;Weight_in_lbs&quot;: 4274, &quot;Acceleration&quot;: 12.0, &quot;Year&quot;: &quot;1972-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;USA&quot;}, {&quot;Name&quot;: &quot;pontiac catalina&quot;, &quot;Miles_per_Gallon&quot;: 14.0, &quot;Cylinders&quot;: 8, &quot;Displacement&quot;: 400.0, &quot;Horsepower&quot;: 175.0, &quot;Weight_in_lbs&quot;: 4385, &quot;Acceleration&quot;: 12.0, &quot;Year&quot;: &quot;1972-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;USA&quot;}, {&quot;Name&quot;: &quot;plymouth fury iii&quot;, &quot;Miles_per_Gallon&quot;: 15.0, &quot;Cylinders&quot;: 8, &quot;Displacement&quot;: 318.0, &quot;Horsepower&quot;: 150.0, &quot;Weight_in_lbs&quot;: 4135, &quot;Acceleration&quot;: 13.5, &quot;Year&quot;: &quot;1972-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;USA&quot;}, {&quot;Name&quot;: &quot;ford galaxie 500&quot;, &quot;Miles_per_Gallon&quot;: 14.0, &quot;Cylinders&quot;: 8, &quot;Displacement&quot;: 351.0, &quot;Horsepower&quot;: 153.0, &quot;Weight_in_lbs&quot;: 4129, &quot;Acceleration&quot;: 13.0, &quot;Year&quot;: &quot;1972-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;USA&quot;}, {&quot;Name&quot;: &quot;amc ambassador sst&quot;, &quot;Miles_per_Gallon&quot;: 17.0, &quot;Cylinders&quot;: 8, &quot;Displacement&quot;: 304.0, &quot;Horsepower&quot;: 150.0, &quot;Weight_in_lbs&quot;: 3672, &quot;Acceleration&quot;: 11.5, &quot;Year&quot;: &quot;1972-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;USA&quot;}, {&quot;Name&quot;: &quot;mercury marquis&quot;, &quot;Miles_per_Gallon&quot;: 11.0, &quot;Cylinders&quot;: 8, &quot;Displacement&quot;: 429.0, &quot;Horsepower&quot;: 208.0, &quot;Weight_in_lbs&quot;: 4633, &quot;Acceleration&quot;: 11.0, &quot;Year&quot;: &quot;1972-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;USA&quot;}, {&quot;Name&quot;: &quot;buick lesabre custom&quot;, &quot;Miles_per_Gallon&quot;: 13.0, &quot;Cylinders&quot;: 8, &quot;Displacement&quot;: 350.0, &quot;Horsepower&quot;: 155.0, &quot;Weight_in_lbs&quot;: 4502, &quot;Acceleration&quot;: 13.5, &quot;Year&quot;: &quot;1972-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;USA&quot;}, {&quot;Name&quot;: &quot;oldsmobile delta 88 royale&quot;, &quot;Miles_per_Gallon&quot;: 12.0, &quot;Cylinders&quot;: 8, &quot;Displacement&quot;: 350.0, &quot;Horsepower&quot;: 160.0, &quot;Weight_in_lbs&quot;: 4456, &quot;Acceleration&quot;: 13.5, &quot;Year&quot;: &quot;1972-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;USA&quot;}, {&quot;Name&quot;: &quot;chrysler newport royal&quot;, &quot;Miles_per_Gallon&quot;: 13.0, &quot;Cylinders&quot;: 8, &quot;Displacement&quot;: 400.0, &quot;Horsepower&quot;: 190.0, &quot;Weight_in_lbs&quot;: 4422, &quot;Acceleration&quot;: 12.5, &quot;Year&quot;: &quot;1972-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;USA&quot;}, {&quot;Name&quot;: &quot;mazda rx2 coupe&quot;, &quot;Miles_per_Gallon&quot;: 19.0, &quot;Cylinders&quot;: 3, &quot;Displacement&quot;: 70.0, &quot;Horsepower&quot;: 97.0, &quot;Weight_in_lbs&quot;: 2330, &quot;Acceleration&quot;: 13.5, &quot;Year&quot;: &quot;1972-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;Japan&quot;}, {&quot;Name&quot;: &quot;amc matador (sw)&quot;, &quot;Miles_per_Gallon&quot;: 15.0, &quot;Cylinders&quot;: 8, &quot;Displacement&quot;: 304.0, &quot;Horsepower&quot;: 150.0, &quot;Weight_in_lbs&quot;: 3892, &quot;Acceleration&quot;: 12.5, &quot;Year&quot;: &quot;1972-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;USA&quot;}, {&quot;Name&quot;: &quot;chevrolet chevelle concours (sw)&quot;, &quot;Miles_per_Gallon&quot;: 13.0, &quot;Cylinders&quot;: 8, &quot;Displacement&quot;: 307.0, &quot;Horsepower&quot;: 130.0, &quot;Weight_in_lbs&quot;: 4098, &quot;Acceleration&quot;: 14.0, &quot;Year&quot;: &quot;1972-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;USA&quot;}, {&quot;Name&quot;: &quot;ford gran torino (sw)&quot;, &quot;Miles_per_Gallon&quot;: 13.0, &quot;Cylinders&quot;: 8, &quot;Displacement&quot;: 302.0, &quot;Horsepower&quot;: 140.0, &quot;Weight_in_lbs&quot;: 4294, &quot;Acceleration&quot;: 16.0, &quot;Year&quot;: &quot;1972-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;USA&quot;}, {&quot;Name&quot;: &quot;plymouth satellite custom (sw)&quot;, &quot;Miles_per_Gallon&quot;: 14.0, &quot;Cylinders&quot;: 8, &quot;Displacement&quot;: 318.0, &quot;Horsepower&quot;: 150.0, &quot;Weight_in_lbs&quot;: 4077, &quot;Acceleration&quot;: 14.0, &quot;Year&quot;: &quot;1972-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;USA&quot;}, {&quot;Name&quot;: &quot;volvo 145e (sw)&quot;, &quot;Miles_per_Gallon&quot;: 18.0, &quot;Cylinders&quot;: 4, &quot;Displacement&quot;: 121.0, &quot;Horsepower&quot;: 112.0, &quot;Weight_in_lbs&quot;: 2933, &quot;Acceleration&quot;: 14.5, &quot;Year&quot;: &quot;1972-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;Europe&quot;}, {&quot;Name&quot;: &quot;volkswagen 411 (sw)&quot;, &quot;Miles_per_Gallon&quot;: 22.0, &quot;Cylinders&quot;: 4, &quot;Displacement&quot;: 121.0, &quot;Horsepower&quot;: 76.0, &quot;Weight_in_lbs&quot;: 2511, &quot;Acceleration&quot;: 18.0, &quot;Year&quot;: &quot;1972-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;Europe&quot;}, {&quot;Name&quot;: &quot;peugeot 504 (sw)&quot;, &quot;Miles_per_Gallon&quot;: 21.0, &quot;Cylinders&quot;: 4, &quot;Displacement&quot;: 120.0, &quot;Horsepower&quot;: 87.0, &quot;Weight_in_lbs&quot;: 2979, &quot;Acceleration&quot;: 19.5, &quot;Year&quot;: &quot;1972-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;Europe&quot;}, {&quot;Name&quot;: &quot;renault 12 (sw)&quot;, &quot;Miles_per_Gallon&quot;: 26.0, &quot;Cylinders&quot;: 4, &quot;Displacement&quot;: 96.0, &quot;Horsepower&quot;: 69.0, &quot;Weight_in_lbs&quot;: 2189, &quot;Acceleration&quot;: 18.0, &quot;Year&quot;: &quot;1972-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;Europe&quot;}, {&quot;Name&quot;: &quot;ford pinto (sw)&quot;, &quot;Miles_per_Gallon&quot;: 22.0, &quot;Cylinders&quot;: 4, &quot;Displacement&quot;: 122.0, &quot;Horsepower&quot;: 86.0, &quot;Weight_in_lbs&quot;: 2395, &quot;Acceleration&quot;: 16.0, &quot;Year&quot;: &quot;1972-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;USA&quot;}, {&quot;Name&quot;: &quot;datsun 510 (sw)&quot;, &quot;Miles_per_Gallon&quot;: 28.0, &quot;Cylinders&quot;: 4, &quot;Displacement&quot;: 97.0, &quot;Horsepower&quot;: 92.0, &quot;Weight_in_lbs&quot;: 2288, &quot;Acceleration&quot;: 17.0, &quot;Year&quot;: &quot;1972-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;Japan&quot;}, {&quot;Name&quot;: &quot;toyouta corona mark ii (sw)&quot;, &quot;Miles_per_Gallon&quot;: 23.0, &quot;Cylinders&quot;: 4, &quot;Displacement&quot;: 120.0, &quot;Horsepower&quot;: 97.0, &quot;Weight_in_lbs&quot;: 2506, &quot;Acceleration&quot;: 14.5, &quot;Year&quot;: &quot;1972-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;Japan&quot;}, {&quot;Name&quot;: &quot;dodge colt (sw)&quot;, &quot;Miles_per_Gallon&quot;: 28.0, &quot;Cylinders&quot;: 4, &quot;Displacement&quot;: 98.0, &quot;Horsepower&quot;: 80.0, &quot;Weight_in_lbs&quot;: 2164, &quot;Acceleration&quot;: 15.0, &quot;Year&quot;: &quot;1972-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;USA&quot;}, {&quot;Name&quot;: &quot;toyota corolla 1600 (sw)&quot;, &quot;Miles_per_Gallon&quot;: 27.0, &quot;Cylinders&quot;: 4, &quot;Displacement&quot;: 97.0, &quot;Horsepower&quot;: 88.0, &quot;Weight_in_lbs&quot;: 2100, &quot;Acceleration&quot;: 16.5, &quot;Year&quot;: &quot;1972-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;Japan&quot;}, {&quot;Name&quot;: &quot;buick century 350&quot;, &quot;Miles_per_Gallon&quot;: 13.0, &quot;Cylinders&quot;: 8, &quot;Displacement&quot;: 350.0, &quot;Horsepower&quot;: 175.0, &quot;Weight_in_lbs&quot;: 4100, &quot;Acceleration&quot;: 13.0, &quot;Year&quot;: &quot;1973-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;USA&quot;}, {&quot;Name&quot;: &quot;amc matador&quot;, &quot;Miles_per_Gallon&quot;: 14.0, &quot;Cylinders&quot;: 8, &quot;Displacement&quot;: 304.0, &quot;Horsepower&quot;: 150.0, &quot;Weight_in_lbs&quot;: 3672, &quot;Acceleration&quot;: 11.5, &quot;Year&quot;: &quot;1973-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;USA&quot;}, {&quot;Name&quot;: &quot;chevrolet malibu&quot;, &quot;Miles_per_Gallon&quot;: 13.0, &quot;Cylinders&quot;: 8, &quot;Displacement&quot;: 350.0, &quot;Horsepower&quot;: 145.0, &quot;Weight_in_lbs&quot;: 3988, &quot;Acceleration&quot;: 13.0, &quot;Year&quot;: &quot;1973-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;USA&quot;}, {&quot;Name&quot;: &quot;ford gran torino&quot;, &quot;Miles_per_Gallon&quot;: 14.0, &quot;Cylinders&quot;: 8, &quot;Displacement&quot;: 302.0, &quot;Horsepower&quot;: 137.0, &quot;Weight_in_lbs&quot;: 4042, &quot;Acceleration&quot;: 14.5, &quot;Year&quot;: &quot;1973-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;USA&quot;}, {&quot;Name&quot;: &quot;dodge coronet custom&quot;, &quot;Miles_per_Gallon&quot;: 15.0, &quot;Cylinders&quot;: 8, &quot;Displacement&quot;: 318.0, &quot;Horsepower&quot;: 150.0, &quot;Weight_in_lbs&quot;: 3777, &quot;Acceleration&quot;: 12.5, &quot;Year&quot;: &quot;1973-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;USA&quot;}, {&quot;Name&quot;: &quot;mercury marquis brougham&quot;, &quot;Miles_per_Gallon&quot;: 12.0, &quot;Cylinders&quot;: 8, &quot;Displacement&quot;: 429.0, &quot;Horsepower&quot;: 198.0, &quot;Weight_in_lbs&quot;: 4952, &quot;Acceleration&quot;: 11.5, &quot;Year&quot;: &quot;1973-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;USA&quot;}, {&quot;Name&quot;: &quot;chevrolet caprice classic&quot;, &quot;Miles_per_Gallon&quot;: 13.0, &quot;Cylinders&quot;: 8, &quot;Displacement&quot;: 400.0, &quot;Horsepower&quot;: 150.0, &quot;Weight_in_lbs&quot;: 4464, &quot;Acceleration&quot;: 12.0, &quot;Year&quot;: &quot;1973-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;USA&quot;}, {&quot;Name&quot;: &quot;ford ltd&quot;, &quot;Miles_per_Gallon&quot;: 13.0, &quot;Cylinders&quot;: 8, &quot;Displacement&quot;: 351.0, &quot;Horsepower&quot;: 158.0, &quot;Weight_in_lbs&quot;: 4363, &quot;Acceleration&quot;: 13.0, &quot;Year&quot;: &quot;1973-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;USA&quot;}, {&quot;Name&quot;: &quot;plymouth fury gran sedan&quot;, &quot;Miles_per_Gallon&quot;: 14.0, &quot;Cylinders&quot;: 8, &quot;Displacement&quot;: 318.0, &quot;Horsepower&quot;: 150.0, &quot;Weight_in_lbs&quot;: 4237, &quot;Acceleration&quot;: 14.5, &quot;Year&quot;: &quot;1973-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;USA&quot;}, {&quot;Name&quot;: &quot;chrysler new yorker brougham&quot;, &quot;Miles_per_Gallon&quot;: 13.0, &quot;Cylinders&quot;: 8, &quot;Displacement&quot;: 440.0, &quot;Horsepower&quot;: 215.0, &quot;Weight_in_lbs&quot;: 4735, &quot;Acceleration&quot;: 11.0, &quot;Year&quot;: &quot;1973-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;USA&quot;}, {&quot;Name&quot;: &quot;buick electra 225 custom&quot;, &quot;Miles_per_Gallon&quot;: 12.0, &quot;Cylinders&quot;: 8, &quot;Displacement&quot;: 455.0, &quot;Horsepower&quot;: 225.0, &quot;Weight_in_lbs&quot;: 4951, &quot;Acceleration&quot;: 11.0, &quot;Year&quot;: &quot;1973-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;USA&quot;}, {&quot;Name&quot;: &quot;amc ambassador brougham&quot;, &quot;Miles_per_Gallon&quot;: 13.0, &quot;Cylinders&quot;: 8, &quot;Displacement&quot;: 360.0, &quot;Horsepower&quot;: 175.0, &quot;Weight_in_lbs&quot;: 3821, &quot;Acceleration&quot;: 11.0, &quot;Year&quot;: &quot;1973-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;USA&quot;}, {&quot;Name&quot;: &quot;plymouth valiant&quot;, &quot;Miles_per_Gallon&quot;: 18.0, &quot;Cylinders&quot;: 6, &quot;Displacement&quot;: 225.0, &quot;Horsepower&quot;: 105.0, &quot;Weight_in_lbs&quot;: 3121, &quot;Acceleration&quot;: 16.5, &quot;Year&quot;: &quot;1973-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;USA&quot;}, {&quot;Name&quot;: &quot;chevrolet nova custom&quot;, &quot;Miles_per_Gallon&quot;: 16.0, &quot;Cylinders&quot;: 6, &quot;Displacement&quot;: 250.0, &quot;Horsepower&quot;: 100.0, &quot;Weight_in_lbs&quot;: 3278, &quot;Acceleration&quot;: 18.0, &quot;Year&quot;: &quot;1973-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;USA&quot;}, {&quot;Name&quot;: &quot;amc hornet&quot;, &quot;Miles_per_Gallon&quot;: 18.0, &quot;Cylinders&quot;: 6, &quot;Displacement&quot;: 232.0, &quot;Horsepower&quot;: 100.0, &quot;Weight_in_lbs&quot;: 2945, &quot;Acceleration&quot;: 16.0, &quot;Year&quot;: &quot;1973-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;USA&quot;}, {&quot;Name&quot;: &quot;ford maverick&quot;, &quot;Miles_per_Gallon&quot;: 18.0, &quot;Cylinders&quot;: 6, &quot;Displacement&quot;: 250.0, &quot;Horsepower&quot;: 88.0, &quot;Weight_in_lbs&quot;: 3021, &quot;Acceleration&quot;: 16.5, &quot;Year&quot;: &quot;1973-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;USA&quot;}, {&quot;Name&quot;: &quot;plymouth duster&quot;, &quot;Miles_per_Gallon&quot;: 23.0, &quot;Cylinders&quot;: 6, &quot;Displacement&quot;: 198.0, &quot;Horsepower&quot;: 95.0, &quot;Weight_in_lbs&quot;: 2904, &quot;Acceleration&quot;: 16.0, &quot;Year&quot;: &quot;1973-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;USA&quot;}, {&quot;Name&quot;: &quot;volkswagen super beetle&quot;, &quot;Miles_per_Gallon&quot;: 26.0, &quot;Cylinders&quot;: 4, &quot;Displacement&quot;: 97.0, &quot;Horsepower&quot;: 46.0, &quot;Weight_in_lbs&quot;: 1950, &quot;Acceleration&quot;: 21.0, &quot;Year&quot;: &quot;1973-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;Europe&quot;}, {&quot;Name&quot;: &quot;chevrolet impala&quot;, &quot;Miles_per_Gallon&quot;: 11.0, &quot;Cylinders&quot;: 8, &quot;Displacement&quot;: 400.0, &quot;Horsepower&quot;: 150.0, &quot;Weight_in_lbs&quot;: 4997, &quot;Acceleration&quot;: 14.0, &quot;Year&quot;: &quot;1973-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;USA&quot;}, {&quot;Name&quot;: &quot;ford country&quot;, &quot;Miles_per_Gallon&quot;: 12.0, &quot;Cylinders&quot;: 8, &quot;Displacement&quot;: 400.0, &quot;Horsepower&quot;: 167.0, &quot;Weight_in_lbs&quot;: 4906, &quot;Acceleration&quot;: 12.5, &quot;Year&quot;: &quot;1973-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;USA&quot;}, {&quot;Name&quot;: &quot;plymouth custom suburb&quot;, &quot;Miles_per_Gallon&quot;: 13.0, &quot;Cylinders&quot;: 8, &quot;Displacement&quot;: 360.0, &quot;Horsepower&quot;: 170.0, &quot;Weight_in_lbs&quot;: 4654, &quot;Acceleration&quot;: 13.0, &quot;Year&quot;: &quot;1973-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;USA&quot;}, {&quot;Name&quot;: &quot;oldsmobile vista cruiser&quot;, &quot;Miles_per_Gallon&quot;: 12.0, &quot;Cylinders&quot;: 8, &quot;Displacement&quot;: 350.0, &quot;Horsepower&quot;: 180.0, &quot;Weight_in_lbs&quot;: 4499, &quot;Acceleration&quot;: 12.5, &quot;Year&quot;: &quot;1973-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;USA&quot;}, {&quot;Name&quot;: &quot;amc gremlin&quot;, &quot;Miles_per_Gallon&quot;: 18.0, &quot;Cylinders&quot;: 6, &quot;Displacement&quot;: 232.0, &quot;Horsepower&quot;: 100.0, &quot;Weight_in_lbs&quot;: 2789, &quot;Acceleration&quot;: 15.0, &quot;Year&quot;: &quot;1973-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;USA&quot;}, {&quot;Name&quot;: &quot;toyota carina&quot;, &quot;Miles_per_Gallon&quot;: 20.0, &quot;Cylinders&quot;: 4, &quot;Displacement&quot;: 97.0, &quot;Horsepower&quot;: 88.0, &quot;Weight_in_lbs&quot;: 2279, &quot;Acceleration&quot;: 19.0, &quot;Year&quot;: &quot;1973-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;Japan&quot;}, {&quot;Name&quot;: &quot;chevrolet vega&quot;, &quot;Miles_per_Gallon&quot;: 21.0, &quot;Cylinders&quot;: 4, &quot;Displacement&quot;: 140.0, &quot;Horsepower&quot;: 72.0, &quot;Weight_in_lbs&quot;: 2401, &quot;Acceleration&quot;: 19.5, &quot;Year&quot;: &quot;1973-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;USA&quot;}, {&quot;Name&quot;: &quot;datsun 610&quot;, &quot;Miles_per_Gallon&quot;: 22.0, &quot;Cylinders&quot;: 4, &quot;Displacement&quot;: 108.0, &quot;Horsepower&quot;: 94.0, &quot;Weight_in_lbs&quot;: 2379, &quot;Acceleration&quot;: 16.5, &quot;Year&quot;: &quot;1973-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;Japan&quot;}, {&quot;Name&quot;: &quot;maxda rx3&quot;, &quot;Miles_per_Gallon&quot;: 18.0, &quot;Cylinders&quot;: 3, &quot;Displacement&quot;: 70.0, &quot;Horsepower&quot;: 90.0, &quot;Weight_in_lbs&quot;: 2124, &quot;Acceleration&quot;: 13.5, &quot;Year&quot;: &quot;1973-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;Japan&quot;}, {&quot;Name&quot;: &quot;ford pinto&quot;, &quot;Miles_per_Gallon&quot;: 19.0, &quot;Cylinders&quot;: 4, &quot;Displacement&quot;: 122.0, &quot;Horsepower&quot;: 85.0, &quot;Weight_in_lbs&quot;: 2310, &quot;Acceleration&quot;: 18.5, &quot;Year&quot;: &quot;1973-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;USA&quot;}, {&quot;Name&quot;: &quot;mercury capri v6&quot;, &quot;Miles_per_Gallon&quot;: 21.0, &quot;Cylinders&quot;: 6, &quot;Displacement&quot;: 155.0, &quot;Horsepower&quot;: 107.0, &quot;Weight_in_lbs&quot;: 2472, &quot;Acceleration&quot;: 14.0, &quot;Year&quot;: &quot;1973-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;USA&quot;}, {&quot;Name&quot;: &quot;fiat 124 sport coupe&quot;, &quot;Miles_per_Gallon&quot;: 26.0, &quot;Cylinders&quot;: 4, &quot;Displacement&quot;: 98.0, &quot;Horsepower&quot;: 90.0, &quot;Weight_in_lbs&quot;: 2265, &quot;Acceleration&quot;: 15.5, &quot;Year&quot;: &quot;1973-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;Europe&quot;}, {&quot;Name&quot;: &quot;chevrolet monte carlo s&quot;, &quot;Miles_per_Gallon&quot;: 15.0, &quot;Cylinders&quot;: 8, &quot;Displacement&quot;: 350.0, &quot;Horsepower&quot;: 145.0, &quot;Weight_in_lbs&quot;: 4082, &quot;Acceleration&quot;: 13.0, &quot;Year&quot;: &quot;1973-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;USA&quot;}, {&quot;Name&quot;: &quot;pontiac grand prix&quot;, &quot;Miles_per_Gallon&quot;: 16.0, &quot;Cylinders&quot;: 8, &quot;Displacement&quot;: 400.0, &quot;Horsepower&quot;: 230.0, &quot;Weight_in_lbs&quot;: 4278, &quot;Acceleration&quot;: 9.5, &quot;Year&quot;: &quot;1973-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;USA&quot;}, {&quot;Name&quot;: &quot;fiat 128&quot;, &quot;Miles_per_Gallon&quot;: 29.0, &quot;Cylinders&quot;: 4, &quot;Displacement&quot;: 68.0, &quot;Horsepower&quot;: 49.0, &quot;Weight_in_lbs&quot;: 1867, &quot;Acceleration&quot;: 19.5, &quot;Year&quot;: &quot;1973-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;Europe&quot;}, {&quot;Name&quot;: &quot;opel manta&quot;, &quot;Miles_per_Gallon&quot;: 24.0, &quot;Cylinders&quot;: 4, &quot;Displacement&quot;: 116.0, &quot;Horsepower&quot;: 75.0, &quot;Weight_in_lbs&quot;: 2158, &quot;Acceleration&quot;: 15.5, &quot;Year&quot;: &quot;1973-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;Europe&quot;}, {&quot;Name&quot;: &quot;audi 100ls&quot;, &quot;Miles_per_Gallon&quot;: 20.0, &quot;Cylinders&quot;: 4, &quot;Displacement&quot;: 114.0, &quot;Horsepower&quot;: 91.0, &quot;Weight_in_lbs&quot;: 2582, &quot;Acceleration&quot;: 14.0, &quot;Year&quot;: &quot;1973-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;Europe&quot;}, {&quot;Name&quot;: &quot;volvo 144ea&quot;, &quot;Miles_per_Gallon&quot;: 19.0, &quot;Cylinders&quot;: 4, &quot;Displacement&quot;: 121.0, &quot;Horsepower&quot;: 112.0, &quot;Weight_in_lbs&quot;: 2868, &quot;Acceleration&quot;: 15.5, &quot;Year&quot;: &quot;1973-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;Europe&quot;}, {&quot;Name&quot;: &quot;dodge dart custom&quot;, &quot;Miles_per_Gallon&quot;: 15.0, &quot;Cylinders&quot;: 8, &quot;Displacement&quot;: 318.0, &quot;Horsepower&quot;: 150.0, &quot;Weight_in_lbs&quot;: 3399, &quot;Acceleration&quot;: 11.0, &quot;Year&quot;: &quot;1973-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;USA&quot;}, {&quot;Name&quot;: &quot;saab 99le&quot;, &quot;Miles_per_Gallon&quot;: 24.0, &quot;Cylinders&quot;: 4, &quot;Displacement&quot;: 121.0, &quot;Horsepower&quot;: 110.0, &quot;Weight_in_lbs&quot;: 2660, &quot;Acceleration&quot;: 14.0, &quot;Year&quot;: &quot;1973-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;Europe&quot;}, {&quot;Name&quot;: &quot;toyota mark ii&quot;, &quot;Miles_per_Gallon&quot;: 20.0, &quot;Cylinders&quot;: 6, &quot;Displacement&quot;: 156.0, &quot;Horsepower&quot;: 122.0, &quot;Weight_in_lbs&quot;: 2807, &quot;Acceleration&quot;: 13.5, &quot;Year&quot;: &quot;1973-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;Japan&quot;}, {&quot;Name&quot;: &quot;oldsmobile omega&quot;, &quot;Miles_per_Gallon&quot;: 11.0, &quot;Cylinders&quot;: 8, &quot;Displacement&quot;: 350.0, &quot;Horsepower&quot;: 180.0, &quot;Weight_in_lbs&quot;: 3664, &quot;Acceleration&quot;: 11.0, &quot;Year&quot;: &quot;1973-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;USA&quot;}, {&quot;Name&quot;: &quot;plymouth duster&quot;, &quot;Miles_per_Gallon&quot;: 20.0, &quot;Cylinders&quot;: 6, &quot;Displacement&quot;: 198.0, &quot;Horsepower&quot;: 95.0, &quot;Weight_in_lbs&quot;: 3102, &quot;Acceleration&quot;: 16.5, &quot;Year&quot;: &quot;1974-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;USA&quot;}, {&quot;Name&quot;: &quot;ford maverick&quot;, &quot;Miles_per_Gallon&quot;: 21.0, &quot;Cylinders&quot;: 6, &quot;Displacement&quot;: 200.0, &quot;Horsepower&quot;: null, &quot;Weight_in_lbs&quot;: 2875, &quot;Acceleration&quot;: 17.0, &quot;Year&quot;: &quot;1974-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;USA&quot;}, {&quot;Name&quot;: &quot;amc hornet&quot;, &quot;Miles_per_Gallon&quot;: 19.0, &quot;Cylinders&quot;: 6, &quot;Displacement&quot;: 232.0, &quot;Horsepower&quot;: 100.0, &quot;Weight_in_lbs&quot;: 2901, &quot;Acceleration&quot;: 16.0, &quot;Year&quot;: &quot;1974-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;USA&quot;}, {&quot;Name&quot;: &quot;chevrolet nova&quot;, &quot;Miles_per_Gallon&quot;: 15.0, &quot;Cylinders&quot;: 6, &quot;Displacement&quot;: 250.0, &quot;Horsepower&quot;: 100.0, &quot;Weight_in_lbs&quot;: 3336, &quot;Acceleration&quot;: 17.0, &quot;Year&quot;: &quot;1974-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;USA&quot;}, {&quot;Name&quot;: &quot;datsun b210&quot;, &quot;Miles_per_Gallon&quot;: 31.0, &quot;Cylinders&quot;: 4, &quot;Displacement&quot;: 79.0, &quot;Horsepower&quot;: 67.0, &quot;Weight_in_lbs&quot;: 1950, &quot;Acceleration&quot;: 19.0, &quot;Year&quot;: &quot;1974-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;Japan&quot;}, {&quot;Name&quot;: &quot;ford pinto&quot;, &quot;Miles_per_Gallon&quot;: 26.0, &quot;Cylinders&quot;: 4, &quot;Displacement&quot;: 122.0, &quot;Horsepower&quot;: 80.0, &quot;Weight_in_lbs&quot;: 2451, &quot;Acceleration&quot;: 16.5, &quot;Year&quot;: &quot;1974-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;USA&quot;}, {&quot;Name&quot;: &quot;toyota corolla 1200&quot;, &quot;Miles_per_Gallon&quot;: 32.0, &quot;Cylinders&quot;: 4, &quot;Displacement&quot;: 71.0, &quot;Horsepower&quot;: 65.0, &quot;Weight_in_lbs&quot;: 1836, &quot;Acceleration&quot;: 21.0, &quot;Year&quot;: &quot;1974-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;Japan&quot;}, {&quot;Name&quot;: &quot;chevrolet vega&quot;, &quot;Miles_per_Gallon&quot;: 25.0, &quot;Cylinders&quot;: 4, &quot;Displacement&quot;: 140.0, &quot;Horsepower&quot;: 75.0, &quot;Weight_in_lbs&quot;: 2542, &quot;Acceleration&quot;: 17.0, &quot;Year&quot;: &quot;1974-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;USA&quot;}, {&quot;Name&quot;: &quot;chevrolet chevelle malibu classic&quot;, &quot;Miles_per_Gallon&quot;: 16.0, &quot;Cylinders&quot;: 6, &quot;Displacement&quot;: 250.0, &quot;Horsepower&quot;: 100.0, &quot;Weight_in_lbs&quot;: 3781, &quot;Acceleration&quot;: 17.0, &quot;Year&quot;: &quot;1974-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;USA&quot;}, {&quot;Name&quot;: &quot;amc matador&quot;, &quot;Miles_per_Gallon&quot;: 16.0, &quot;Cylinders&quot;: 6, &quot;Displacement&quot;: 258.0, &quot;Horsepower&quot;: 110.0, &quot;Weight_in_lbs&quot;: 3632, &quot;Acceleration&quot;: 18.0, &quot;Year&quot;: &quot;1974-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;USA&quot;}, {&quot;Name&quot;: &quot;plymouth satellite sebring&quot;, &quot;Miles_per_Gallon&quot;: 18.0, &quot;Cylinders&quot;: 6, &quot;Displacement&quot;: 225.0, &quot;Horsepower&quot;: 105.0, &quot;Weight_in_lbs&quot;: 3613, &quot;Acceleration&quot;: 16.5, &quot;Year&quot;: &quot;1974-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;USA&quot;}, {&quot;Name&quot;: &quot;ford gran torino&quot;, &quot;Miles_per_Gallon&quot;: 16.0, &quot;Cylinders&quot;: 8, &quot;Displacement&quot;: 302.0, &quot;Horsepower&quot;: 140.0, &quot;Weight_in_lbs&quot;: 4141, &quot;Acceleration&quot;: 14.0, &quot;Year&quot;: &quot;1974-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;USA&quot;}, {&quot;Name&quot;: &quot;buick century luxus (sw)&quot;, &quot;Miles_per_Gallon&quot;: 13.0, &quot;Cylinders&quot;: 8, &quot;Displacement&quot;: 350.0, &quot;Horsepower&quot;: 150.0, &quot;Weight_in_lbs&quot;: 4699, &quot;Acceleration&quot;: 14.5, &quot;Year&quot;: &quot;1974-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;USA&quot;}, {&quot;Name&quot;: &quot;dodge coronet custom (sw)&quot;, &quot;Miles_per_Gallon&quot;: 14.0, &quot;Cylinders&quot;: 8, &quot;Displacement&quot;: 318.0, &quot;Horsepower&quot;: 150.0, &quot;Weight_in_lbs&quot;: 4457, &quot;Acceleration&quot;: 13.5, &quot;Year&quot;: &quot;1974-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;USA&quot;}, {&quot;Name&quot;: &quot;ford gran torino (sw)&quot;, &quot;Miles_per_Gallon&quot;: 14.0, &quot;Cylinders&quot;: 8, &quot;Displacement&quot;: 302.0, &quot;Horsepower&quot;: 140.0, &quot;Weight_in_lbs&quot;: 4638, &quot;Acceleration&quot;: 16.0, &quot;Year&quot;: &quot;1974-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;USA&quot;}, {&quot;Name&quot;: &quot;amc matador (sw)&quot;, &quot;Miles_per_Gallon&quot;: 14.0, &quot;Cylinders&quot;: 8, &quot;Displacement&quot;: 304.0, &quot;Horsepower&quot;: 150.0, &quot;Weight_in_lbs&quot;: 4257, &quot;Acceleration&quot;: 15.5, &quot;Year&quot;: &quot;1974-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;USA&quot;}, {&quot;Name&quot;: &quot;audi fox&quot;, &quot;Miles_per_Gallon&quot;: 29.0, &quot;Cylinders&quot;: 4, &quot;Displacement&quot;: 98.0, &quot;Horsepower&quot;: 83.0, &quot;Weight_in_lbs&quot;: 2219, &quot;Acceleration&quot;: 16.5, &quot;Year&quot;: &quot;1974-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;Europe&quot;}, {&quot;Name&quot;: &quot;volkswagen dasher&quot;, &quot;Miles_per_Gallon&quot;: 26.0, &quot;Cylinders&quot;: 4, &quot;Displacement&quot;: 79.0, &quot;Horsepower&quot;: 67.0, &quot;Weight_in_lbs&quot;: 1963, &quot;Acceleration&quot;: 15.5, &quot;Year&quot;: &quot;1974-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;Europe&quot;}, {&quot;Name&quot;: &quot;opel manta&quot;, &quot;Miles_per_Gallon&quot;: 26.0, &quot;Cylinders&quot;: 4, &quot;Displacement&quot;: 97.0, &quot;Horsepower&quot;: 78.0, &quot;Weight_in_lbs&quot;: 2300, &quot;Acceleration&quot;: 14.5, &quot;Year&quot;: &quot;1974-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;Europe&quot;}, {&quot;Name&quot;: &quot;toyota corona&quot;, &quot;Miles_per_Gallon&quot;: 31.0, &quot;Cylinders&quot;: 4, &quot;Displacement&quot;: 76.0, &quot;Horsepower&quot;: 52.0, &quot;Weight_in_lbs&quot;: 1649, &quot;Acceleration&quot;: 16.5, &quot;Year&quot;: &quot;1974-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;Japan&quot;}, {&quot;Name&quot;: &quot;datsun 710&quot;, &quot;Miles_per_Gallon&quot;: 32.0, &quot;Cylinders&quot;: 4, &quot;Displacement&quot;: 83.0, &quot;Horsepower&quot;: 61.0, &quot;Weight_in_lbs&quot;: 2003, &quot;Acceleration&quot;: 19.0, &quot;Year&quot;: &quot;1974-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;Japan&quot;}, {&quot;Name&quot;: &quot;dodge colt&quot;, &quot;Miles_per_Gallon&quot;: 28.0, &quot;Cylinders&quot;: 4, &quot;Displacement&quot;: 90.0, &quot;Horsepower&quot;: 75.0, &quot;Weight_in_lbs&quot;: 2125, &quot;Acceleration&quot;: 14.5, &quot;Year&quot;: &quot;1974-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;USA&quot;}, {&quot;Name&quot;: &quot;fiat 128&quot;, &quot;Miles_per_Gallon&quot;: 24.0, &quot;Cylinders&quot;: 4, &quot;Displacement&quot;: 90.0, &quot;Horsepower&quot;: 75.0, &quot;Weight_in_lbs&quot;: 2108, &quot;Acceleration&quot;: 15.5, &quot;Year&quot;: &quot;1974-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;Europe&quot;}, {&quot;Name&quot;: &quot;fiat 124 tc&quot;, &quot;Miles_per_Gallon&quot;: 26.0, &quot;Cylinders&quot;: 4, &quot;Displacement&quot;: 116.0, &quot;Horsepower&quot;: 75.0, &quot;Weight_in_lbs&quot;: 2246, &quot;Acceleration&quot;: 14.0, &quot;Year&quot;: &quot;1974-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;Europe&quot;}, {&quot;Name&quot;: &quot;honda civic&quot;, &quot;Miles_per_Gallon&quot;: 24.0, &quot;Cylinders&quot;: 4, &quot;Displacement&quot;: 120.0, &quot;Horsepower&quot;: 97.0, &quot;Weight_in_lbs&quot;: 2489, &quot;Acceleration&quot;: 15.0, &quot;Year&quot;: &quot;1974-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;Japan&quot;}, {&quot;Name&quot;: &quot;subaru&quot;, &quot;Miles_per_Gallon&quot;: 26.0, &quot;Cylinders&quot;: 4, &quot;Displacement&quot;: 108.0, &quot;Horsepower&quot;: 93.0, &quot;Weight_in_lbs&quot;: 2391, &quot;Acceleration&quot;: 15.5, &quot;Year&quot;: &quot;1974-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;Japan&quot;}, {&quot;Name&quot;: &quot;fiat x1.9&quot;, &quot;Miles_per_Gallon&quot;: 31.0, &quot;Cylinders&quot;: 4, &quot;Displacement&quot;: 79.0, &quot;Horsepower&quot;: 67.0, &quot;Weight_in_lbs&quot;: 2000, &quot;Acceleration&quot;: 16.0, &quot;Year&quot;: &quot;1974-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;Europe&quot;}, {&quot;Name&quot;: &quot;plymouth valiant custom&quot;, &quot;Miles_per_Gallon&quot;: 19.0, &quot;Cylinders&quot;: 6, &quot;Displacement&quot;: 225.0, &quot;Horsepower&quot;: 95.0, &quot;Weight_in_lbs&quot;: 3264, &quot;Acceleration&quot;: 16.0, &quot;Year&quot;: &quot;1975-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;USA&quot;}, {&quot;Name&quot;: &quot;chevrolet nova&quot;, &quot;Miles_per_Gallon&quot;: 18.0, &quot;Cylinders&quot;: 6, &quot;Displacement&quot;: 250.0, &quot;Horsepower&quot;: 105.0, &quot;Weight_in_lbs&quot;: 3459, &quot;Acceleration&quot;: 16.0, &quot;Year&quot;: &quot;1975-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;USA&quot;}, {&quot;Name&quot;: &quot;mercury monarch&quot;, &quot;Miles_per_Gallon&quot;: 15.0, &quot;Cylinders&quot;: 6, &quot;Displacement&quot;: 250.0, &quot;Horsepower&quot;: 72.0, &quot;Weight_in_lbs&quot;: 3432, &quot;Acceleration&quot;: 21.0, &quot;Year&quot;: &quot;1975-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;USA&quot;}, {&quot;Name&quot;: &quot;ford maverick&quot;, &quot;Miles_per_Gallon&quot;: 15.0, &quot;Cylinders&quot;: 6, &quot;Displacement&quot;: 250.0, &quot;Horsepower&quot;: 72.0, &quot;Weight_in_lbs&quot;: 3158, &quot;Acceleration&quot;: 19.5, &quot;Year&quot;: &quot;1975-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;USA&quot;}, {&quot;Name&quot;: &quot;pontiac catalina&quot;, &quot;Miles_per_Gallon&quot;: 16.0, &quot;Cylinders&quot;: 8, &quot;Displacement&quot;: 400.0, &quot;Horsepower&quot;: 170.0, &quot;Weight_in_lbs&quot;: 4668, &quot;Acceleration&quot;: 11.5, &quot;Year&quot;: &quot;1975-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;USA&quot;}, {&quot;Name&quot;: &quot;chevrolet bel air&quot;, &quot;Miles_per_Gallon&quot;: 15.0, &quot;Cylinders&quot;: 8, &quot;Displacement&quot;: 350.0, &quot;Horsepower&quot;: 145.0, &quot;Weight_in_lbs&quot;: 4440, &quot;Acceleration&quot;: 14.0, &quot;Year&quot;: &quot;1975-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;USA&quot;}, {&quot;Name&quot;: &quot;plymouth grand fury&quot;, &quot;Miles_per_Gallon&quot;: 16.0, &quot;Cylinders&quot;: 8, &quot;Displacement&quot;: 318.0, &quot;Horsepower&quot;: 150.0, &quot;Weight_in_lbs&quot;: 4498, &quot;Acceleration&quot;: 14.5, &quot;Year&quot;: &quot;1975-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;USA&quot;}, {&quot;Name&quot;: &quot;ford ltd&quot;, &quot;Miles_per_Gallon&quot;: 14.0, &quot;Cylinders&quot;: 8, &quot;Displacement&quot;: 351.0, &quot;Horsepower&quot;: 148.0, &quot;Weight_in_lbs&quot;: 4657, &quot;Acceleration&quot;: 13.5, &quot;Year&quot;: &quot;1975-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;USA&quot;}, {&quot;Name&quot;: &quot;buick century&quot;, &quot;Miles_per_Gallon&quot;: 17.0, &quot;Cylinders&quot;: 6, &quot;Displacement&quot;: 231.0, &quot;Horsepower&quot;: 110.0, &quot;Weight_in_lbs&quot;: 3907, &quot;Acceleration&quot;: 21.0, &quot;Year&quot;: &quot;1975-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;USA&quot;}, {&quot;Name&quot;: &quot;chevroelt chevelle malibu&quot;, &quot;Miles_per_Gallon&quot;: 16.0, &quot;Cylinders&quot;: 6, &quot;Displacement&quot;: 250.0, &quot;Horsepower&quot;: 105.0, &quot;Weight_in_lbs&quot;: 3897, &quot;Acceleration&quot;: 18.5, &quot;Year&quot;: &quot;1975-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;USA&quot;}, {&quot;Name&quot;: &quot;amc matador&quot;, &quot;Miles_per_Gallon&quot;: 15.0, &quot;Cylinders&quot;: 6, &quot;Displacement&quot;: 258.0, &quot;Horsepower&quot;: 110.0, &quot;Weight_in_lbs&quot;: 3730, &quot;Acceleration&quot;: 19.0, &quot;Year&quot;: &quot;1975-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;USA&quot;}, {&quot;Name&quot;: &quot;plymouth fury&quot;, &quot;Miles_per_Gallon&quot;: 18.0, &quot;Cylinders&quot;: 6, &quot;Displacement&quot;: 225.0, &quot;Horsepower&quot;: 95.0, &quot;Weight_in_lbs&quot;: 3785, &quot;Acceleration&quot;: 19.0, &quot;Year&quot;: &quot;1975-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;USA&quot;}, {&quot;Name&quot;: &quot;buick skyhawk&quot;, &quot;Miles_per_Gallon&quot;: 21.0, &quot;Cylinders&quot;: 6, &quot;Displacement&quot;: 231.0, &quot;Horsepower&quot;: 110.0, &quot;Weight_in_lbs&quot;: 3039, &quot;Acceleration&quot;: 15.0, &quot;Year&quot;: &quot;1975-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;USA&quot;}, {&quot;Name&quot;: &quot;chevrolet monza 2+2&quot;, &quot;Miles_per_Gallon&quot;: 20.0, &quot;Cylinders&quot;: 8, &quot;Displacement&quot;: 262.0, &quot;Horsepower&quot;: 110.0, &quot;Weight_in_lbs&quot;: 3221, &quot;Acceleration&quot;: 13.5, &quot;Year&quot;: &quot;1975-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;USA&quot;}, {&quot;Name&quot;: &quot;ford mustang ii&quot;, &quot;Miles_per_Gallon&quot;: 13.0, &quot;Cylinders&quot;: 8, &quot;Displacement&quot;: 302.0, &quot;Horsepower&quot;: 129.0, &quot;Weight_in_lbs&quot;: 3169, &quot;Acceleration&quot;: 12.0, &quot;Year&quot;: &quot;1975-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;USA&quot;}, {&quot;Name&quot;: &quot;toyota corolla&quot;, &quot;Miles_per_Gallon&quot;: 29.0, &quot;Cylinders&quot;: 4, &quot;Displacement&quot;: 97.0, &quot;Horsepower&quot;: 75.0, &quot;Weight_in_lbs&quot;: 2171, &quot;Acceleration&quot;: 16.0, &quot;Year&quot;: &quot;1975-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;Japan&quot;}, {&quot;Name&quot;: &quot;ford pinto&quot;, &quot;Miles_per_Gallon&quot;: 23.0, &quot;Cylinders&quot;: 4, &quot;Displacement&quot;: 140.0, &quot;Horsepower&quot;: 83.0, &quot;Weight_in_lbs&quot;: 2639, &quot;Acceleration&quot;: 17.0, &quot;Year&quot;: &quot;1975-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;USA&quot;}, {&quot;Name&quot;: &quot;amc gremlin&quot;, &quot;Miles_per_Gallon&quot;: 20.0, &quot;Cylinders&quot;: 6, &quot;Displacement&quot;: 232.0, &quot;Horsepower&quot;: 100.0, &quot;Weight_in_lbs&quot;: 2914, &quot;Acceleration&quot;: 16.0, &quot;Year&quot;: &quot;1975-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;USA&quot;}, {&quot;Name&quot;: &quot;pontiac astro&quot;, &quot;Miles_per_Gallon&quot;: 23.0, &quot;Cylinders&quot;: 4, &quot;Displacement&quot;: 140.0, &quot;Horsepower&quot;: 78.0, &quot;Weight_in_lbs&quot;: 2592, &quot;Acceleration&quot;: 18.5, &quot;Year&quot;: &quot;1975-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;USA&quot;}, {&quot;Name&quot;: &quot;toyota corona&quot;, &quot;Miles_per_Gallon&quot;: 24.0, &quot;Cylinders&quot;: 4, &quot;Displacement&quot;: 134.0, &quot;Horsepower&quot;: 96.0, &quot;Weight_in_lbs&quot;: 2702, &quot;Acceleration&quot;: 13.5, &quot;Year&quot;: &quot;1975-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;Japan&quot;}, {&quot;Name&quot;: &quot;volkswagen dasher&quot;, &quot;Miles_per_Gallon&quot;: 25.0, &quot;Cylinders&quot;: 4, &quot;Displacement&quot;: 90.0, &quot;Horsepower&quot;: 71.0, &quot;Weight_in_lbs&quot;: 2223, &quot;Acceleration&quot;: 16.5, &quot;Year&quot;: &quot;1975-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;Europe&quot;}, {&quot;Name&quot;: &quot;datsun 710&quot;, &quot;Miles_per_Gallon&quot;: 24.0, &quot;Cylinders&quot;: 4, &quot;Displacement&quot;: 119.0, &quot;Horsepower&quot;: 97.0, &quot;Weight_in_lbs&quot;: 2545, &quot;Acceleration&quot;: 17.0, &quot;Year&quot;: &quot;1975-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;Japan&quot;}, {&quot;Name&quot;: &quot;ford pinto&quot;, &quot;Miles_per_Gallon&quot;: 18.0, &quot;Cylinders&quot;: 6, &quot;Displacement&quot;: 171.0, &quot;Horsepower&quot;: 97.0, &quot;Weight_in_lbs&quot;: 2984, &quot;Acceleration&quot;: 14.5, &quot;Year&quot;: &quot;1975-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;USA&quot;}, {&quot;Name&quot;: &quot;volkswagen rabbit&quot;, &quot;Miles_per_Gallon&quot;: 29.0, &quot;Cylinders&quot;: 4, &quot;Displacement&quot;: 90.0, &quot;Horsepower&quot;: 70.0, &quot;Weight_in_lbs&quot;: 1937, &quot;Acceleration&quot;: 14.0, &quot;Year&quot;: &quot;1975-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;Europe&quot;}, {&quot;Name&quot;: &quot;amc pacer&quot;, &quot;Miles_per_Gallon&quot;: 19.0, &quot;Cylinders&quot;: 6, &quot;Displacement&quot;: 232.0, &quot;Horsepower&quot;: 90.0, &quot;Weight_in_lbs&quot;: 3211, &quot;Acceleration&quot;: 17.0, &quot;Year&quot;: &quot;1975-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;USA&quot;}, {&quot;Name&quot;: &quot;audi 100ls&quot;, &quot;Miles_per_Gallon&quot;: 23.0, &quot;Cylinders&quot;: 4, &quot;Displacement&quot;: 115.0, &quot;Horsepower&quot;: 95.0, &quot;Weight_in_lbs&quot;: 2694, &quot;Acceleration&quot;: 15.0, &quot;Year&quot;: &quot;1975-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;Europe&quot;}, {&quot;Name&quot;: &quot;peugeot 504&quot;, &quot;Miles_per_Gallon&quot;: 23.0, &quot;Cylinders&quot;: 4, &quot;Displacement&quot;: 120.0, &quot;Horsepower&quot;: 88.0, &quot;Weight_in_lbs&quot;: 2957, &quot;Acceleration&quot;: 17.0, &quot;Year&quot;: &quot;1975-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;Europe&quot;}, {&quot;Name&quot;: &quot;volvo 244dl&quot;, &quot;Miles_per_Gallon&quot;: 22.0, &quot;Cylinders&quot;: 4, &quot;Displacement&quot;: 121.0, &quot;Horsepower&quot;: 98.0, &quot;Weight_in_lbs&quot;: 2945, &quot;Acceleration&quot;: 14.5, &quot;Year&quot;: &quot;1975-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;Europe&quot;}, {&quot;Name&quot;: &quot;saab 99le&quot;, &quot;Miles_per_Gallon&quot;: 25.0, &quot;Cylinders&quot;: 4, &quot;Displacement&quot;: 121.0, &quot;Horsepower&quot;: 115.0, &quot;Weight_in_lbs&quot;: 2671, &quot;Acceleration&quot;: 13.5, &quot;Year&quot;: &quot;1975-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;Europe&quot;}, {&quot;Name&quot;: &quot;honda civic cvcc&quot;, &quot;Miles_per_Gallon&quot;: 33.0, &quot;Cylinders&quot;: 4, &quot;Displacement&quot;: 91.0, &quot;Horsepower&quot;: 53.0, &quot;Weight_in_lbs&quot;: 1795, &quot;Acceleration&quot;: 17.5, &quot;Year&quot;: &quot;1975-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;Japan&quot;}, {&quot;Name&quot;: &quot;fiat 131&quot;, &quot;Miles_per_Gallon&quot;: 28.0, &quot;Cylinders&quot;: 4, &quot;Displacement&quot;: 107.0, &quot;Horsepower&quot;: 86.0, &quot;Weight_in_lbs&quot;: 2464, &quot;Acceleration&quot;: 15.5, &quot;Year&quot;: &quot;1976-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;Europe&quot;}, {&quot;Name&quot;: &quot;opel 1900&quot;, &quot;Miles_per_Gallon&quot;: 25.0, &quot;Cylinders&quot;: 4, &quot;Displacement&quot;: 116.0, &quot;Horsepower&quot;: 81.0, &quot;Weight_in_lbs&quot;: 2220, &quot;Acceleration&quot;: 16.9, &quot;Year&quot;: &quot;1976-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;Europe&quot;}, {&quot;Name&quot;: &quot;capri ii&quot;, &quot;Miles_per_Gallon&quot;: 25.0, &quot;Cylinders&quot;: 4, &quot;Displacement&quot;: 140.0, &quot;Horsepower&quot;: 92.0, &quot;Weight_in_lbs&quot;: 2572, &quot;Acceleration&quot;: 14.9, &quot;Year&quot;: &quot;1976-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;USA&quot;}, {&quot;Name&quot;: &quot;dodge colt&quot;, &quot;Miles_per_Gallon&quot;: 26.0, &quot;Cylinders&quot;: 4, &quot;Displacement&quot;: 98.0, &quot;Horsepower&quot;: 79.0, &quot;Weight_in_lbs&quot;: 2255, &quot;Acceleration&quot;: 17.7, &quot;Year&quot;: &quot;1976-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;USA&quot;}, {&quot;Name&quot;: &quot;renault 12tl&quot;, &quot;Miles_per_Gallon&quot;: 27.0, &quot;Cylinders&quot;: 4, &quot;Displacement&quot;: 101.0, &quot;Horsepower&quot;: 83.0, &quot;Weight_in_lbs&quot;: 2202, &quot;Acceleration&quot;: 15.3, &quot;Year&quot;: &quot;1976-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;Europe&quot;}, {&quot;Name&quot;: &quot;chevrolet chevelle malibu classic&quot;, &quot;Miles_per_Gallon&quot;: 17.5, &quot;Cylinders&quot;: 8, &quot;Displacement&quot;: 305.0, &quot;Horsepower&quot;: 140.0, &quot;Weight_in_lbs&quot;: 4215, &quot;Acceleration&quot;: 13.0, &quot;Year&quot;: &quot;1976-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;USA&quot;}, {&quot;Name&quot;: &quot;dodge coronet brougham&quot;, &quot;Miles_per_Gallon&quot;: 16.0, &quot;Cylinders&quot;: 8, &quot;Displacement&quot;: 318.0, &quot;Horsepower&quot;: 150.0, &quot;Weight_in_lbs&quot;: 4190, &quot;Acceleration&quot;: 13.0, &quot;Year&quot;: &quot;1976-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;USA&quot;}, {&quot;Name&quot;: &quot;amc matador&quot;, &quot;Miles_per_Gallon&quot;: 15.5, &quot;Cylinders&quot;: 8, &quot;Displacement&quot;: 304.0, &quot;Horsepower&quot;: 120.0, &quot;Weight_in_lbs&quot;: 3962, &quot;Acceleration&quot;: 13.9, &quot;Year&quot;: &quot;1976-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;USA&quot;}, {&quot;Name&quot;: &quot;ford gran torino&quot;, &quot;Miles_per_Gallon&quot;: 14.5, &quot;Cylinders&quot;: 8, &quot;Displacement&quot;: 351.0, &quot;Horsepower&quot;: 152.0, &quot;Weight_in_lbs&quot;: 4215, &quot;Acceleration&quot;: 12.8, &quot;Year&quot;: &quot;1976-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;USA&quot;}, {&quot;Name&quot;: &quot;plymouth valiant&quot;, &quot;Miles_per_Gallon&quot;: 22.0, &quot;Cylinders&quot;: 6, &quot;Displacement&quot;: 225.0, &quot;Horsepower&quot;: 100.0, &quot;Weight_in_lbs&quot;: 3233, &quot;Acceleration&quot;: 15.4, &quot;Year&quot;: &quot;1976-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;USA&quot;}, {&quot;Name&quot;: &quot;chevrolet nova&quot;, &quot;Miles_per_Gallon&quot;: 22.0, &quot;Cylinders&quot;: 6, &quot;Displacement&quot;: 250.0, &quot;Horsepower&quot;: 105.0, &quot;Weight_in_lbs&quot;: 3353, &quot;Acceleration&quot;: 14.5, &quot;Year&quot;: &quot;1976-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;USA&quot;}, {&quot;Name&quot;: &quot;ford maverick&quot;, &quot;Miles_per_Gallon&quot;: 24.0, &quot;Cylinders&quot;: 6, &quot;Displacement&quot;: 200.0, &quot;Horsepower&quot;: 81.0, &quot;Weight_in_lbs&quot;: 3012, &quot;Acceleration&quot;: 17.6, &quot;Year&quot;: &quot;1976-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;USA&quot;}, {&quot;Name&quot;: &quot;amc hornet&quot;, &quot;Miles_per_Gallon&quot;: 22.5, &quot;Cylinders&quot;: 6, &quot;Displacement&quot;: 232.0, &quot;Horsepower&quot;: 90.0, &quot;Weight_in_lbs&quot;: 3085, &quot;Acceleration&quot;: 17.6, &quot;Year&quot;: &quot;1976-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;USA&quot;}, {&quot;Name&quot;: &quot;chevrolet chevette&quot;, &quot;Miles_per_Gallon&quot;: 29.0, &quot;Cylinders&quot;: 4, &quot;Displacement&quot;: 85.0, &quot;Horsepower&quot;: 52.0, &quot;Weight_in_lbs&quot;: 2035, &quot;Acceleration&quot;: 22.2, &quot;Year&quot;: &quot;1976-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;USA&quot;}, {&quot;Name&quot;: &quot;chevrolet woody&quot;, &quot;Miles_per_Gallon&quot;: 24.5, &quot;Cylinders&quot;: 4, &quot;Displacement&quot;: 98.0, &quot;Horsepower&quot;: 60.0, &quot;Weight_in_lbs&quot;: 2164, &quot;Acceleration&quot;: 22.1, &quot;Year&quot;: &quot;1976-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;USA&quot;}, {&quot;Name&quot;: &quot;vw rabbit&quot;, &quot;Miles_per_Gallon&quot;: 29.0, &quot;Cylinders&quot;: 4, &quot;Displacement&quot;: 90.0, &quot;Horsepower&quot;: 70.0, &quot;Weight_in_lbs&quot;: 1937, &quot;Acceleration&quot;: 14.2, &quot;Year&quot;: &quot;1976-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;Europe&quot;}, {&quot;Name&quot;: &quot;honda civic&quot;, &quot;Miles_per_Gallon&quot;: 33.0, &quot;Cylinders&quot;: 4, &quot;Displacement&quot;: 91.0, &quot;Horsepower&quot;: 53.0, &quot;Weight_in_lbs&quot;: 1795, &quot;Acceleration&quot;: 17.4, &quot;Year&quot;: &quot;1976-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;Japan&quot;}, {&quot;Name&quot;: &quot;dodge aspen se&quot;, &quot;Miles_per_Gallon&quot;: 20.0, &quot;Cylinders&quot;: 6, &quot;Displacement&quot;: 225.0, &quot;Horsepower&quot;: 100.0, &quot;Weight_in_lbs&quot;: 3651, &quot;Acceleration&quot;: 17.7, &quot;Year&quot;: &quot;1976-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;USA&quot;}, {&quot;Name&quot;: &quot;ford granada ghia&quot;, &quot;Miles_per_Gallon&quot;: 18.0, &quot;Cylinders&quot;: 6, &quot;Displacement&quot;: 250.0, &quot;Horsepower&quot;: 78.0, &quot;Weight_in_lbs&quot;: 3574, &quot;Acceleration&quot;: 21.0, &quot;Year&quot;: &quot;1976-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;USA&quot;}, {&quot;Name&quot;: &quot;pontiac ventura sj&quot;, &quot;Miles_per_Gallon&quot;: 18.5, &quot;Cylinders&quot;: 6, &quot;Displacement&quot;: 250.0, &quot;Horsepower&quot;: 110.0, &quot;Weight_in_lbs&quot;: 3645, &quot;Acceleration&quot;: 16.2, &quot;Year&quot;: &quot;1976-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;USA&quot;}, {&quot;Name&quot;: &quot;amc pacer d&#x2F;l&quot;, &quot;Miles_per_Gallon&quot;: 17.5, &quot;Cylinders&quot;: 6, &quot;Displacement&quot;: 258.0, &quot;Horsepower&quot;: 95.0, &quot;Weight_in_lbs&quot;: 3193, &quot;Acceleration&quot;: 17.8, &quot;Year&quot;: &quot;1976-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;USA&quot;}, {&quot;Name&quot;: &quot;volkswagen rabbit&quot;, &quot;Miles_per_Gallon&quot;: 29.5, &quot;Cylinders&quot;: 4, &quot;Displacement&quot;: 97.0, &quot;Horsepower&quot;: 71.0, &quot;Weight_in_lbs&quot;: 1825, &quot;Acceleration&quot;: 12.2, &quot;Year&quot;: &quot;1976-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;Europe&quot;}, {&quot;Name&quot;: &quot;datsun b-210&quot;, &quot;Miles_per_Gallon&quot;: 32.0, &quot;Cylinders&quot;: 4, &quot;Displacement&quot;: 85.0, &quot;Horsepower&quot;: 70.0, &quot;Weight_in_lbs&quot;: 1990, &quot;Acceleration&quot;: 17.0, &quot;Year&quot;: &quot;1976-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;Japan&quot;}, {&quot;Name&quot;: &quot;toyota corolla&quot;, &quot;Miles_per_Gallon&quot;: 28.0, &quot;Cylinders&quot;: 4, &quot;Displacement&quot;: 97.0, &quot;Horsepower&quot;: 75.0, &quot;Weight_in_lbs&quot;: 2155, &quot;Acceleration&quot;: 16.4, &quot;Year&quot;: &quot;1976-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;Japan&quot;}, {&quot;Name&quot;: &quot;ford pinto&quot;, &quot;Miles_per_Gallon&quot;: 26.5, &quot;Cylinders&quot;: 4, &quot;Displacement&quot;: 140.0, &quot;Horsepower&quot;: 72.0, &quot;Weight_in_lbs&quot;: 2565, &quot;Acceleration&quot;: 13.6, &quot;Year&quot;: &quot;1976-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;USA&quot;}, {&quot;Name&quot;: &quot;volvo 245&quot;, &quot;Miles_per_Gallon&quot;: 20.0, &quot;Cylinders&quot;: 4, &quot;Displacement&quot;: 130.0, &quot;Horsepower&quot;: 102.0, &quot;Weight_in_lbs&quot;: 3150, &quot;Acceleration&quot;: 15.7, &quot;Year&quot;: &quot;1976-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;Europe&quot;}, {&quot;Name&quot;: &quot;plymouth volare premier v8&quot;, &quot;Miles_per_Gallon&quot;: 13.0, &quot;Cylinders&quot;: 8, &quot;Displacement&quot;: 318.0, &quot;Horsepower&quot;: 150.0, &quot;Weight_in_lbs&quot;: 3940, &quot;Acceleration&quot;: 13.2, &quot;Year&quot;: &quot;1976-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;USA&quot;}, {&quot;Name&quot;: &quot;peugeot 504&quot;, &quot;Miles_per_Gallon&quot;: 19.0, &quot;Cylinders&quot;: 4, &quot;Displacement&quot;: 120.0, &quot;Horsepower&quot;: 88.0, &quot;Weight_in_lbs&quot;: 3270, &quot;Acceleration&quot;: 21.9, &quot;Year&quot;: &quot;1976-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;Europe&quot;}, {&quot;Name&quot;: &quot;toyota mark ii&quot;, &quot;Miles_per_Gallon&quot;: 19.0, &quot;Cylinders&quot;: 6, &quot;Displacement&quot;: 156.0, &quot;Horsepower&quot;: 108.0, &quot;Weight_in_lbs&quot;: 2930, &quot;Acceleration&quot;: 15.5, &quot;Year&quot;: &quot;1976-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;Japan&quot;}, {&quot;Name&quot;: &quot;mercedes-benz 280s&quot;, &quot;Miles_per_Gallon&quot;: 16.5, &quot;Cylinders&quot;: 6, &quot;Displacement&quot;: 168.0, &quot;Horsepower&quot;: 120.0, &quot;Weight_in_lbs&quot;: 3820, &quot;Acceleration&quot;: 16.7, &quot;Year&quot;: &quot;1976-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;Europe&quot;}, {&quot;Name&quot;: &quot;cadillac seville&quot;, &quot;Miles_per_Gallon&quot;: 16.5, &quot;Cylinders&quot;: 8, &quot;Displacement&quot;: 350.0, &quot;Horsepower&quot;: 180.0, &quot;Weight_in_lbs&quot;: 4380, &quot;Acceleration&quot;: 12.1, &quot;Year&quot;: &quot;1976-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;USA&quot;}, {&quot;Name&quot;: &quot;chevy c10&quot;, &quot;Miles_per_Gallon&quot;: 13.0, &quot;Cylinders&quot;: 8, &quot;Displacement&quot;: 350.0, &quot;Horsepower&quot;: 145.0, &quot;Weight_in_lbs&quot;: 4055, &quot;Acceleration&quot;: 12.0, &quot;Year&quot;: &quot;1976-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;USA&quot;}, {&quot;Name&quot;: &quot;ford f108&quot;, &quot;Miles_per_Gallon&quot;: 13.0, &quot;Cylinders&quot;: 8, &quot;Displacement&quot;: 302.0, &quot;Horsepower&quot;: 130.0, &quot;Weight_in_lbs&quot;: 3870, &quot;Acceleration&quot;: 15.0, &quot;Year&quot;: &quot;1976-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;USA&quot;}, {&quot;Name&quot;: &quot;dodge d100&quot;, &quot;Miles_per_Gallon&quot;: 13.0, &quot;Cylinders&quot;: 8, &quot;Displacement&quot;: 318.0, &quot;Horsepower&quot;: 150.0, &quot;Weight_in_lbs&quot;: 3755, &quot;Acceleration&quot;: 14.0, &quot;Year&quot;: &quot;1976-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;USA&quot;}, {&quot;Name&quot;: &quot;honda Accelerationord cvcc&quot;, &quot;Miles_per_Gallon&quot;: 31.5, &quot;Cylinders&quot;: 4, &quot;Displacement&quot;: 98.0, &quot;Horsepower&quot;: 68.0, &quot;Weight_in_lbs&quot;: 2045, &quot;Acceleration&quot;: 18.5, &quot;Year&quot;: &quot;1977-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;Japan&quot;}, {&quot;Name&quot;: &quot;buick opel isuzu deluxe&quot;, &quot;Miles_per_Gallon&quot;: 30.0, &quot;Cylinders&quot;: 4, &quot;Displacement&quot;: 111.0, &quot;Horsepower&quot;: 80.0, &quot;Weight_in_lbs&quot;: 2155, &quot;Acceleration&quot;: 14.8, &quot;Year&quot;: &quot;1977-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;USA&quot;}, {&quot;Name&quot;: &quot;renault 5 gtl&quot;, &quot;Miles_per_Gallon&quot;: 36.0, &quot;Cylinders&quot;: 4, &quot;Displacement&quot;: 79.0, &quot;Horsepower&quot;: 58.0, &quot;Weight_in_lbs&quot;: 1825, &quot;Acceleration&quot;: 18.6, &quot;Year&quot;: &quot;1977-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;Europe&quot;}, {&quot;Name&quot;: &quot;plymouth arrow gs&quot;, &quot;Miles_per_Gallon&quot;: 25.5, &quot;Cylinders&quot;: 4, &quot;Displacement&quot;: 122.0, &quot;Horsepower&quot;: 96.0, &quot;Weight_in_lbs&quot;: 2300, &quot;Acceleration&quot;: 15.5, &quot;Year&quot;: &quot;1977-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;USA&quot;}, {&quot;Name&quot;: &quot;datsun f-10 hatchback&quot;, &quot;Miles_per_Gallon&quot;: 33.5, &quot;Cylinders&quot;: 4, &quot;Displacement&quot;: 85.0, &quot;Horsepower&quot;: 70.0, &quot;Weight_in_lbs&quot;: 1945, &quot;Acceleration&quot;: 16.8, &quot;Year&quot;: &quot;1977-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;Japan&quot;}, {&quot;Name&quot;: &quot;chevrolet caprice classic&quot;, &quot;Miles_per_Gallon&quot;: 17.5, &quot;Cylinders&quot;: 8, &quot;Displacement&quot;: 305.0, &quot;Horsepower&quot;: 145.0, &quot;Weight_in_lbs&quot;: 3880, &quot;Acceleration&quot;: 12.5, &quot;Year&quot;: &quot;1977-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;USA&quot;}, {&quot;Name&quot;: &quot;oldsmobile cutlass supreme&quot;, &quot;Miles_per_Gallon&quot;: 17.0, &quot;Cylinders&quot;: 8, &quot;Displacement&quot;: 260.0, &quot;Horsepower&quot;: 110.0, &quot;Weight_in_lbs&quot;: 4060, &quot;Acceleration&quot;: 19.0, &quot;Year&quot;: &quot;1977-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;USA&quot;}, {&quot;Name&quot;: &quot;dodge monaco brougham&quot;, &quot;Miles_per_Gallon&quot;: 15.5, &quot;Cylinders&quot;: 8, &quot;Displacement&quot;: 318.0, &quot;Horsepower&quot;: 145.0, &quot;Weight_in_lbs&quot;: 4140, &quot;Acceleration&quot;: 13.7, &quot;Year&quot;: &quot;1977-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;USA&quot;}, {&quot;Name&quot;: &quot;mercury cougar brougham&quot;, &quot;Miles_per_Gallon&quot;: 15.0, &quot;Cylinders&quot;: 8, &quot;Displacement&quot;: 302.0, &quot;Horsepower&quot;: 130.0, &quot;Weight_in_lbs&quot;: 4295, &quot;Acceleration&quot;: 14.9, &quot;Year&quot;: &quot;1977-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;USA&quot;}, {&quot;Name&quot;: &quot;chevrolet concours&quot;, &quot;Miles_per_Gallon&quot;: 17.5, &quot;Cylinders&quot;: 6, &quot;Displacement&quot;: 250.0, &quot;Horsepower&quot;: 110.0, &quot;Weight_in_lbs&quot;: 3520, &quot;Acceleration&quot;: 16.4, &quot;Year&quot;: &quot;1977-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;USA&quot;}, {&quot;Name&quot;: &quot;buick skylark&quot;, &quot;Miles_per_Gallon&quot;: 20.5, &quot;Cylinders&quot;: 6, &quot;Displacement&quot;: 231.0, &quot;Horsepower&quot;: 105.0, &quot;Weight_in_lbs&quot;: 3425, &quot;Acceleration&quot;: 16.9, &quot;Year&quot;: &quot;1977-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;USA&quot;}, {&quot;Name&quot;: &quot;plymouth volare custom&quot;, &quot;Miles_per_Gallon&quot;: 19.0, &quot;Cylinders&quot;: 6, &quot;Displacement&quot;: 225.0, &quot;Horsepower&quot;: 100.0, &quot;Weight_in_lbs&quot;: 3630, &quot;Acceleration&quot;: 17.7, &quot;Year&quot;: &quot;1977-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;USA&quot;}, {&quot;Name&quot;: &quot;ford granada&quot;, &quot;Miles_per_Gallon&quot;: 18.5, &quot;Cylinders&quot;: 6, &quot;Displacement&quot;: 250.0, &quot;Horsepower&quot;: 98.0, &quot;Weight_in_lbs&quot;: 3525, &quot;Acceleration&quot;: 19.0, &quot;Year&quot;: &quot;1977-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;USA&quot;}, {&quot;Name&quot;: &quot;pontiac grand prix lj&quot;, &quot;Miles_per_Gallon&quot;: 16.0, &quot;Cylinders&quot;: 8, &quot;Displacement&quot;: 400.0, &quot;Horsepower&quot;: 180.0, &quot;Weight_in_lbs&quot;: 4220, &quot;Acceleration&quot;: 11.1, &quot;Year&quot;: &quot;1977-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;USA&quot;}, {&quot;Name&quot;: &quot;chevrolet monte carlo landau&quot;, &quot;Miles_per_Gallon&quot;: 15.5, &quot;Cylinders&quot;: 8, &quot;Displacement&quot;: 350.0, &quot;Horsepower&quot;: 170.0, &quot;Weight_in_lbs&quot;: 4165, &quot;Acceleration&quot;: 11.4, &quot;Year&quot;: &quot;1977-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;USA&quot;}, {&quot;Name&quot;: &quot;chrysler cordoba&quot;, &quot;Miles_per_Gallon&quot;: 15.5, &quot;Cylinders&quot;: 8, &quot;Displacement&quot;: 400.0, &quot;Horsepower&quot;: 190.0, &quot;Weight_in_lbs&quot;: 4325, &quot;Acceleration&quot;: 12.2, &quot;Year&quot;: &quot;1977-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;USA&quot;}, {&quot;Name&quot;: &quot;ford thunderbird&quot;, &quot;Miles_per_Gallon&quot;: 16.0, &quot;Cylinders&quot;: 8, &quot;Displacement&quot;: 351.0, &quot;Horsepower&quot;: 149.0, &quot;Weight_in_lbs&quot;: 4335, &quot;Acceleration&quot;: 14.5, &quot;Year&quot;: &quot;1977-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;USA&quot;}, {&quot;Name&quot;: &quot;volkswagen rabbit custom&quot;, &quot;Miles_per_Gallon&quot;: 29.0, &quot;Cylinders&quot;: 4, &quot;Displacement&quot;: 97.0, &quot;Horsepower&quot;: 78.0, &quot;Weight_in_lbs&quot;: 1940, &quot;Acceleration&quot;: 14.5, &quot;Year&quot;: &quot;1977-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;Europe&quot;}, {&quot;Name&quot;: &quot;pontiac sunbird coupe&quot;, &quot;Miles_per_Gallon&quot;: 24.5, &quot;Cylinders&quot;: 4, &quot;Displacement&quot;: 151.0, &quot;Horsepower&quot;: 88.0, &quot;Weight_in_lbs&quot;: 2740, &quot;Acceleration&quot;: 16.0, &quot;Year&quot;: &quot;1977-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;USA&quot;}, {&quot;Name&quot;: &quot;toyota corolla liftback&quot;, &quot;Miles_per_Gallon&quot;: 26.0, &quot;Cylinders&quot;: 4, &quot;Displacement&quot;: 97.0, &quot;Horsepower&quot;: 75.0, &quot;Weight_in_lbs&quot;: 2265, &quot;Acceleration&quot;: 18.2, &quot;Year&quot;: &quot;1977-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;Japan&quot;}, {&quot;Name&quot;: &quot;ford mustang ii 2+2&quot;, &quot;Miles_per_Gallon&quot;: 25.5, &quot;Cylinders&quot;: 4, &quot;Displacement&quot;: 140.0, &quot;Horsepower&quot;: 89.0, &quot;Weight_in_lbs&quot;: 2755, &quot;Acceleration&quot;: 15.8, &quot;Year&quot;: &quot;1977-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;USA&quot;}, {&quot;Name&quot;: &quot;chevrolet chevette&quot;, &quot;Miles_per_Gallon&quot;: 30.5, &quot;Cylinders&quot;: 4, &quot;Displacement&quot;: 98.0, &quot;Horsepower&quot;: 63.0, &quot;Weight_in_lbs&quot;: 2051, &quot;Acceleration&quot;: 17.0, &quot;Year&quot;: &quot;1977-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;USA&quot;}, {&quot;Name&quot;: &quot;dodge colt m&#x2F;m&quot;, &quot;Miles_per_Gallon&quot;: 33.5, &quot;Cylinders&quot;: 4, &quot;Displacement&quot;: 98.0, &quot;Horsepower&quot;: 83.0, &quot;Weight_in_lbs&quot;: 2075, &quot;Acceleration&quot;: 15.9, &quot;Year&quot;: &quot;1977-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;USA&quot;}, {&quot;Name&quot;: &quot;subaru dl&quot;, &quot;Miles_per_Gallon&quot;: 30.0, &quot;Cylinders&quot;: 4, &quot;Displacement&quot;: 97.0, &quot;Horsepower&quot;: 67.0, &quot;Weight_in_lbs&quot;: 1985, &quot;Acceleration&quot;: 16.4, &quot;Year&quot;: &quot;1977-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;Japan&quot;}, {&quot;Name&quot;: &quot;volkswagen dasher&quot;, &quot;Miles_per_Gallon&quot;: 30.5, &quot;Cylinders&quot;: 4, &quot;Displacement&quot;: 97.0, &quot;Horsepower&quot;: 78.0, &quot;Weight_in_lbs&quot;: 2190, &quot;Acceleration&quot;: 14.1, &quot;Year&quot;: &quot;1977-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;Europe&quot;}, {&quot;Name&quot;: &quot;datsun 810&quot;, &quot;Miles_per_Gallon&quot;: 22.0, &quot;Cylinders&quot;: 6, &quot;Displacement&quot;: 146.0, &quot;Horsepower&quot;: 97.0, &quot;Weight_in_lbs&quot;: 2815, &quot;Acceleration&quot;: 14.5, &quot;Year&quot;: &quot;1977-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;Japan&quot;}, {&quot;Name&quot;: &quot;bmw 320i&quot;, &quot;Miles_per_Gallon&quot;: 21.5, &quot;Cylinders&quot;: 4, &quot;Displacement&quot;: 121.0, &quot;Horsepower&quot;: 110.0, &quot;Weight_in_lbs&quot;: 2600, &quot;Acceleration&quot;: 12.8, &quot;Year&quot;: &quot;1977-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;Europe&quot;}, {&quot;Name&quot;: &quot;mazda rx-4&quot;, &quot;Miles_per_Gallon&quot;: 21.5, &quot;Cylinders&quot;: 3, &quot;Displacement&quot;: 80.0, &quot;Horsepower&quot;: 110.0, &quot;Weight_in_lbs&quot;: 2720, &quot;Acceleration&quot;: 13.5, &quot;Year&quot;: &quot;1977-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;Japan&quot;}, {&quot;Name&quot;: &quot;volkswagen rabbit custom diesel&quot;, &quot;Miles_per_Gallon&quot;: 43.1, &quot;Cylinders&quot;: 4, &quot;Displacement&quot;: 90.0, &quot;Horsepower&quot;: 48.0, &quot;Weight_in_lbs&quot;: 1985, &quot;Acceleration&quot;: 21.5, &quot;Year&quot;: &quot;1978-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;Europe&quot;}, {&quot;Name&quot;: &quot;ford fiesta&quot;, &quot;Miles_per_Gallon&quot;: 36.1, &quot;Cylinders&quot;: 4, &quot;Displacement&quot;: 98.0, &quot;Horsepower&quot;: 66.0, &quot;Weight_in_lbs&quot;: 1800, &quot;Acceleration&quot;: 14.4, &quot;Year&quot;: &quot;1978-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;USA&quot;}, {&quot;Name&quot;: &quot;mazda glc deluxe&quot;, &quot;Miles_per_Gallon&quot;: 32.8, &quot;Cylinders&quot;: 4, &quot;Displacement&quot;: 78.0, &quot;Horsepower&quot;: 52.0, &quot;Weight_in_lbs&quot;: 1985, &quot;Acceleration&quot;: 19.4, &quot;Year&quot;: &quot;1978-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;Japan&quot;}, {&quot;Name&quot;: &quot;datsun b210 gx&quot;, &quot;Miles_per_Gallon&quot;: 39.4, &quot;Cylinders&quot;: 4, &quot;Displacement&quot;: 85.0, &quot;Horsepower&quot;: 70.0, &quot;Weight_in_lbs&quot;: 2070, &quot;Acceleration&quot;: 18.6, &quot;Year&quot;: &quot;1978-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;Japan&quot;}, {&quot;Name&quot;: &quot;honda civic cvcc&quot;, &quot;Miles_per_Gallon&quot;: 36.1, &quot;Cylinders&quot;: 4, &quot;Displacement&quot;: 91.0, &quot;Horsepower&quot;: 60.0, &quot;Weight_in_lbs&quot;: 1800, &quot;Acceleration&quot;: 16.4, &quot;Year&quot;: &quot;1978-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;Japan&quot;}, {&quot;Name&quot;: &quot;oldsmobile cutlass salon brougham&quot;, &quot;Miles_per_Gallon&quot;: 19.9, &quot;Cylinders&quot;: 8, &quot;Displacement&quot;: 260.0, &quot;Horsepower&quot;: 110.0, &quot;Weight_in_lbs&quot;: 3365, &quot;Acceleration&quot;: 15.5, &quot;Year&quot;: &quot;1978-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;USA&quot;}, {&quot;Name&quot;: &quot;dodge diplomat&quot;, &quot;Miles_per_Gallon&quot;: 19.4, &quot;Cylinders&quot;: 8, &quot;Displacement&quot;: 318.0, &quot;Horsepower&quot;: 140.0, &quot;Weight_in_lbs&quot;: 3735, &quot;Acceleration&quot;: 13.2, &quot;Year&quot;: &quot;1978-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;USA&quot;}, {&quot;Name&quot;: &quot;mercury monarch ghia&quot;, &quot;Miles_per_Gallon&quot;: 20.2, &quot;Cylinders&quot;: 8, &quot;Displacement&quot;: 302.0, &quot;Horsepower&quot;: 139.0, &quot;Weight_in_lbs&quot;: 3570, &quot;Acceleration&quot;: 12.8, &quot;Year&quot;: &quot;1978-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;USA&quot;}, {&quot;Name&quot;: &quot;pontiac phoenix lj&quot;, &quot;Miles_per_Gallon&quot;: 19.2, &quot;Cylinders&quot;: 6, &quot;Displacement&quot;: 231.0, &quot;Horsepower&quot;: 105.0, &quot;Weight_in_lbs&quot;: 3535, &quot;Acceleration&quot;: 19.2, &quot;Year&quot;: &quot;1978-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;USA&quot;}, {&quot;Name&quot;: &quot;chevrolet malibu&quot;, &quot;Miles_per_Gallon&quot;: 20.5, &quot;Cylinders&quot;: 6, &quot;Displacement&quot;: 200.0, &quot;Horsepower&quot;: 95.0, &quot;Weight_in_lbs&quot;: 3155, &quot;Acceleration&quot;: 18.2, &quot;Year&quot;: &quot;1978-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;USA&quot;}, {&quot;Name&quot;: &quot;ford fairmont (auto)&quot;, &quot;Miles_per_Gallon&quot;: 20.2, &quot;Cylinders&quot;: 6, &quot;Displacement&quot;: 200.0, &quot;Horsepower&quot;: 85.0, &quot;Weight_in_lbs&quot;: 2965, &quot;Acceleration&quot;: 15.8, &quot;Year&quot;: &quot;1978-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;USA&quot;}, {&quot;Name&quot;: &quot;ford fairmont (man)&quot;, &quot;Miles_per_Gallon&quot;: 25.1, &quot;Cylinders&quot;: 4, &quot;Displacement&quot;: 140.0, &quot;Horsepower&quot;: 88.0, &quot;Weight_in_lbs&quot;: 2720, &quot;Acceleration&quot;: 15.4, &quot;Year&quot;: &quot;1978-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;USA&quot;}, {&quot;Name&quot;: &quot;plymouth volare&quot;, &quot;Miles_per_Gallon&quot;: 20.5, &quot;Cylinders&quot;: 6, &quot;Displacement&quot;: 225.0, &quot;Horsepower&quot;: 100.0, &quot;Weight_in_lbs&quot;: 3430, &quot;Acceleration&quot;: 17.2, &quot;Year&quot;: &quot;1978-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;USA&quot;}, {&quot;Name&quot;: &quot;amc concord&quot;, &quot;Miles_per_Gallon&quot;: 19.4, &quot;Cylinders&quot;: 6, &quot;Displacement&quot;: 232.0, &quot;Horsepower&quot;: 90.0, &quot;Weight_in_lbs&quot;: 3210, &quot;Acceleration&quot;: 17.2, &quot;Year&quot;: &quot;1978-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;USA&quot;}, {&quot;Name&quot;: &quot;buick century special&quot;, &quot;Miles_per_Gallon&quot;: 20.6, &quot;Cylinders&quot;: 6, &quot;Displacement&quot;: 231.0, &quot;Horsepower&quot;: 105.0, &quot;Weight_in_lbs&quot;: 3380, &quot;Acceleration&quot;: 15.8, &quot;Year&quot;: &quot;1978-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;USA&quot;}, {&quot;Name&quot;: &quot;mercury zephyr&quot;, &quot;Miles_per_Gallon&quot;: 20.8, &quot;Cylinders&quot;: 6, &quot;Displacement&quot;: 200.0, &quot;Horsepower&quot;: 85.0, &quot;Weight_in_lbs&quot;: 3070, &quot;Acceleration&quot;: 16.7, &quot;Year&quot;: &quot;1978-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;USA&quot;}, {&quot;Name&quot;: &quot;dodge aspen&quot;, &quot;Miles_per_Gallon&quot;: 18.6, &quot;Cylinders&quot;: 6, &quot;Displacement&quot;: 225.0, &quot;Horsepower&quot;: 110.0, &quot;Weight_in_lbs&quot;: 3620, &quot;Acceleration&quot;: 18.7, &quot;Year&quot;: &quot;1978-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;USA&quot;}, {&quot;Name&quot;: &quot;amc concord d&#x2F;l&quot;, &quot;Miles_per_Gallon&quot;: 18.1, &quot;Cylinders&quot;: 6, &quot;Displacement&quot;: 258.0, &quot;Horsepower&quot;: 120.0, &quot;Weight_in_lbs&quot;: 3410, &quot;Acceleration&quot;: 15.1, &quot;Year&quot;: &quot;1978-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;USA&quot;}, {&quot;Name&quot;: &quot;chevrolet monte carlo landau&quot;, &quot;Miles_per_Gallon&quot;: 19.2, &quot;Cylinders&quot;: 8, &quot;Displacement&quot;: 305.0, &quot;Horsepower&quot;: 145.0, &quot;Weight_in_lbs&quot;: 3425, &quot;Acceleration&quot;: 13.2, &quot;Year&quot;: &quot;1978-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;USA&quot;}, {&quot;Name&quot;: &quot;buick regal sport coupe (turbo)&quot;, &quot;Miles_per_Gallon&quot;: 17.7, &quot;Cylinders&quot;: 6, &quot;Displacement&quot;: 231.0, &quot;Horsepower&quot;: 165.0, &quot;Weight_in_lbs&quot;: 3445, &quot;Acceleration&quot;: 13.4, &quot;Year&quot;: &quot;1978-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;USA&quot;}, {&quot;Name&quot;: &quot;ford futura&quot;, &quot;Miles_per_Gallon&quot;: 18.1, &quot;Cylinders&quot;: 8, &quot;Displacement&quot;: 302.0, &quot;Horsepower&quot;: 139.0, &quot;Weight_in_lbs&quot;: 3205, &quot;Acceleration&quot;: 11.2, &quot;Year&quot;: &quot;1978-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;USA&quot;}, {&quot;Name&quot;: &quot;dodge magnum xe&quot;, &quot;Miles_per_Gallon&quot;: 17.5, &quot;Cylinders&quot;: 8, &quot;Displacement&quot;: 318.0, &quot;Horsepower&quot;: 140.0, &quot;Weight_in_lbs&quot;: 4080, &quot;Acceleration&quot;: 13.7, &quot;Year&quot;: &quot;1978-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;USA&quot;}, {&quot;Name&quot;: &quot;chevrolet chevette&quot;, &quot;Miles_per_Gallon&quot;: 30.0, &quot;Cylinders&quot;: 4, &quot;Displacement&quot;: 98.0, &quot;Horsepower&quot;: 68.0, &quot;Weight_in_lbs&quot;: 2155, &quot;Acceleration&quot;: 16.5, &quot;Year&quot;: &quot;1978-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;USA&quot;}, {&quot;Name&quot;: &quot;toyota corona&quot;, &quot;Miles_per_Gallon&quot;: 27.5, &quot;Cylinders&quot;: 4, &quot;Displacement&quot;: 134.0, &quot;Horsepower&quot;: 95.0, &quot;Weight_in_lbs&quot;: 2560, &quot;Acceleration&quot;: 14.2, &quot;Year&quot;: &quot;1978-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;Japan&quot;}, {&quot;Name&quot;: &quot;datsun 510&quot;, &quot;Miles_per_Gallon&quot;: 27.2, &quot;Cylinders&quot;: 4, &quot;Displacement&quot;: 119.0, &quot;Horsepower&quot;: 97.0, &quot;Weight_in_lbs&quot;: 2300, &quot;Acceleration&quot;: 14.7, &quot;Year&quot;: &quot;1978-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;Japan&quot;}, {&quot;Name&quot;: &quot;dodge omni&quot;, &quot;Miles_per_Gallon&quot;: 30.9, &quot;Cylinders&quot;: 4, &quot;Displacement&quot;: 105.0, &quot;Horsepower&quot;: 75.0, &quot;Weight_in_lbs&quot;: 2230, &quot;Acceleration&quot;: 14.5, &quot;Year&quot;: &quot;1978-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;USA&quot;}, {&quot;Name&quot;: &quot;toyota celica gt liftback&quot;, &quot;Miles_per_Gallon&quot;: 21.1, &quot;Cylinders&quot;: 4, &quot;Displacement&quot;: 134.0, &quot;Horsepower&quot;: 95.0, &quot;Weight_in_lbs&quot;: 2515, &quot;Acceleration&quot;: 14.8, &quot;Year&quot;: &quot;1978-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;Japan&quot;}, {&quot;Name&quot;: &quot;plymouth sapporo&quot;, &quot;Miles_per_Gallon&quot;: 23.2, &quot;Cylinders&quot;: 4, &quot;Displacement&quot;: 156.0, &quot;Horsepower&quot;: 105.0, &quot;Weight_in_lbs&quot;: 2745, &quot;Acceleration&quot;: 16.7, &quot;Year&quot;: &quot;1978-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;USA&quot;}, {&quot;Name&quot;: &quot;oldsmobile starfire sx&quot;, &quot;Miles_per_Gallon&quot;: 23.8, &quot;Cylinders&quot;: 4, &quot;Displacement&quot;: 151.0, &quot;Horsepower&quot;: 85.0, &quot;Weight_in_lbs&quot;: 2855, &quot;Acceleration&quot;: 17.6, &quot;Year&quot;: &quot;1978-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;USA&quot;}, {&quot;Name&quot;: &quot;datsun 200-sx&quot;, &quot;Miles_per_Gallon&quot;: 23.9, &quot;Cylinders&quot;: 4, &quot;Displacement&quot;: 119.0, &quot;Horsepower&quot;: 97.0, &quot;Weight_in_lbs&quot;: 2405, &quot;Acceleration&quot;: 14.9, &quot;Year&quot;: &quot;1978-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;Japan&quot;}, {&quot;Name&quot;: &quot;audi 5000&quot;, &quot;Miles_per_Gallon&quot;: 20.3, &quot;Cylinders&quot;: 5, &quot;Displacement&quot;: 131.0, &quot;Horsepower&quot;: 103.0, &quot;Weight_in_lbs&quot;: 2830, &quot;Acceleration&quot;: 15.9, &quot;Year&quot;: &quot;1978-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;Europe&quot;}, {&quot;Name&quot;: &quot;volvo 264gl&quot;, &quot;Miles_per_Gallon&quot;: 17.0, &quot;Cylinders&quot;: 6, &quot;Displacement&quot;: 163.0, &quot;Horsepower&quot;: 125.0, &quot;Weight_in_lbs&quot;: 3140, &quot;Acceleration&quot;: 13.6, &quot;Year&quot;: &quot;1978-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;Europe&quot;}, {&quot;Name&quot;: &quot;saab 99gle&quot;, &quot;Miles_per_Gallon&quot;: 21.6, &quot;Cylinders&quot;: 4, &quot;Displacement&quot;: 121.0, &quot;Horsepower&quot;: 115.0, &quot;Weight_in_lbs&quot;: 2795, &quot;Acceleration&quot;: 15.7, &quot;Year&quot;: &quot;1978-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;Europe&quot;}, {&quot;Name&quot;: &quot;peugeot 604sl&quot;, &quot;Miles_per_Gallon&quot;: 16.2, &quot;Cylinders&quot;: 6, &quot;Displacement&quot;: 163.0, &quot;Horsepower&quot;: 133.0, &quot;Weight_in_lbs&quot;: 3410, &quot;Acceleration&quot;: 15.8, &quot;Year&quot;: &quot;1978-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;Europe&quot;}, {&quot;Name&quot;: &quot;volkswagen scirocco&quot;, &quot;Miles_per_Gallon&quot;: 31.5, &quot;Cylinders&quot;: 4, &quot;Displacement&quot;: 89.0, &quot;Horsepower&quot;: 71.0, &quot;Weight_in_lbs&quot;: 1990, &quot;Acceleration&quot;: 14.9, &quot;Year&quot;: &quot;1978-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;Europe&quot;}, {&quot;Name&quot;: &quot;honda Accelerationord lx&quot;, &quot;Miles_per_Gallon&quot;: 29.5, &quot;Cylinders&quot;: 4, &quot;Displacement&quot;: 98.0, &quot;Horsepower&quot;: 68.0, &quot;Weight_in_lbs&quot;: 2135, &quot;Acceleration&quot;: 16.6, &quot;Year&quot;: &quot;1978-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;Japan&quot;}, {&quot;Name&quot;: &quot;pontiac lemans v6&quot;, &quot;Miles_per_Gallon&quot;: 21.5, &quot;Cylinders&quot;: 6, &quot;Displacement&quot;: 231.0, &quot;Horsepower&quot;: 115.0, &quot;Weight_in_lbs&quot;: 3245, &quot;Acceleration&quot;: 15.4, &quot;Year&quot;: &quot;1979-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;USA&quot;}, {&quot;Name&quot;: &quot;mercury zephyr 6&quot;, &quot;Miles_per_Gallon&quot;: 19.8, &quot;Cylinders&quot;: 6, &quot;Displacement&quot;: 200.0, &quot;Horsepower&quot;: 85.0, &quot;Weight_in_lbs&quot;: 2990, &quot;Acceleration&quot;: 18.2, &quot;Year&quot;: &quot;1979-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;USA&quot;}, {&quot;Name&quot;: &quot;ford fairmont 4&quot;, &quot;Miles_per_Gallon&quot;: 22.3, &quot;Cylinders&quot;: 4, &quot;Displacement&quot;: 140.0, &quot;Horsepower&quot;: 88.0, &quot;Weight_in_lbs&quot;: 2890, &quot;Acceleration&quot;: 17.3, &quot;Year&quot;: &quot;1979-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;USA&quot;}, {&quot;Name&quot;: &quot;amc concord dl 6&quot;, &quot;Miles_per_Gallon&quot;: 20.2, &quot;Cylinders&quot;: 6, &quot;Displacement&quot;: 232.0, &quot;Horsepower&quot;: 90.0, &quot;Weight_in_lbs&quot;: 3265, &quot;Acceleration&quot;: 18.2, &quot;Year&quot;: &quot;1979-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;USA&quot;}, {&quot;Name&quot;: &quot;dodge aspen 6&quot;, &quot;Miles_per_Gallon&quot;: 20.6, &quot;Cylinders&quot;: 6, &quot;Displacement&quot;: 225.0, &quot;Horsepower&quot;: 110.0, &quot;Weight_in_lbs&quot;: 3360, &quot;Acceleration&quot;: 16.6, &quot;Year&quot;: &quot;1979-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;USA&quot;}, {&quot;Name&quot;: &quot;chevrolet caprice classic&quot;, &quot;Miles_per_Gallon&quot;: 17.0, &quot;Cylinders&quot;: 8, &quot;Displacement&quot;: 305.0, &quot;Horsepower&quot;: 130.0, &quot;Weight_in_lbs&quot;: 3840, &quot;Acceleration&quot;: 15.4, &quot;Year&quot;: &quot;1979-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;USA&quot;}, {&quot;Name&quot;: &quot;ford ltd landau&quot;, &quot;Miles_per_Gallon&quot;: 17.6, &quot;Cylinders&quot;: 8, &quot;Displacement&quot;: 302.0, &quot;Horsepower&quot;: 129.0, &quot;Weight_in_lbs&quot;: 3725, &quot;Acceleration&quot;: 13.4, &quot;Year&quot;: &quot;1979-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;USA&quot;}, {&quot;Name&quot;: &quot;mercury grand marquis&quot;, &quot;Miles_per_Gallon&quot;: 16.5, &quot;Cylinders&quot;: 8, &quot;Displacement&quot;: 351.0, &quot;Horsepower&quot;: 138.0, &quot;Weight_in_lbs&quot;: 3955, &quot;Acceleration&quot;: 13.2, &quot;Year&quot;: &quot;1979-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;USA&quot;}, {&quot;Name&quot;: &quot;dodge st. regis&quot;, &quot;Miles_per_Gallon&quot;: 18.2, &quot;Cylinders&quot;: 8, &quot;Displacement&quot;: 318.0, &quot;Horsepower&quot;: 135.0, &quot;Weight_in_lbs&quot;: 3830, &quot;Acceleration&quot;: 15.2, &quot;Year&quot;: &quot;1979-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;USA&quot;}, {&quot;Name&quot;: &quot;buick estate wagon (sw)&quot;, &quot;Miles_per_Gallon&quot;: 16.9, &quot;Cylinders&quot;: 8, &quot;Displacement&quot;: 350.0, &quot;Horsepower&quot;: 155.0, &quot;Weight_in_lbs&quot;: 4360, &quot;Acceleration&quot;: 14.9, &quot;Year&quot;: &quot;1979-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;USA&quot;}, {&quot;Name&quot;: &quot;ford country squire (sw)&quot;, &quot;Miles_per_Gallon&quot;: 15.5, &quot;Cylinders&quot;: 8, &quot;Displacement&quot;: 351.0, &quot;Horsepower&quot;: 142.0, &quot;Weight_in_lbs&quot;: 4054, &quot;Acceleration&quot;: 14.3, &quot;Year&quot;: &quot;1979-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;USA&quot;}, {&quot;Name&quot;: &quot;chevrolet malibu classic (sw)&quot;, &quot;Miles_per_Gallon&quot;: 19.2, &quot;Cylinders&quot;: 8, &quot;Displacement&quot;: 267.0, &quot;Horsepower&quot;: 125.0, &quot;Weight_in_lbs&quot;: 3605, &quot;Acceleration&quot;: 15.0, &quot;Year&quot;: &quot;1979-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;USA&quot;}, {&quot;Name&quot;: &quot;chrysler lebaron town @ country (sw)&quot;, &quot;Miles_per_Gallon&quot;: 18.5, &quot;Cylinders&quot;: 8, &quot;Displacement&quot;: 360.0, &quot;Horsepower&quot;: 150.0, &quot;Weight_in_lbs&quot;: 3940, &quot;Acceleration&quot;: 13.0, &quot;Year&quot;: &quot;1979-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;USA&quot;}, {&quot;Name&quot;: &quot;vw rabbit custom&quot;, &quot;Miles_per_Gallon&quot;: 31.9, &quot;Cylinders&quot;: 4, &quot;Displacement&quot;: 89.0, &quot;Horsepower&quot;: 71.0, &quot;Weight_in_lbs&quot;: 1925, &quot;Acceleration&quot;: 14.0, &quot;Year&quot;: &quot;1979-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;Europe&quot;}, {&quot;Name&quot;: &quot;maxda glc deluxe&quot;, &quot;Miles_per_Gallon&quot;: 34.1, &quot;Cylinders&quot;: 4, &quot;Displacement&quot;: 86.0, &quot;Horsepower&quot;: 65.0, &quot;Weight_in_lbs&quot;: 1975, &quot;Acceleration&quot;: 15.2, &quot;Year&quot;: &quot;1979-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;Japan&quot;}, {&quot;Name&quot;: &quot;dodge colt hatchback custom&quot;, &quot;Miles_per_Gallon&quot;: 35.7, &quot;Cylinders&quot;: 4, &quot;Displacement&quot;: 98.0, &quot;Horsepower&quot;: 80.0, &quot;Weight_in_lbs&quot;: 1915, &quot;Acceleration&quot;: 14.4, &quot;Year&quot;: &quot;1979-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;USA&quot;}, {&quot;Name&quot;: &quot;amc spirit dl&quot;, &quot;Miles_per_Gallon&quot;: 27.4, &quot;Cylinders&quot;: 4, &quot;Displacement&quot;: 121.0, &quot;Horsepower&quot;: 80.0, &quot;Weight_in_lbs&quot;: 2670, &quot;Acceleration&quot;: 15.0, &quot;Year&quot;: &quot;1979-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;USA&quot;}, {&quot;Name&quot;: &quot;mercedes benz 300d&quot;, &quot;Miles_per_Gallon&quot;: 25.4, &quot;Cylinders&quot;: 5, &quot;Displacement&quot;: 183.0, &quot;Horsepower&quot;: 77.0, &quot;Weight_in_lbs&quot;: 3530, &quot;Acceleration&quot;: 20.1, &quot;Year&quot;: &quot;1979-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;Europe&quot;}, {&quot;Name&quot;: &quot;cadillac eldorado&quot;, &quot;Miles_per_Gallon&quot;: 23.0, &quot;Cylinders&quot;: 8, &quot;Displacement&quot;: 350.0, &quot;Horsepower&quot;: 125.0, &quot;Weight_in_lbs&quot;: 3900, &quot;Acceleration&quot;: 17.4, &quot;Year&quot;: &quot;1979-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;USA&quot;}, {&quot;Name&quot;: &quot;peugeot 504&quot;, &quot;Miles_per_Gallon&quot;: 27.2, &quot;Cylinders&quot;: 4, &quot;Displacement&quot;: 141.0, &quot;Horsepower&quot;: 71.0, &quot;Weight_in_lbs&quot;: 3190, &quot;Acceleration&quot;: 24.8, &quot;Year&quot;: &quot;1979-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;Europe&quot;}, {&quot;Name&quot;: &quot;oldsmobile cutlass salon brougham&quot;, &quot;Miles_per_Gallon&quot;: 23.9, &quot;Cylinders&quot;: 8, &quot;Displacement&quot;: 260.0, &quot;Horsepower&quot;: 90.0, &quot;Weight_in_lbs&quot;: 3420, &quot;Acceleration&quot;: 22.2, &quot;Year&quot;: &quot;1979-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;USA&quot;}, {&quot;Name&quot;: &quot;plymouth horizon&quot;, &quot;Miles_per_Gallon&quot;: 34.2, &quot;Cylinders&quot;: 4, &quot;Displacement&quot;: 105.0, &quot;Horsepower&quot;: 70.0, &quot;Weight_in_lbs&quot;: 2200, &quot;Acceleration&quot;: 13.2, &quot;Year&quot;: &quot;1979-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;USA&quot;}, {&quot;Name&quot;: &quot;plymouth horizon tc3&quot;, &quot;Miles_per_Gallon&quot;: 34.5, &quot;Cylinders&quot;: 4, &quot;Displacement&quot;: 105.0, &quot;Horsepower&quot;: 70.0, &quot;Weight_in_lbs&quot;: 2150, &quot;Acceleration&quot;: 14.9, &quot;Year&quot;: &quot;1979-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;USA&quot;}, {&quot;Name&quot;: &quot;datsun 210&quot;, &quot;Miles_per_Gallon&quot;: 31.8, &quot;Cylinders&quot;: 4, &quot;Displacement&quot;: 85.0, &quot;Horsepower&quot;: 65.0, &quot;Weight_in_lbs&quot;: 2020, &quot;Acceleration&quot;: 19.2, &quot;Year&quot;: &quot;1979-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;Japan&quot;}, {&quot;Name&quot;: &quot;fiat strada custom&quot;, &quot;Miles_per_Gallon&quot;: 37.3, &quot;Cylinders&quot;: 4, &quot;Displacement&quot;: 91.0, &quot;Horsepower&quot;: 69.0, &quot;Weight_in_lbs&quot;: 2130, &quot;Acceleration&quot;: 14.7, &quot;Year&quot;: &quot;1979-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;Europe&quot;}, {&quot;Name&quot;: &quot;buick skylark limited&quot;, &quot;Miles_per_Gallon&quot;: 28.4, &quot;Cylinders&quot;: 4, &quot;Displacement&quot;: 151.0, &quot;Horsepower&quot;: 90.0, &quot;Weight_in_lbs&quot;: 2670, &quot;Acceleration&quot;: 16.0, &quot;Year&quot;: &quot;1979-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;USA&quot;}, {&quot;Name&quot;: &quot;chevrolet citation&quot;, &quot;Miles_per_Gallon&quot;: 28.8, &quot;Cylinders&quot;: 6, &quot;Displacement&quot;: 173.0, &quot;Horsepower&quot;: 115.0, &quot;Weight_in_lbs&quot;: 2595, &quot;Acceleration&quot;: 11.3, &quot;Year&quot;: &quot;1979-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;USA&quot;}, {&quot;Name&quot;: &quot;oldsmobile omega brougham&quot;, &quot;Miles_per_Gallon&quot;: 26.8, &quot;Cylinders&quot;: 6, &quot;Displacement&quot;: 173.0, &quot;Horsepower&quot;: 115.0, &quot;Weight_in_lbs&quot;: 2700, &quot;Acceleration&quot;: 12.9, &quot;Year&quot;: &quot;1979-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;USA&quot;}, {&quot;Name&quot;: &quot;pontiac phoenix&quot;, &quot;Miles_per_Gallon&quot;: 33.5, &quot;Cylinders&quot;: 4, &quot;Displacement&quot;: 151.0, &quot;Horsepower&quot;: 90.0, &quot;Weight_in_lbs&quot;: 2556, &quot;Acceleration&quot;: 13.2, &quot;Year&quot;: &quot;1979-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;USA&quot;}, {&quot;Name&quot;: &quot;vw rabbit&quot;, &quot;Miles_per_Gallon&quot;: 41.5, &quot;Cylinders&quot;: 4, &quot;Displacement&quot;: 98.0, &quot;Horsepower&quot;: 76.0, &quot;Weight_in_lbs&quot;: 2144, &quot;Acceleration&quot;: 14.7, &quot;Year&quot;: &quot;1980-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;Europe&quot;}, {&quot;Name&quot;: &quot;toyota corolla tercel&quot;, &quot;Miles_per_Gallon&quot;: 38.1, &quot;Cylinders&quot;: 4, &quot;Displacement&quot;: 89.0, &quot;Horsepower&quot;: 60.0, &quot;Weight_in_lbs&quot;: 1968, &quot;Acceleration&quot;: 18.8, &quot;Year&quot;: &quot;1980-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;Japan&quot;}, {&quot;Name&quot;: &quot;chevrolet chevette&quot;, &quot;Miles_per_Gallon&quot;: 32.1, &quot;Cylinders&quot;: 4, &quot;Displacement&quot;: 98.0, &quot;Horsepower&quot;: 70.0, &quot;Weight_in_lbs&quot;: 2120, &quot;Acceleration&quot;: 15.5, &quot;Year&quot;: &quot;1980-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;USA&quot;}, {&quot;Name&quot;: &quot;datsun 310&quot;, &quot;Miles_per_Gallon&quot;: 37.2, &quot;Cylinders&quot;: 4, &quot;Displacement&quot;: 86.0, &quot;Horsepower&quot;: 65.0, &quot;Weight_in_lbs&quot;: 2019, &quot;Acceleration&quot;: 16.4, &quot;Year&quot;: &quot;1980-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;Japan&quot;}, {&quot;Name&quot;: &quot;chevrolet citation&quot;, &quot;Miles_per_Gallon&quot;: 28.0, &quot;Cylinders&quot;: 4, &quot;Displacement&quot;: 151.0, &quot;Horsepower&quot;: 90.0, &quot;Weight_in_lbs&quot;: 2678, &quot;Acceleration&quot;: 16.5, &quot;Year&quot;: &quot;1980-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;USA&quot;}, {&quot;Name&quot;: &quot;ford fairmont&quot;, &quot;Miles_per_Gallon&quot;: 26.4, &quot;Cylinders&quot;: 4, &quot;Displacement&quot;: 140.0, &quot;Horsepower&quot;: 88.0, &quot;Weight_in_lbs&quot;: 2870, &quot;Acceleration&quot;: 18.1, &quot;Year&quot;: &quot;1980-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;USA&quot;}, {&quot;Name&quot;: &quot;amc concord&quot;, &quot;Miles_per_Gallon&quot;: 24.3, &quot;Cylinders&quot;: 4, &quot;Displacement&quot;: 151.0, &quot;Horsepower&quot;: 90.0, &quot;Weight_in_lbs&quot;: 3003, &quot;Acceleration&quot;: 20.1, &quot;Year&quot;: &quot;1980-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;USA&quot;}, {&quot;Name&quot;: &quot;dodge aspen&quot;, &quot;Miles_per_Gallon&quot;: 19.1, &quot;Cylinders&quot;: 6, &quot;Displacement&quot;: 225.0, &quot;Horsepower&quot;: 90.0, &quot;Weight_in_lbs&quot;: 3381, &quot;Acceleration&quot;: 18.7, &quot;Year&quot;: &quot;1980-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;USA&quot;}, {&quot;Name&quot;: &quot;audi 4000&quot;, &quot;Miles_per_Gallon&quot;: 34.3, &quot;Cylinders&quot;: 4, &quot;Displacement&quot;: 97.0, &quot;Horsepower&quot;: 78.0, &quot;Weight_in_lbs&quot;: 2188, &quot;Acceleration&quot;: 15.8, &quot;Year&quot;: &quot;1980-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;Europe&quot;}, {&quot;Name&quot;: &quot;toyota corona liftback&quot;, &quot;Miles_per_Gallon&quot;: 29.8, &quot;Cylinders&quot;: 4, &quot;Displacement&quot;: 134.0, &quot;Horsepower&quot;: 90.0, &quot;Weight_in_lbs&quot;: 2711, &quot;Acceleration&quot;: 15.5, &quot;Year&quot;: &quot;1980-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;Japan&quot;}, {&quot;Name&quot;: &quot;mazda 626&quot;, &quot;Miles_per_Gallon&quot;: 31.3, &quot;Cylinders&quot;: 4, &quot;Displacement&quot;: 120.0, &quot;Horsepower&quot;: 75.0, &quot;Weight_in_lbs&quot;: 2542, &quot;Acceleration&quot;: 17.5, &quot;Year&quot;: &quot;1980-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;Japan&quot;}, {&quot;Name&quot;: &quot;datsun 510 hatchback&quot;, &quot;Miles_per_Gallon&quot;: 37.0, &quot;Cylinders&quot;: 4, &quot;Displacement&quot;: 119.0, &quot;Horsepower&quot;: 92.0, &quot;Weight_in_lbs&quot;: 2434, &quot;Acceleration&quot;: 15.0, &quot;Year&quot;: &quot;1980-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;Japan&quot;}, {&quot;Name&quot;: &quot;toyota corolla&quot;, &quot;Miles_per_Gallon&quot;: 32.2, &quot;Cylinders&quot;: 4, &quot;Displacement&quot;: 108.0, &quot;Horsepower&quot;: 75.0, &quot;Weight_in_lbs&quot;: 2265, &quot;Acceleration&quot;: 15.2, &quot;Year&quot;: &quot;1980-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;Japan&quot;}, {&quot;Name&quot;: &quot;mazda glc&quot;, &quot;Miles_per_Gallon&quot;: 46.6, &quot;Cylinders&quot;: 4, &quot;Displacement&quot;: 86.0, &quot;Horsepower&quot;: 65.0, &quot;Weight_in_lbs&quot;: 2110, &quot;Acceleration&quot;: 17.9, &quot;Year&quot;: &quot;1980-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;Japan&quot;}, {&quot;Name&quot;: &quot;dodge colt&quot;, &quot;Miles_per_Gallon&quot;: 27.9, &quot;Cylinders&quot;: 4, &quot;Displacement&quot;: 156.0, &quot;Horsepower&quot;: 105.0, &quot;Weight_in_lbs&quot;: 2800, &quot;Acceleration&quot;: 14.4, &quot;Year&quot;: &quot;1980-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;USA&quot;}, {&quot;Name&quot;: &quot;datsun 210&quot;, &quot;Miles_per_Gallon&quot;: 40.8, &quot;Cylinders&quot;: 4, &quot;Displacement&quot;: 85.0, &quot;Horsepower&quot;: 65.0, &quot;Weight_in_lbs&quot;: 2110, &quot;Acceleration&quot;: 19.2, &quot;Year&quot;: &quot;1980-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;Japan&quot;}, {&quot;Name&quot;: &quot;vw rabbit c (diesel)&quot;, &quot;Miles_per_Gallon&quot;: 44.3, &quot;Cylinders&quot;: 4, &quot;Displacement&quot;: 90.0, &quot;Horsepower&quot;: 48.0, &quot;Weight_in_lbs&quot;: 2085, &quot;Acceleration&quot;: 21.7, &quot;Year&quot;: &quot;1980-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;Europe&quot;}, {&quot;Name&quot;: &quot;vw dasher (diesel)&quot;, &quot;Miles_per_Gallon&quot;: 43.4, &quot;Cylinders&quot;: 4, &quot;Displacement&quot;: 90.0, &quot;Horsepower&quot;: 48.0, &quot;Weight_in_lbs&quot;: 2335, &quot;Acceleration&quot;: 23.7, &quot;Year&quot;: &quot;1980-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;Europe&quot;}, {&quot;Name&quot;: &quot;audi 5000s (diesel)&quot;, &quot;Miles_per_Gallon&quot;: 36.4, &quot;Cylinders&quot;: 5, &quot;Displacement&quot;: 121.0, &quot;Horsepower&quot;: 67.0, &quot;Weight_in_lbs&quot;: 2950, &quot;Acceleration&quot;: 19.9, &quot;Year&quot;: &quot;1980-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;Europe&quot;}, {&quot;Name&quot;: &quot;mercedes-benz 240d&quot;, &quot;Miles_per_Gallon&quot;: 30.0, &quot;Cylinders&quot;: 4, &quot;Displacement&quot;: 146.0, &quot;Horsepower&quot;: 67.0, &quot;Weight_in_lbs&quot;: 3250, &quot;Acceleration&quot;: 21.8, &quot;Year&quot;: &quot;1980-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;Europe&quot;}, {&quot;Name&quot;: &quot;honda civic 1500 gl&quot;, &quot;Miles_per_Gallon&quot;: 44.6, &quot;Cylinders&quot;: 4, &quot;Displacement&quot;: 91.0, &quot;Horsepower&quot;: 67.0, &quot;Weight_in_lbs&quot;: 1850, &quot;Acceleration&quot;: 13.8, &quot;Year&quot;: &quot;1980-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;Japan&quot;}, {&quot;Name&quot;: &quot;renault lecar deluxe&quot;, &quot;Miles_per_Gallon&quot;: 40.9, &quot;Cylinders&quot;: 4, &quot;Displacement&quot;: 85.0, &quot;Horsepower&quot;: null, &quot;Weight_in_lbs&quot;: 1835, &quot;Acceleration&quot;: 17.3, &quot;Year&quot;: &quot;1980-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;Europe&quot;}, {&quot;Name&quot;: &quot;subaru dl&quot;, &quot;Miles_per_Gallon&quot;: 33.8, &quot;Cylinders&quot;: 4, &quot;Displacement&quot;: 97.0, &quot;Horsepower&quot;: 67.0, &quot;Weight_in_lbs&quot;: 2145, &quot;Acceleration&quot;: 18.0, &quot;Year&quot;: &quot;1980-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;Japan&quot;}, {&quot;Name&quot;: &quot;vokswagen rabbit&quot;, &quot;Miles_per_Gallon&quot;: 29.8, &quot;Cylinders&quot;: 4, &quot;Displacement&quot;: 89.0, &quot;Horsepower&quot;: 62.0, &quot;Weight_in_lbs&quot;: 1845, &quot;Acceleration&quot;: 15.3, &quot;Year&quot;: &quot;1980-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;Europe&quot;}, {&quot;Name&quot;: &quot;datsun 280-zx&quot;, &quot;Miles_per_Gallon&quot;: 32.7, &quot;Cylinders&quot;: 6, &quot;Displacement&quot;: 168.0, &quot;Horsepower&quot;: 132.0, &quot;Weight_in_lbs&quot;: 2910, &quot;Acceleration&quot;: 11.4, &quot;Year&quot;: &quot;1980-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;Japan&quot;}, {&quot;Name&quot;: &quot;mazda rx-7 gs&quot;, &quot;Miles_per_Gallon&quot;: 23.7, &quot;Cylinders&quot;: 3, &quot;Displacement&quot;: 70.0, &quot;Horsepower&quot;: 100.0, &quot;Weight_in_lbs&quot;: 2420, &quot;Acceleration&quot;: 12.5, &quot;Year&quot;: &quot;1980-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;Japan&quot;}, {&quot;Name&quot;: &quot;triumph tr7 coupe&quot;, &quot;Miles_per_Gallon&quot;: 35.0, &quot;Cylinders&quot;: 4, &quot;Displacement&quot;: 122.0, &quot;Horsepower&quot;: 88.0, &quot;Weight_in_lbs&quot;: 2500, &quot;Acceleration&quot;: 15.1, &quot;Year&quot;: &quot;1980-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;Europe&quot;}, {&quot;Name&quot;: &quot;ford mustang cobra&quot;, &quot;Miles_per_Gallon&quot;: 23.6, &quot;Cylinders&quot;: 4, &quot;Displacement&quot;: 140.0, &quot;Horsepower&quot;: null, &quot;Weight_in_lbs&quot;: 2905, &quot;Acceleration&quot;: 14.3, &quot;Year&quot;: &quot;1980-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;USA&quot;}, {&quot;Name&quot;: &quot;honda Accelerationord&quot;, &quot;Miles_per_Gallon&quot;: 32.4, &quot;Cylinders&quot;: 4, &quot;Displacement&quot;: 107.0, &quot;Horsepower&quot;: 72.0, &quot;Weight_in_lbs&quot;: 2290, &quot;Acceleration&quot;: 17.0, &quot;Year&quot;: &quot;1980-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;Japan&quot;}, {&quot;Name&quot;: &quot;plymouth reliant&quot;, &quot;Miles_per_Gallon&quot;: 27.2, &quot;Cylinders&quot;: 4, &quot;Displacement&quot;: 135.0, &quot;Horsepower&quot;: 84.0, &quot;Weight_in_lbs&quot;: 2490, &quot;Acceleration&quot;: 15.7, &quot;Year&quot;: &quot;1982-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;USA&quot;}, {&quot;Name&quot;: &quot;buick skylark&quot;, &quot;Miles_per_Gallon&quot;: 26.6, &quot;Cylinders&quot;: 4, &quot;Displacement&quot;: 151.0, &quot;Horsepower&quot;: 84.0, &quot;Weight_in_lbs&quot;: 2635, &quot;Acceleration&quot;: 16.4, &quot;Year&quot;: &quot;1982-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;USA&quot;}, {&quot;Name&quot;: &quot;dodge aries wagon (sw)&quot;, &quot;Miles_per_Gallon&quot;: 25.8, &quot;Cylinders&quot;: 4, &quot;Displacement&quot;: 156.0, &quot;Horsepower&quot;: 92.0, &quot;Weight_in_lbs&quot;: 2620, &quot;Acceleration&quot;: 14.4, &quot;Year&quot;: &quot;1982-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;USA&quot;}, {&quot;Name&quot;: &quot;chevrolet citation&quot;, &quot;Miles_per_Gallon&quot;: 23.5, &quot;Cylinders&quot;: 6, &quot;Displacement&quot;: 173.0, &quot;Horsepower&quot;: 110.0, &quot;Weight_in_lbs&quot;: 2725, &quot;Acceleration&quot;: 12.6, &quot;Year&quot;: &quot;1982-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;USA&quot;}, {&quot;Name&quot;: &quot;plymouth reliant&quot;, &quot;Miles_per_Gallon&quot;: 30.0, &quot;Cylinders&quot;: 4, &quot;Displacement&quot;: 135.0, &quot;Horsepower&quot;: 84.0, &quot;Weight_in_lbs&quot;: 2385, &quot;Acceleration&quot;: 12.9, &quot;Year&quot;: &quot;1982-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;USA&quot;}, {&quot;Name&quot;: &quot;toyota starlet&quot;, &quot;Miles_per_Gallon&quot;: 39.1, &quot;Cylinders&quot;: 4, &quot;Displacement&quot;: 79.0, &quot;Horsepower&quot;: 58.0, &quot;Weight_in_lbs&quot;: 1755, &quot;Acceleration&quot;: 16.9, &quot;Year&quot;: &quot;1982-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;Japan&quot;}, {&quot;Name&quot;: &quot;plymouth champ&quot;, &quot;Miles_per_Gallon&quot;: 39.0, &quot;Cylinders&quot;: 4, &quot;Displacement&quot;: 86.0, &quot;Horsepower&quot;: 64.0, &quot;Weight_in_lbs&quot;: 1875, &quot;Acceleration&quot;: 16.4, &quot;Year&quot;: &quot;1982-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;USA&quot;}, {&quot;Name&quot;: &quot;honda civic 1300&quot;, &quot;Miles_per_Gallon&quot;: 35.1, &quot;Cylinders&quot;: 4, &quot;Displacement&quot;: 81.0, &quot;Horsepower&quot;: 60.0, &quot;Weight_in_lbs&quot;: 1760, &quot;Acceleration&quot;: 16.1, &quot;Year&quot;: &quot;1982-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;Japan&quot;}, {&quot;Name&quot;: &quot;subaru&quot;, &quot;Miles_per_Gallon&quot;: 32.3, &quot;Cylinders&quot;: 4, &quot;Displacement&quot;: 97.0, &quot;Horsepower&quot;: 67.0, &quot;Weight_in_lbs&quot;: 2065, &quot;Acceleration&quot;: 17.8, &quot;Year&quot;: &quot;1982-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;Japan&quot;}, {&quot;Name&quot;: &quot;datsun 210&quot;, &quot;Miles_per_Gallon&quot;: 37.0, &quot;Cylinders&quot;: 4, &quot;Displacement&quot;: 85.0, &quot;Horsepower&quot;: 65.0, &quot;Weight_in_lbs&quot;: 1975, &quot;Acceleration&quot;: 19.4, &quot;Year&quot;: &quot;1982-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;Japan&quot;}, {&quot;Name&quot;: &quot;toyota tercel&quot;, &quot;Miles_per_Gallon&quot;: 37.7, &quot;Cylinders&quot;: 4, &quot;Displacement&quot;: 89.0, &quot;Horsepower&quot;: 62.0, &quot;Weight_in_lbs&quot;: 2050, &quot;Acceleration&quot;: 17.3, &quot;Year&quot;: &quot;1982-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;Japan&quot;}, {&quot;Name&quot;: &quot;mazda glc 4&quot;, &quot;Miles_per_Gallon&quot;: 34.1, &quot;Cylinders&quot;: 4, &quot;Displacement&quot;: 91.0, &quot;Horsepower&quot;: 68.0, &quot;Weight_in_lbs&quot;: 1985, &quot;Acceleration&quot;: 16.0, &quot;Year&quot;: &quot;1982-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;Japan&quot;}, {&quot;Name&quot;: &quot;plymouth horizon 4&quot;, &quot;Miles_per_Gallon&quot;: 34.7, &quot;Cylinders&quot;: 4, &quot;Displacement&quot;: 105.0, &quot;Horsepower&quot;: 63.0, &quot;Weight_in_lbs&quot;: 2215, &quot;Acceleration&quot;: 14.9, &quot;Year&quot;: &quot;1982-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;USA&quot;}, {&quot;Name&quot;: &quot;ford escort 4w&quot;, &quot;Miles_per_Gallon&quot;: 34.4, &quot;Cylinders&quot;: 4, &quot;Displacement&quot;: 98.0, &quot;Horsepower&quot;: 65.0, &quot;Weight_in_lbs&quot;: 2045, &quot;Acceleration&quot;: 16.2, &quot;Year&quot;: &quot;1982-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;USA&quot;}, {&quot;Name&quot;: &quot;ford escort 2h&quot;, &quot;Miles_per_Gallon&quot;: 29.9, &quot;Cylinders&quot;: 4, &quot;Displacement&quot;: 98.0, &quot;Horsepower&quot;: 65.0, &quot;Weight_in_lbs&quot;: 2380, &quot;Acceleration&quot;: 20.7, &quot;Year&quot;: &quot;1982-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;USA&quot;}, {&quot;Name&quot;: &quot;volkswagen jetta&quot;, &quot;Miles_per_Gallon&quot;: 33.0, &quot;Cylinders&quot;: 4, &quot;Displacement&quot;: 105.0, &quot;Horsepower&quot;: 74.0, &quot;Weight_in_lbs&quot;: 2190, &quot;Acceleration&quot;: 14.2, &quot;Year&quot;: &quot;1982-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;Europe&quot;}, {&quot;Name&quot;: &quot;renault 18i&quot;, &quot;Miles_per_Gallon&quot;: 34.5, &quot;Cylinders&quot;: 4, &quot;Displacement&quot;: 100.0, &quot;Horsepower&quot;: null, &quot;Weight_in_lbs&quot;: 2320, &quot;Acceleration&quot;: 15.8, &quot;Year&quot;: &quot;1982-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;Europe&quot;}, {&quot;Name&quot;: &quot;honda prelude&quot;, &quot;Miles_per_Gallon&quot;: 33.7, &quot;Cylinders&quot;: 4, &quot;Displacement&quot;: 107.0, &quot;Horsepower&quot;: 75.0, &quot;Weight_in_lbs&quot;: 2210, &quot;Acceleration&quot;: 14.4, &quot;Year&quot;: &quot;1982-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;Japan&quot;}, {&quot;Name&quot;: &quot;toyota corolla&quot;, &quot;Miles_per_Gallon&quot;: 32.4, &quot;Cylinders&quot;: 4, &quot;Displacement&quot;: 108.0, &quot;Horsepower&quot;: 75.0, &quot;Weight_in_lbs&quot;: 2350, &quot;Acceleration&quot;: 16.8, &quot;Year&quot;: &quot;1982-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;Japan&quot;}, {&quot;Name&quot;: &quot;datsun 200sx&quot;, &quot;Miles_per_Gallon&quot;: 32.9, &quot;Cylinders&quot;: 4, &quot;Displacement&quot;: 119.0, &quot;Horsepower&quot;: 100.0, &quot;Weight_in_lbs&quot;: 2615, &quot;Acceleration&quot;: 14.8, &quot;Year&quot;: &quot;1982-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;Japan&quot;}, {&quot;Name&quot;: &quot;mazda 626&quot;, &quot;Miles_per_Gallon&quot;: 31.6, &quot;Cylinders&quot;: 4, &quot;Displacement&quot;: 120.0, &quot;Horsepower&quot;: 74.0, &quot;Weight_in_lbs&quot;: 2635, &quot;Acceleration&quot;: 18.3, &quot;Year&quot;: &quot;1982-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;Japan&quot;}, {&quot;Name&quot;: &quot;peugeot 505s turbo diesel&quot;, &quot;Miles_per_Gallon&quot;: 28.1, &quot;Cylinders&quot;: 4, &quot;Displacement&quot;: 141.0, &quot;Horsepower&quot;: 80.0, &quot;Weight_in_lbs&quot;: 3230, &quot;Acceleration&quot;: 20.4, &quot;Year&quot;: &quot;1982-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;Europe&quot;}, {&quot;Name&quot;: &quot;saab 900s&quot;, &quot;Miles_per_Gallon&quot;: null, &quot;Cylinders&quot;: 4, &quot;Displacement&quot;: 121.0, &quot;Horsepower&quot;: 110.0, &quot;Weight_in_lbs&quot;: 2800, &quot;Acceleration&quot;: 15.4, &quot;Year&quot;: &quot;1982-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;Europe&quot;}, {&quot;Name&quot;: &quot;volvo diesel&quot;, &quot;Miles_per_Gallon&quot;: 30.7, &quot;Cylinders&quot;: 6, &quot;Displacement&quot;: 145.0, &quot;Horsepower&quot;: 76.0, &quot;Weight_in_lbs&quot;: 3160, &quot;Acceleration&quot;: 19.6, &quot;Year&quot;: &quot;1982-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;Europe&quot;}, {&quot;Name&quot;: &quot;toyota cressida&quot;, &quot;Miles_per_Gallon&quot;: 25.4, &quot;Cylinders&quot;: 6, &quot;Displacement&quot;: 168.0, &quot;Horsepower&quot;: 116.0, &quot;Weight_in_lbs&quot;: 2900, &quot;Acceleration&quot;: 12.6, &quot;Year&quot;: &quot;1982-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;Japan&quot;}, {&quot;Name&quot;: &quot;datsun 810 maxima&quot;, &quot;Miles_per_Gallon&quot;: 24.2, &quot;Cylinders&quot;: 6, &quot;Displacement&quot;: 146.0, &quot;Horsepower&quot;: 120.0, &quot;Weight_in_lbs&quot;: 2930, &quot;Acceleration&quot;: 13.8, &quot;Year&quot;: &quot;1982-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;Japan&quot;}, {&quot;Name&quot;: &quot;buick century&quot;, &quot;Miles_per_Gallon&quot;: 22.4, &quot;Cylinders&quot;: 6, &quot;Displacement&quot;: 231.0, &quot;Horsepower&quot;: 110.0, &quot;Weight_in_lbs&quot;: 3415, &quot;Acceleration&quot;: 15.8, &quot;Year&quot;: &quot;1982-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;USA&quot;}, {&quot;Name&quot;: &quot;oldsmobile cutlass ls&quot;, &quot;Miles_per_Gallon&quot;: 26.6, &quot;Cylinders&quot;: 8, &quot;Displacement&quot;: 350.0, &quot;Horsepower&quot;: 105.0, &quot;Weight_in_lbs&quot;: 3725, &quot;Acceleration&quot;: 19.0, &quot;Year&quot;: &quot;1982-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;USA&quot;}, {&quot;Name&quot;: &quot;ford granada gl&quot;, &quot;Miles_per_Gallon&quot;: 20.2, &quot;Cylinders&quot;: 6, &quot;Displacement&quot;: 200.0, &quot;Horsepower&quot;: 88.0, &quot;Weight_in_lbs&quot;: 3060, &quot;Acceleration&quot;: 17.1, &quot;Year&quot;: &quot;1982-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;USA&quot;}, {&quot;Name&quot;: &quot;chrysler lebaron salon&quot;, &quot;Miles_per_Gallon&quot;: 17.6, &quot;Cylinders&quot;: 6, &quot;Displacement&quot;: 225.0, &quot;Horsepower&quot;: 85.0, &quot;Weight_in_lbs&quot;: 3465, &quot;Acceleration&quot;: 16.6, &quot;Year&quot;: &quot;1982-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;USA&quot;}, {&quot;Name&quot;: &quot;chevrolet cavalier&quot;, &quot;Miles_per_Gallon&quot;: 28.0, &quot;Cylinders&quot;: 4, &quot;Displacement&quot;: 112.0, &quot;Horsepower&quot;: 88.0, &quot;Weight_in_lbs&quot;: 2605, &quot;Acceleration&quot;: 19.6, &quot;Year&quot;: &quot;1982-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;USA&quot;}, {&quot;Name&quot;: &quot;chevrolet cavalier wagon&quot;, &quot;Miles_per_Gallon&quot;: 27.0, &quot;Cylinders&quot;: 4, &quot;Displacement&quot;: 112.0, &quot;Horsepower&quot;: 88.0, &quot;Weight_in_lbs&quot;: 2640, &quot;Acceleration&quot;: 18.6, &quot;Year&quot;: &quot;1982-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;USA&quot;}, {&quot;Name&quot;: &quot;chevrolet cavalier 2-door&quot;, &quot;Miles_per_Gallon&quot;: 34.0, &quot;Cylinders&quot;: 4, &quot;Displacement&quot;: 112.0, &quot;Horsepower&quot;: 88.0, &quot;Weight_in_lbs&quot;: 2395, &quot;Acceleration&quot;: 18.0, &quot;Year&quot;: &quot;1982-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;USA&quot;}, {&quot;Name&quot;: &quot;pontiac j2000 se hatchback&quot;, &quot;Miles_per_Gallon&quot;: 31.0, &quot;Cylinders&quot;: 4, &quot;Displacement&quot;: 112.0, &quot;Horsepower&quot;: 85.0, &quot;Weight_in_lbs&quot;: 2575, &quot;Acceleration&quot;: 16.2, &quot;Year&quot;: &quot;1982-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;USA&quot;}, {&quot;Name&quot;: &quot;dodge aries se&quot;, &quot;Miles_per_Gallon&quot;: 29.0, &quot;Cylinders&quot;: 4, &quot;Displacement&quot;: 135.0, &quot;Horsepower&quot;: 84.0, &quot;Weight_in_lbs&quot;: 2525, &quot;Acceleration&quot;: 16.0, &quot;Year&quot;: &quot;1982-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;USA&quot;}, {&quot;Name&quot;: &quot;pontiac phoenix&quot;, &quot;Miles_per_Gallon&quot;: 27.0, &quot;Cylinders&quot;: 4, &quot;Displacement&quot;: 151.0, &quot;Horsepower&quot;: 90.0, &quot;Weight_in_lbs&quot;: 2735, &quot;Acceleration&quot;: 18.0, &quot;Year&quot;: &quot;1982-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;USA&quot;}, {&quot;Name&quot;: &quot;ford fairmont futura&quot;, &quot;Miles_per_Gallon&quot;: 24.0, &quot;Cylinders&quot;: 4, &quot;Displacement&quot;: 140.0, &quot;Horsepower&quot;: 92.0, &quot;Weight_in_lbs&quot;: 2865, &quot;Acceleration&quot;: 16.4, &quot;Year&quot;: &quot;1982-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;USA&quot;}, {&quot;Name&quot;: &quot;amc concord dl&quot;, &quot;Miles_per_Gallon&quot;: 23.0, &quot;Cylinders&quot;: 4, &quot;Displacement&quot;: 151.0, &quot;Horsepower&quot;: null, &quot;Weight_in_lbs&quot;: 3035, &quot;Acceleration&quot;: 20.5, &quot;Year&quot;: &quot;1982-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;USA&quot;}, {&quot;Name&quot;: &quot;volkswagen rabbit l&quot;, &quot;Miles_per_Gallon&quot;: 36.0, &quot;Cylinders&quot;: 4, &quot;Displacement&quot;: 105.0, &quot;Horsepower&quot;: 74.0, &quot;Weight_in_lbs&quot;: 1980, &quot;Acceleration&quot;: 15.3, &quot;Year&quot;: &quot;1982-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;Europe&quot;}, {&quot;Name&quot;: &quot;mazda glc custom l&quot;, &quot;Miles_per_Gallon&quot;: 37.0, &quot;Cylinders&quot;: 4, &quot;Displacement&quot;: 91.0, &quot;Horsepower&quot;: 68.0, &quot;Weight_in_lbs&quot;: 2025, &quot;Acceleration&quot;: 18.2, &quot;Year&quot;: &quot;1982-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;Japan&quot;}, {&quot;Name&quot;: &quot;mazda glc custom&quot;, &quot;Miles_per_Gallon&quot;: 31.0, &quot;Cylinders&quot;: 4, &quot;Displacement&quot;: 91.0, &quot;Horsepower&quot;: 68.0, &quot;Weight_in_lbs&quot;: 1970, &quot;Acceleration&quot;: 17.6, &quot;Year&quot;: &quot;1982-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;Japan&quot;}, {&quot;Name&quot;: &quot;plymouth horizon miser&quot;, &quot;Miles_per_Gallon&quot;: 38.0, &quot;Cylinders&quot;: 4, &quot;Displacement&quot;: 105.0, &quot;Horsepower&quot;: 63.0, &quot;Weight_in_lbs&quot;: 2125, &quot;Acceleration&quot;: 14.7, &quot;Year&quot;: &quot;1982-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;USA&quot;}, {&quot;Name&quot;: &quot;mercury lynx l&quot;, &quot;Miles_per_Gallon&quot;: 36.0, &quot;Cylinders&quot;: 4, &quot;Displacement&quot;: 98.0, &quot;Horsepower&quot;: 70.0, &quot;Weight_in_lbs&quot;: 2125, &quot;Acceleration&quot;: 17.3, &quot;Year&quot;: &quot;1982-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;USA&quot;}, {&quot;Name&quot;: &quot;nissan stanza xe&quot;, &quot;Miles_per_Gallon&quot;: 36.0, &quot;Cylinders&quot;: 4, &quot;Displacement&quot;: 120.0, &quot;Horsepower&quot;: 88.0, &quot;Weight_in_lbs&quot;: 2160, &quot;Acceleration&quot;: 14.5, &quot;Year&quot;: &quot;1982-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;Japan&quot;}, {&quot;Name&quot;: &quot;honda Accelerationord&quot;, &quot;Miles_per_Gallon&quot;: 36.0, &quot;Cylinders&quot;: 4, &quot;Displacement&quot;: 107.0, &quot;Horsepower&quot;: 75.0, &quot;Weight_in_lbs&quot;: 2205, &quot;Acceleration&quot;: 14.5, &quot;Year&quot;: &quot;1982-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;Japan&quot;}, {&quot;Name&quot;: &quot;toyota corolla&quot;, &quot;Miles_per_Gallon&quot;: 34.0, &quot;Cylinders&quot;: 4, &quot;Displacement&quot;: 108.0, &quot;Horsepower&quot;: 70.0, &quot;Weight_in_lbs&quot;: 2245, &quot;Acceleration&quot;: 16.9, &quot;Year&quot;: &quot;1982-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;Japan&quot;}, {&quot;Name&quot;: &quot;honda civic&quot;, &quot;Miles_per_Gallon&quot;: 38.0, &quot;Cylinders&quot;: 4, &quot;Displacement&quot;: 91.0, &quot;Horsepower&quot;: 67.0, &quot;Weight_in_lbs&quot;: 1965, &quot;Acceleration&quot;: 15.0, &quot;Year&quot;: &quot;1982-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;Japan&quot;}, {&quot;Name&quot;: &quot;honda civic (auto)&quot;, &quot;Miles_per_Gallon&quot;: 32.0, &quot;Cylinders&quot;: 4, &quot;Displacement&quot;: 91.0, &quot;Horsepower&quot;: 67.0, &quot;Weight_in_lbs&quot;: 1965, &quot;Acceleration&quot;: 15.7, &quot;Year&quot;: &quot;1982-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;Japan&quot;}, {&quot;Name&quot;: &quot;datsun 310 gx&quot;, &quot;Miles_per_Gallon&quot;: 38.0, &quot;Cylinders&quot;: 4, &quot;Displacement&quot;: 91.0, &quot;Horsepower&quot;: 67.0, &quot;Weight_in_lbs&quot;: 1995, &quot;Acceleration&quot;: 16.2, &quot;Year&quot;: &quot;1982-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;Japan&quot;}, {&quot;Name&quot;: &quot;buick century limited&quot;, &quot;Miles_per_Gallon&quot;: 25.0, &quot;Cylinders&quot;: 6, &quot;Displacement&quot;: 181.0, &quot;Horsepower&quot;: 110.0, &quot;Weight_in_lbs&quot;: 2945, &quot;Acceleration&quot;: 16.4, &quot;Year&quot;: &quot;1982-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;USA&quot;}, {&quot;Name&quot;: &quot;oldsmobile cutlass ciera (diesel)&quot;, &quot;Miles_per_Gallon&quot;: 38.0, &quot;Cylinders&quot;: 6, &quot;Displacement&quot;: 262.0, &quot;Horsepower&quot;: 85.0, &quot;Weight_in_lbs&quot;: 3015, &quot;Acceleration&quot;: 17.0, &quot;Year&quot;: &quot;1982-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;USA&quot;}, {&quot;Name&quot;: &quot;chrysler lebaron medallion&quot;, &quot;Miles_per_Gallon&quot;: 26.0, &quot;Cylinders&quot;: 4, &quot;Displacement&quot;: 156.0, &quot;Horsepower&quot;: 92.0, &quot;Weight_in_lbs&quot;: 2585, &quot;Acceleration&quot;: 14.5, &quot;Year&quot;: &quot;1982-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;USA&quot;}, {&quot;Name&quot;: &quot;ford granada l&quot;, &quot;Miles_per_Gallon&quot;: 22.0, &quot;Cylinders&quot;: 6, &quot;Displacement&quot;: 232.0, &quot;Horsepower&quot;: 112.0, &quot;Weight_in_lbs&quot;: 2835, &quot;Acceleration&quot;: 14.7, &quot;Year&quot;: &quot;1982-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;USA&quot;}, {&quot;Name&quot;: &quot;toyota celica gt&quot;, &quot;Miles_per_Gallon&quot;: 32.0, &quot;Cylinders&quot;: 4, &quot;Displacement&quot;: 144.0, &quot;Horsepower&quot;: 96.0, &quot;Weight_in_lbs&quot;: 2665, &quot;Acceleration&quot;: 13.9, &quot;Year&quot;: &quot;1982-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;Japan&quot;}, {&quot;Name&quot;: &quot;dodge charger 2.2&quot;, &quot;Miles_per_Gallon&quot;: 36.0, &quot;Cylinders&quot;: 4, &quot;Displacement&quot;: 135.0, &quot;Horsepower&quot;: 84.0, &quot;Weight_in_lbs&quot;: 2370, &quot;Acceleration&quot;: 13.0, &quot;Year&quot;: &quot;1982-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;USA&quot;}, {&quot;Name&quot;: &quot;chevrolet camaro&quot;, &quot;Miles_per_Gallon&quot;: 27.0, &quot;Cylinders&quot;: 4, &quot;Displacement&quot;: 151.0, &quot;Horsepower&quot;: 90.0, &quot;Weight_in_lbs&quot;: 2950, &quot;Acceleration&quot;: 17.3, &quot;Year&quot;: &quot;1982-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;USA&quot;}, {&quot;Name&quot;: &quot;ford mustang gl&quot;, &quot;Miles_per_Gallon&quot;: 27.0, &quot;Cylinders&quot;: 4, &quot;Displacement&quot;: 140.0, &quot;Horsepower&quot;: 86.0, &quot;Weight_in_lbs&quot;: 2790, &quot;Acceleration&quot;: 15.6, &quot;Year&quot;: &quot;1982-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;USA&quot;}, {&quot;Name&quot;: &quot;vw pickup&quot;, &quot;Miles_per_Gallon&quot;: 44.0, &quot;Cylinders&quot;: 4, &quot;Displacement&quot;: 97.0, &quot;Horsepower&quot;: 52.0, &quot;Weight_in_lbs&quot;: 2130, &quot;Acceleration&quot;: 24.6, &quot;Year&quot;: &quot;1982-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;Europe&quot;}, {&quot;Name&quot;: &quot;dodge rampage&quot;, &quot;Miles_per_Gallon&quot;: 32.0, &quot;Cylinders&quot;: 4, &quot;Displacement&quot;: 135.0, &quot;Horsepower&quot;: 84.0, &quot;Weight_in_lbs&quot;: 2295, &quot;Acceleration&quot;: 11.6, &quot;Year&quot;: &quot;1982-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;USA&quot;}, {&quot;Name&quot;: &quot;ford ranger&quot;, &quot;Miles_per_Gallon&quot;: 28.0, &quot;Cylinders&quot;: 4, &quot;Displacement&quot;: 120.0, &quot;Horsepower&quot;: 79.0, &quot;Weight_in_lbs&quot;: 2625, &quot;Acceleration&quot;: 18.6, &quot;Year&quot;: &quot;1982-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;USA&quot;}, {&quot;Name&quot;: &quot;chevy s-10&quot;, &quot;Miles_per_Gallon&quot;: 31.0, &quot;Cylinders&quot;: 4, &quot;Displacement&quot;: 119.0, &quot;Horsepower&quot;: 82.0, &quot;Weight_in_lbs&quot;: 2720, &quot;Acceleration&quot;: 19.4, &quot;Year&quot;: &quot;1982-01-01T00:00:00&quot;, &quot;Origin&quot;: &quot;USA&quot;}]}}, {&quot;mode&quot;: &quot;vega-lite&quot;});*
#### [Book Review - In the Service of Republic](https:&#x2F;&#x2F;sureshshanmugam.com&#x2F;articles&#x2F;service-republic-review&#x2F;) 
*Here are some interesting parallels between business &amp; politics
I’ve been reading this great book on why India fails to get policy decisions often wrong and how to go about building that capacity at various levels of public institutions.
This advice is crystallised for me in the comparison between an enterprise and a political party.
In the world of business, there is a balance between building a great product and selling it on the market. An extreme emphasis on a sales and advertising team can yield a brief surge of customer interest, but this doesn’t translate into sustained success if the product is not of high quality and the machinery of production and distribution is not in place. In other words, a firm needs not just sales and advertising, it also needs research, design and operations management. It needs a great product and the capability to produce and distribute the product, on top of which the sales and advertising offensive is essential.
While politics is about elections, the parallel between overt focus on growth is the very problem that is taking a toll on technology companies and political parties in India.
There is an analogy with the world of politics, running an election campaign is analogous to the sales and advertising problem. Political parties need to prepare to govern, alongside  campaigning to get elected. Once the election results are in, everyday lost in establishing the team and kicking off a portfolio of reforms is a costly delay.
This book has interesting analytical clarity - especially when looking at topics on education, healthcare and financial industry.
Here is the link to book on Amazon
Book

this is an affiliate link and would lead me to earn commissions.*
#### [Publishing Jupyter Notebooks on Github Pages](https:&#x2F;&#x2F;sureshshanmugam.com&#x2F;articles&#x2F;publish-jupyter-notebooks&#x2F;) 
*Publishing Jupyter Notebooks on GitHub
Converting Jupyter notebooks into markdown
I’ve been looking for ways to publish Jupyter notebook based analysis into this blog. This post explains a process that I’ve come to use in creating these blog posts.
This method allows inclusion of styled cell input and output, including graphs. Whe you have completed your iPython notebook (sample_notebook.ipynb in this case), run the following command in your terminal to convert your notebook file into markdown.




1

$ jupyter nbconvert sample_notebook.ipynb --to markdown




Add markdown to Jekyll
For notebooks with text and code this approach works fine. There are couple more steps to get images and plots incorporated into these posts. The Markdown doc expects these PNGs so be in the same folder as the doc, but Jekyll works with a separate &#x2F;assets&#x2F;… folder, as is more common for websites. It would need a some scripting to fix this path difference. I also do like the Jupyter Notebook style, so it would be nice not to go through Markdown and lose all that.*
#### [Example Post](https:&#x2F;&#x2F;sureshshanmugam.com&#x2F;articles&#x2F;example-post&#x2F;) 
*Howdy! This is an example blog post that shows several types of HTML content supported in this theme.


Cum sociis natoque penatibus et magnis dis parturient montes, nascetur ridiculus mus. Aenean eu leo quam. Pellentesque ornare sem lacinia quam venenatis vestibulum. Sed posuere consectetur est at lobortis. Cras mattis consectetur purus sit amet fermentum.
Curabitur blandit tempus porttitor. Nullam quis risus eget urna mollis ornare vel eu leo. Nullam id dolor id nibh ultricies vehicula ut id elit.
Etiam porta sem malesuada magna mollis euismod. Cras mattis consectetur purus sit amet fermentum. Aenean lacinia bibendum nulla sed consectetur.
Inline HTML elements
HTML defines a long list of available inline tags, a complete list of which can be found on the Mozilla Developer Network.
To bold text, use &lt;strong&gt;.
To italicize text, use &lt;em&gt;.
Abbreviations, like HTML should use &lt;abbr&gt;, with an optional title attribute for the full phrase.
Citations, like — Mark otto, should use &lt;cite&gt;.
Deleted text should use &lt;del&gt; and inserted text should use &lt;ins&gt;.
Superscript text uses &lt;sup&gt; and subscript text uses &lt;sub&gt;.
Most of these elements are styled by browsers with few modifications on our part.
Heading
Vivamus sagittis lacus vel augue rutrum faucibus dolor auctor. Duis mollis, est non commodo luctus, nisi erat porttitor ligula, eget lacinia odio sem nec elit. Morbi leo risus, porta ac consectetur ac, vestibulum at eros.
Code
Cum sociis natoque penatibus et magnis dis code element montes, nascetur ridiculus mus.
&#x2F;&#x2F; Example can be run directly in your JavaScript console

&#x2F;&#x2F; Create a function that takes two arguments and returns the sum of those arguments
var adder &#x3D; new Function(&quot;a&quot;, &quot;b&quot;, &quot;return a + b&quot;);

&#x2F;&#x2F; Call the function
adder(2, 6);
&#x2F;&#x2F; &gt; 8


Aenean lacinia bibendum nulla sed consectetur. Etiam porta sem malesuada magna mollis euismod. Fusce dapibus, tellus ac cursus commodo, tortor mauris condimentum nibh, ut fermentum massa.
Gists via GitHub Pages
Vestibulum id ligula porta felis euismod semper. Nullam quis risus eget urna mollis ornare vel eu leo. Donec sed odio dui.
 

Aenean eu leo quam. Pellentesque ornare sem lacinia quam venenatis vestibulum. Nullam quis risus eget urna mollis ornare vel eu leo. Cum sociis natoque penatibus et magnis dis parturient montes, nascetur ridiculus mus. Donec sed odio dui. Vestibulum id ligula porta felis euismod semper.
Lists
Cum sociis natoque penatibus et magnis dis parturient montes, nascetur ridiculus mus. Aenean lacinia bibendum nulla sed consectetur. Etiam porta sem malesuada magna mollis euismod. Fusce dapibus, tellus ac cursus commodo, tortor mauris condimentum nibh, ut fermentum massa justo sit amet risus.
Praesent commodo cursus magna, vel scelerisque nisl consectetur et.
Donec id elit non mi porta gravida at eget metus.
Nulla vitae elit libero, a pharetra augue.
Donec ullamcorper nulla non metus auctor fringilla. Nulla vitae elit libero, a pharetra augue.
Vestibulum id ligula porta felis euismod semper.
Cum sociis natoque penatibus et magnis dis parturient montes, nascetur ridiculus mus.
Maecenas sed diam eget risus varius blandit sit amet non magna.
Cras mattis consectetur purus sit amet fermentum. Sed posuere consectetur est at lobortis.
HyperText Markup Language (HTML)
  The language used to describe and define the content of a Web page

  Cascading Style Sheets (CSS)
  Used to describe the appearance of Web content

  JavaScript (JS)
  The programming language used to build advanced Web sites and applications


Integer posuere erat a ante venenatis dapibus posuere velit aliquet. Morbi leo risus, porta ac consectetur ac, vestibulum at eros. Nullam quis risus eget urna mollis ornare vel eu leo.
Images
Quisque consequat sapien eget quam rhoncus, sit amet laoreet diam tempus. Aliquam aliquam metus erat, a pulvinar turpis suscipit at.



Tables
Aenean lacinia bibendum nulla sed consectetur. Lorem ipsum dolor sit amet, consectetur adipiscing elit.
Name
      Upvotes
      Downvotes
    
Totals
      21
      23
    
Alice
      10
      11
    
Bob
      4
      3
    
Charlie
      7
      9
    
Nullam id dolor id nibh ultricies vehicula ut id elit. Sed posuere consectetur est at lobortis. Nullam quis risus eget urna mollis ornare vel eu leo.
Want to see something else added? Open an issue.*
#### [Introduction to timeseries plots in Python](https:&#x2F;&#x2F;sureshshanmugam.com&#x2F;articles&#x2F;Python-Finance&#x2F;) 
*Imports




1
2
3
4
5
6
7
8

%matplotlib inline
import pandas as pd
import numpy as np
import matplotlib.pyplot as plt
import math

from datetime import date
from nsepy import get_history








1
2
3
4
5
6
7
8
9
10
11
12
13
14
15
16
17

# NIFTY 50 index
nifty_50 &#x3D; get_history(symbol&#x3D;&quot;NIFTY 50&quot;,
                            start&#x3D;date(2001,1,1),
                            end&#x3D;date(2020,5,3),
                            index&#x3D;True)

# NIFTY Next 50 index
nifty_next50 &#x3D; get_history(symbol&#x3D;&quot;NIFTY NEXT 50&quot;,
                            start&#x3D;date(2001,1,1),
                            end&#x3D;date(2020,5,3),
                            index&#x3D;True)

# India VIX index
india_vix &#x3D; get_history(symbol&#x3D;&quot;INDIAVIX&quot;,
                            start&#x3D;date(2001,1,1),
                            end&#x3D;date(2020,5,3),
                            index&#x3D;True)








1

nifty_50.shape, nifty_next50.shape, india_vix.shape








1

((4806, 6), (4806, 6), (2796, 7))








1

MKT &#x3D; nifty_next50.join(nifty_50[&#39;Close&#39;], how&#x3D;&#39;outer&#39;, rsuffix&#x3D;&#39;_N50&#39;).dropna()








1
2
3

data &#x3D; MKT.rename(columns&#x3D;{&#39;Close&#39;:&#39;NN50&#39;,&#39;Close_N50&#39;:&#39;N50&#39;})\
            .assign(NN50_returns&#x3D;lambda x: np.log(x[&#39;NN50&#39;]&#x2F;x[&#39;NN50&#39;].shift(1)))\
            .assign(N50_returns&#x3D;lambda x: np.log(x[&#39;N50&#39;]&#x2F;x[&#39;N50&#39;].shift(1)))








1

data &#x3D; data[[&#39;NN50&#39;, &#39;N50&#39;, &#39;NN50_returns&#39;, &#39;N50_returns&#39;]].dropna()








1

data.index &#x3D; pd.DatetimeIndex(data.index)








1
2
3
4
5
6
7

# Let&#39;s plot SPX and VIX cumulative returns with recession overlay
plot_cols &#x3D; [&#39;NN50&#39;, &#39;N50&#39;]

# 2 axes for 2 subplots

fig, axes &#x3D; plt.subplots(2,1, figsize&#x3D;(10,7), sharex&#x3D;True)
data[plot_cols].plot(subplots&#x3D;True, ax&#x3D;axes)








1
2
3

array([&lt;matplotlib.axes._subplots.AxesSubplot object at 0x11b5f6610&gt;,
       &lt;matplotlib.axes._subplots.AxesSubplot object at 0x11a0cf8d0&gt;],
      dtype&#x3D;object)









1
2
3
4
5
6
7

# Let&#39;s plot SPX and VIX cumulative returns with recession overlay
plot_cols &#x3D; [&#39;NN50_returns&#39;, &#39;N50_returns&#39;]

# 2 axes for 2 subplots

fig, axes &#x3D; plt.subplots(2,1, figsize&#x3D;(10,7), sharex&#x3D;True)
data[plot_cols].plot(subplots&#x3D;True, ax&#x3D;axes)








1
2
3

array([&lt;matplotlib.axes._subplots.AxesSubplot object at 0x11669c550&gt;,
       &lt;matplotlib.axes._subplots.AxesSubplot object at 0x115ccc090&gt;],
      dtype&#x3D;object)









1
2
3
4
5
6
7
8
9
10
11
12
13
14
15
16

# &#x3D;&#x3D;&#x3D;&#x3D;&#x3D;&#x3D;&#x3D;&#x3D;&#x3D;&#x3D;&#x3D;&#x3D;&#x3D;&#x3D;&#x3D;&#x3D;&#x3D;&#x3D;&#x3D;&#x3D;&#x3D;&#x3D;&#x3D;&#x3D;&#x3D;&#x3D;&#x3D;&#x3D;&#x3D;&#x3D;&#x3D;&#x3D;&#x3D;&#x3D;&#x3D;&#x3D;&#x3D;&#x3D;&#x3D;&#x3D;&#x3D;&#x3D;&#x3D;&#x3D;&#x3D;&#x3D;&#x3D;&#x3D;&#x3D;&#x3D;&#x3D;&#x3D;&#x3D;&#x3D;&#x3D;&#x3D;&#x3D;&#x3D;&#x3D;&#x3D;&#x3D;&#x3D;&#x3D;&#x3D;&#x3D;&#x3D; #
# resample log returns weekly starting monday
lrets_resampled &#x3D; data[[&#39;NN50_returns&#39;, &#39;N50_returns&#39;]].resample(&#39;W-MON&#39;).sum()

# &#x3D;&#x3D;&#x3D;&#x3D;&#x3D;&#x3D;&#x3D;&#x3D;&#x3D;&#x3D;&#x3D;&#x3D;&#x3D;&#x3D;&#x3D;&#x3D;&#x3D;&#x3D;&#x3D;&#x3D;&#x3D;&#x3D;&#x3D;&#x3D;&#x3D;&#x3D;&#x3D;&#x3D;&#x3D;&#x3D;&#x3D;&#x3D;&#x3D;&#x3D;&#x3D;&#x3D;&#x3D;&#x3D;&#x3D;&#x3D;&#x3D;&#x3D;&#x3D;&#x3D;&#x3D;&#x3D;&#x3D;&#x3D;&#x3D;&#x3D;&#x3D;&#x3D;&#x3D;&#x3D;&#x3D;&#x3D;&#x3D;&#x3D;&#x3D;&#x3D;&#x3D;&#x3D;&#x3D;&#x3D;&#x3D;&#x3D; #
# rolling mean returns
n &#x3D; 52
roll_mean &#x3D; lrets_resampled.rolling(window&#x3D;n, min_periods&#x3D;n ).mean().dropna(axis&#x3D;0,how&#x3D;&#39;all&#39;)

# &#x3D;&#x3D;&#x3D;&#x3D;&#x3D;&#x3D;&#x3D;&#x3D;&#x3D;&#x3D;&#x3D;&#x3D;&#x3D;&#x3D;&#x3D;&#x3D;&#x3D;&#x3D;&#x3D;&#x3D;&#x3D;&#x3D;&#x3D;&#x3D;&#x3D;&#x3D;&#x3D;&#x3D;&#x3D;&#x3D;&#x3D;&#x3D;&#x3D;&#x3D;&#x3D;&#x3D;&#x3D;&#x3D;&#x3D;&#x3D;&#x3D;&#x3D;&#x3D;&#x3D;&#x3D;&#x3D;&#x3D;&#x3D;&#x3D;&#x3D;&#x3D;&#x3D;&#x3D;&#x3D;&#x3D;&#x3D;&#x3D;&#x3D;&#x3D;&#x3D;&#x3D;&#x3D;&#x3D;&#x3D;&#x3D;&#x3D; #
# rolling sigmas
roll_sigs &#x3D; lrets_resampled.rolling(window&#x3D;n, min_periods&#x3D;n ).std().dropna(axis&#x3D;0,how&#x3D;&#39;all&#39;) * math.sqrt(n)

# &#x3D;&#x3D;&#x3D;&#x3D;&#x3D;&#x3D;&#x3D;&#x3D;&#x3D;&#x3D;&#x3D;&#x3D;&#x3D;&#x3D;&#x3D;&#x3D;&#x3D;&#x3D;&#x3D;&#x3D;&#x3D;&#x3D;&#x3D;&#x3D;&#x3D;&#x3D;&#x3D;&#x3D;&#x3D;&#x3D;&#x3D;&#x3D;&#x3D;&#x3D;&#x3D;&#x3D;&#x3D;&#x3D;&#x3D;&#x3D;&#x3D;&#x3D;&#x3D;&#x3D;&#x3D;&#x3D;&#x3D;&#x3D;&#x3D;&#x3D;&#x3D;&#x3D;&#x3D;&#x3D;&#x3D;&#x3D;&#x3D;&#x3D;&#x3D;&#x3D;&#x3D;&#x3D;&#x3D;&#x3D;&#x3D;&#x3D; #
# rolling risk adjusted returns 
roll_risk_rets &#x3D; roll_mean&#x2F;roll_sigs








1
2
3
4
5
6
7

# Let&#39;s plot SPX and VIX cumulative returns with recession overlay
plot_cols &#x3D; [&#39;NN50_returns&#39;, &#39;N50_returns&#39;]

# 2 axes for 2 subplots

fig, axes &#x3D; plt.subplots(2,1, figsize&#x3D;(10,7), sharex&#x3D;True)
roll_mean[plot_cols].plot(subplots&#x3D;True, ax&#x3D;axes)








1
2
3

array([&lt;matplotlib.axes._subplots.AxesSubplot object at 0x1165e9b50&gt;,
       &lt;matplotlib.axes._subplots.AxesSubplot object at 0x11738d190&gt;],
      dtype&#x3D;object)









1
2
3
4

data[[&#39;NN50&#39;, &#39;N50&#39;]].rolling(250).mean().head()
# \
#             .assign(NN50_returns&#x3D;lambda x: np.log(x[&#39;NN50&#39;]&#x2F;x[&#39;NN50&#39;].shift(1)))\
#             .assign(N50_returns&#x3D;lambda x: np.log(x[&#39;N50&#39;]&#x2F;x[&#39;N50&#39;].shift(1)))






      NN50
      N50
    
Date
      
      
    
2001-01-02
      NaN
      NaN
    
2001-01-03
      NaN
      NaN
    
2001-01-04
      NaN
      NaN
    
2001-01-05
      NaN
      NaN
    
2001-01-08
      NaN
      NaN
    




1
2

%load_ext watermark
%watermark








1
2
3
4
5
6
7
8
9
10
11
12
13
14

The watermark extension is already loaded. To reload it, use:
  %reload_ext watermark
2020-05-04T08:30:27+05:30

CPython 3.7.4
IPython 7.9.0

compiler   : Clang 4.0.1 (tags&#x2F;RELEASE_401&#x2F;final)
system     : Darwin
release    : 19.4.0
machine    : x86_64
processor  : i386
CPU cores  : 4
interpreter: 64bit








1*
#### [What’s Jekyll](https:&#x2F;&#x2F;sureshshanmugam.com&#x2F;articles&#x2F;what-jekyll&#x2F;) 
*Jekyll is a static site generator, an open source tool for creating simple yet powerful websites of all shapes and sizes. From the project’s readme:
Jekyll is a simple, blog-aware, static site generator perfect for personal, project, or organization sites. Think of it like a file-based CMS, without all the complexity. Jekyll takes your content, renders Markdown and Liquid templates, and spits out a complete, static website ready to be served by Apache, Nginx or another web server. Jekyll is the engine behind GitHub Pages, which you can use to host sites right from your GitHub repositories.
It’s an immensely useful tool and one I encourage you to use for making portfolio sites.*
#### [Distributions](https:&#x2F;&#x2F;sureshshanmugam.com&#x2F;articles&#x2F;distributions&#x2F;) 
*Import necessary libraries




1
2
3
4

import numpy as np

%matplotlib inline
from matplotlib import pyplot as plt




Generate Normal &amp; Pareto random numbers




1
2
3
4

np.random.seed(1087)

X_norm &#x3D; np.random.normal(size&#x3D;(500))
X_poisson &#x3D; np.random.pareto(5, size&#x3D;(500))




Plot histogram of random variables




1
2
3
4
5
6
7
8

fig, ax &#x3D; plt.subplots(2,1, figsize&#x3D;(15, 10))

ax[0].hist(X_norm, bins&#x3D;50, density&#x3D;True, label&#x3D;&#39;normal&#39;, color&#x3D;&#39;b&#39;, alpha&#x3D;0.3)
ax[1].hist(X_poisson, bins&#x3D;50, density&#x3D;True, label&#x3D;&#39;pareto&#39;, color&#x3D;&#39;r&#39;, alpha&#x3D;0.3)
ax[0].legend(loc&#x3D;&#39;best&#39;);
ax[0].set_title(&#39;Normal Distribution&#39;);
ax[1].legend(loc&#x3D;&#39;best&#39;);
ax[1].set_title(&#39;Pareto α&#x3D;5 Distribution&#39;);*
#### [Text Features](https:&#x2F;&#x2F;sureshshanmugam.com&#x2F;articles&#x2F;text-features&#x2F;) 
*Importing necessary packages




1
2
3
4

import pandas as pd
import numpy as np

from sklearn.feature_extraction.text import CountVectorizer, TfidfVectorizer




Count Vectorizer turns sentences into word counts




1

corpus &#x3D; [&#39;This is first sentence&#39;, &#39;Here is the second sentence&#39;, &#39;Third sentence&#39;]








1
2

count_vec &#x3D; CountVectorizer()
features &#x3D; count_vec.fit_transform(corpus)








1

pd.DataFrame(features.todense(), columns&#x3D;count_vec.get_feature_names())





      first
      here
      is
      second
      sentence
      the
      third
      this
    
0
      1
      0
      1
      0
      1
      0
      0
      1
    
1
      0
      1
      1
      1
      1
      1
      0
      0
    
2
      0
      0
      0
      0
      1
      0
      1
      0
    
TFIDF Vectorizer turns sentences into vectors using probabilities




1
2

tfidf &#x3D; TfidfVectorizer()
features_tfidf &#x3D; tfidf.fit_transform(corpus)








1

pd.DataFrame(features_tfidf.todense(), columns&#x3D;tfidf.get_feature_names())





      first
      here
      is
      second
      sentence
      the
      third
      this
    
0
      0.584483
      0.000000
      0.444514
      0.000000
      0.345205
      0.000000
      0.000000
      0.584483
    
1
      0.000000
      0.504611
      0.383770
      0.504611
      0.298032
      0.504611
      0.000000
      0.000000
    
2
      0.000000
      0.000000
      0.000000
      0.000000
      0.508542
      0.000000
      0.861037
      0.000000*
#### [Financial Timeseries](https:&#x2F;&#x2F;sureshshanmugam.com&#x2F;articles&#x2F;financial&#x2F;) 
*Get Pandas Datareader
ProTip: Be sure to remove &#x2F;docs and &#x2F;test if you forked Minimal Mistakes. These folders contain documentation and test pages for the theme and you probably don’t want them littering up your repo.




1
2
3

import pandas as pd
import numpy as np
from pandas_datareader import data




Get Google stock prices




1
2

goog &#x3D; data.DataReader(&#39;GOOG&#39;, start&#x3D;&#39;2004&#39;, end&#x3D;&#39;2018&#39;, data_source&#x3D;&#39;yahoo&#39;)
goog.head()





      High
      Low
      Open
      Close
      Volume
      Adj Close
    
Date
      
      
      
      
      
      
    
2004-08-19
      51.835709
      47.800831
      49.813286
      49.982655
      44871300.0
      49.982655
    
2004-08-20
      54.336334
      50.062355
      50.316402
      53.952770
      22942800.0
      53.952770
    
2004-08-23
      56.528118
      54.321388
      55.168217
      54.495735
      18342800.0
      54.495735
    
2004-08-24
      55.591629
      51.591621
      55.412300
      52.239193
      15319700.0
      52.239193
    
2004-08-25
      53.798351
      51.746044
      52.284027
      52.802086
      9232100.0
      52.802086
    




1

goog_p &#x3D; goog[&#39;Adj Close&#39;]








1
2
3
4

%matplotlib inline
import matplotlib.pyplot as plt
plt.style.use(&#39;seaborn-ticks&#39;)
import seaborn; seaborn.set_style(&#39;whitegrid&#39;)








1

goog_p.plot(figsize&#x3D;(15,10))








1

&lt;matplotlib.axes._subplots.AxesSubplot at 0x128dc0610&gt;





Compute Yearly Return
A common context for financial timeseries data is computing difference over time. For example, we can calculate one-year returns using pandas.




1
2
3
4
5

goog_p &#x3D; goog_p.asfreq(&#39;D&#39;, method&#x3D;&#39;pad&#39;)    
ROI &#x3D; 100 * (goog_p.tshift(-365)&#x2F;goog_p - 1)

ROI.plot(figsize&#x3D;(15, 10))
plt.ylabel(&#39;% Return on Investment&#39;);









1
2

y1_return &#x3D; goog[&#39;Adj Close&#39;].pct_change().rolling(365).sum().dropna()
y1_vol &#x3D; goog[&#39;Adj Close&#39;].pct_change().rolling(365).std().dropna()








1
2
3
4

plt.figure(figsize&#x3D;(15, 10))
seaborn.distplot(y1_return*100)
plt.ylabel(&#39;% Yearly Rolling Return&#39;)
plt.title(&#39;GOOG Historical Returns&#39;);*
<!--END_SECTION:feed-->
