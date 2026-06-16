---
title: "Introduction to Data Visualization"
teaching: 45
exercises: 30
---

:::::::::::::::::::::::::::::::::::::: questions

- What is data visualization and how does it differ from simply displaying charts?
- Why do humans process visualized data so much faster than raw numbers or tables?
- What are the advantages and risks of using visuals in data analysis?
- How does visualization help when working with big data?
- Which tools are most suitable for beginners, intermediate users, and advanced programmers?
- What makes a visualization "good" versus "misleading"?

::::::::::::::::::::::::::::::::::::::::::::::::

::::::::::::::::::::::::::::::::::::: objectives

- Define data visualization and explain its core purpose
- Distinguish between exploratory and explanatory visualizations with real-world examples
- Describe at least five advantages and three disadvantages of data visualization
- Describe how visualization addresses challenges posed by big data
- Compare popular open-source and commercial tools for creating visualizations
- Recognize key principles of effective visualization design
- Understand ethical considerations and accessibility best practices

::::::::::::::::::::::::::::::::::::::::::::::::

::::::::::::::::::::::::::::::::::::: keypoints

- Data visualization turns numbers into stories that the human brain can understand quickly.
- Good visualizations reveal patterns, trends, and outliers that are invisible in spreadsheets.
- Poor design can mislead audiences more powerfully than raw data ever could.
- Big data demands interactive, scalable, and often multi-dimensional visualizations.
- Choose the right tool for your audience and skill level — start simple and iterate.
- Always prioritize clarity, honesty, and accessibility over visual flair.

::::::::::::::::::::::::::::::::::::::::::::::::

## What Is Data Visualization?

**Data visualization** is the graphical representation of information and data. Instead of showing rows and columns of numbers, it uses charts, graphs, maps, diagrams, and interactive dashboards to make patterns, trends, relationships, and outliers immediately understandable.

Think of it as **data storytelling** with graphics. A well-designed visualization does in seconds what a 10-page spreadsheet cannot: it lets the human brain — which processes images 60,000 times faster than text — grasp complex information at a glance.

In the Carpentries context, data visualization is not just "making pretty pictures." It is a core skill that bridges **data wrangling** (covered in previous episodes) and **data-driven decision making**.

There are two broad modes of visualization, and knowing which one you are doing shapes every design decision:

- **Exploratory visualizations** help *you* discover insights while analyzing data — quick, rough, and disposable.
- **Explanatory visualizations** help *others* understand your discoveries — polished, annotated, and purposeful.

## Why Visualize Data?

Our brains devote more than 50% of their processing power to vision. This means a well-chosen chart is not just convenient — it is cognitively more efficient than a table for most tasks. Visualization matters because it:

- **Reveals what numbers hide** — trends over time, clusters, correlations, outliers, geographic patterns, and distributions are rarely obvious in raw data but leap out in a well-chosen chart.
- **Enables faster decision-making** — executives, scientists, journalists, and policymakers routinely use visualizations to justify budgets, publish findings, or inform public opinion.
- **Democratizes data** — a clear chart can be understood by domain experts and non-technical stakeholders alike, lowering the barrier to engaging with evidence.
- **Supports error detection** — visuals often surface data quality problems (missing values, impossible ranges, duplicate records) that automated checks miss entirely.

## Advantages and Disadvantages

Understanding both sides helps you use visualization responsibly.

### Advantages

- **Speed**: Spot trends in seconds rather than hours of table-reading.
- **Clarity**: One well-designed image can replace thousands of numbers and reduce cognitive load significantly.
- **Pattern recognition**: Humans excel at detecting lines, clusters, and shapes — abilities that do not transfer well to reading numbers.
- **Engagement**: Interactive or well-designed visuals capture attention and improve information retention.
- **Storytelling power**: Visualization turns dry statistics into compelling, memorable narratives.
- **Accessibility across audiences**: Good visuals communicate across language barriers and varying technical skill levels.

### Disadvantages and Risks

- **Misleading results**: A truncated y-axis, 3D perspective effects, or cherry-picked color scales can distort the truth — sometimes dramatically.
- **Chartjunk** (Edward Tufte's term): Decorative elements that add visual noise without adding information, such as unnecessary gridlines, shadows, or clip art.
- **Time investment**: Creating a professional, publication-ready visualization can take longer than the underlying analysis.
- **Skill gap**: Effective visualization requires both analytical thinking *and* design sensibility — a combination that takes practice to develop.
- **Over-simplification**: Reducing a complex multi-variable relationship to a single chart can flatten important nuance into something misleading.
- **Accessibility barriers**: Poor color contrast, the absence of alt text, or reliance on color alone to encode information excludes users with color blindness or who use screen readers.

::::::::::::::::::::::::::::::::::::: callout

### The "Lying With Charts" Phenomenon

Visual choices that seem minor — axis scale, color palette, which data points to include — can completely change what a chart appears to say. Always ask yourself: *"Does this visual tell the whole story, or just the story I want to tell?"*

::::::::::::::::::::::::::::::::::::::::::::::::

## Big Data and the Need for Visualization

The explosion of big data — characterized by high **volume**, **velocity**, **variety**, and **veracity** — has made visualization not just helpful, but **essential**.

- **Volume**: A dataset with one million rows is impossible to read. A heatmap or density plot can show the entire distribution at a glance.
- **Velocity**: Real-time dashboards (stock markets, public health trackers, IoT sensor networks) must update continuously and communicate change instantly.
- **Variety**: Combining structured tables, free text, imagery, and geospatial data requires multi-layered visuals — for example, a choropleth map with an overlaid time-series.
- **Dimensionality**: With 50 or more variables, techniques like PCA, t-SNE, or parallel coordinates plots are needed to reduce complexity without losing meaning.

Modern big-data visualizations are generally:

- **Interactive** — users can zoom, filter, and hover for tooltips rather than reading a static snapshot.
- **Scalable** — capable of rendering millions of data points without crashing the browser or notebook.
- **Collaborative** — built on shared dashboard platforms (Tableau Server, Power BI, Plotly Dash) so teams can explore the same data together.

## Real-World Examples

### Simple but powerful

- **Line chart**: Global average temperature rise from 1880 to present — a single trend line communicates over a century of climate data immediately.
- **Bar chart**: Top 10 countries by share of renewable energy, ranked — comparisons across categories are instant.
- **Scatter plot**: Study hours versus exam scores with a regression line — reveals both the relationship and individual variation.

### More advanced

- **Heatmap**: Correlation matrix of 20 genomics variables — shows which pairs of variables are related without producing 190 individual scatter plots.
- **Treemap**: Company revenue broken down by department and region — shows both composition and relative size simultaneously.
- **Network graph**: Social media follower connections or protein interaction maps — structures that have no natural x/y axis.
- **Choropleth map**: COVID case rates or election results by county — geographic patterns that are invisible in a table.
- **Animated bubble chart** (Hans Rosling style): 200 years of global health and wealth data — adds time as a dimension without requiring 200 separate charts.

::::::::::::::::::::::::::::::::::::: challenge

### Good vs. Bad

Look at the two descriptions below and identify what makes one effective and one misleading:

- **Chart A**: A line chart showing annual global CO₂ emissions from 1960 to present. The y-axis starts at zero, the source is labeled, and the title reads "Global CO₂ Emissions Have Risen Steadily Since 1960."
- **Chart B**: A 3D exploding pie chart with 12 color-coded slices, no legend, a y-axis that starts at 94%, and a title that reads "Our Product Dominates the Market."

What specific design choices in Chart B make it misleading? What would you change?

::::::::::::::::::::::::::::::::::::::::::::::::

## Popular Tools — From Beginner to Advanced

| Skill Level | Tool / Library | Best For | Open Source? | Carpentries Recommendation |
|---|---|---|---|---|
| Beginner | Excel / Google Sheets | Quick bar, line, and pie charts | No | Great starting point |
| Beginner–Intermediate | Tableau Public / Power BI | Interactive dashboards | Partial | Excellent for non-coders |
| Intermediate | Python + Matplotlib / Seaborn | Publication-quality static plots | Yes | **Highly recommended** |
| Intermediate–Advanced | Python + Plotly | Interactive web-ready charts | Yes | Perfect for sharing |
| Advanced | R + ggplot2 | Statistical graphics | Yes | Data Carpentry favorite |
| Advanced | JavaScript + D3.js | Fully custom web visualizations | Yes | For web developers |
| All levels | Observable / Vega-Lite | Notebook-style interactive viz | Yes | Modern and flexible |

In this workshop we focus primarily on **Python** (Matplotlib, Seaborn, Plotly) because these tools integrate directly with the data-cleaning and analysis skills covered in earlier episodes.

## Principles of Effective Visualization

These principles draw on the work of Edward Tufte, William Cleveland, and Alberto Cairo:

1. **Maximize the data-ink ratio** — every drop of ink (or pixel) should carry information. Remove gridlines, borders, and decorations that do not contribute.
2. **Use small multiples** instead of overloading a single chart with too many variables or series.
3. **Choose the right chart type** for the message — bar charts for comparison, lines for trends, scatter plots for relationships. Avoid pie charts with more than four or five slices.
4. **Label everything clearly** — titles, axis labels, legends, and units should never require guessing.
5. **Be honest about scale** — never truncate axes without a clear disclosure; never use 3D effects that distort area or angle.
6. **Choose colors deliberately** — use colorblind-friendly palettes such as ColorBrewer or viridis; avoid rainbow scales that imply ordering where none exists.
7. **Make it accessible** — provide alt text for images, ensure sufficient contrast ratios, and encode information with shape or pattern in addition to color alone.
8. **Guide the viewer** — use titles, subtitles, and annotations to direct attention and make the main takeaway explicit.

## Ethical Considerations

Visualizations can influence policy, investment decisions, and public opinion at scale, which creates real responsibility:

- **Avoid cherry-picking**: Selecting only the time window or data subset that supports your conclusion is a form of dishonesty, even if every data point shown is accurate.
- **Disclose sources and limitations**: Readers cannot evaluate a chart they cannot trace back to its data. Always cite the source and note key caveats (sample size, date range, missing data).
- **Respect privacy**: Geospatial and demographic data can expose individuals even when names are removed. Consider aggregation levels carefully.
- **Consider unintended consequences**: A map of crime rates, for example, can reinforce harmful stereotypes if presented without context about policing patterns or historical disinvestment.

## Challenges You Will Face

| Challenge | Recommended approach |
|---|---|
| Too many variables to show at once | Use dimensionality reduction (PCA, t-SNE) or faceting (small multiples) |
| Slow rendering with millions of data points | Sample the data, pre-aggregate, or use WebGL-based tools like Datashader |
| Plots that can't be reproduced later | Always save the code that generated the image alongside the image file |
| Tracking how a visualization changes over time | Store plots and notebooks in version control (Git) |
| Color choices that exclude colorblind users | Test palettes with a simulator; default to viridis or ColorBrewer sequential schemes |
| Audiences with different technical backgrounds | Provide layered detail — a clear headline finding up front, supporting data behind a click or in an appendix |