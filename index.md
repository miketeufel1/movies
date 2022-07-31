<html>
<script src='https://d3js.org/d3.v5.min.js'></script>
<style> path {stroke: black;}</style>
<body>
<svg width=300 height=300>
</svg>
<script>
		var data = [4,8,15,16,23,42];

		var svg = d3.select("svg"),
			width = svg.attr("width"),
			height = svg.attr("height"),
			radius = Math.min(width, height) / 2,
			g = svg.append("g").attr("transform", "translate(" + width / 2 + "," + height / 2 + ")");

		var color = d3.scaleOrdinal(['pink','lightyellow','lightgreen','lightcyan','lightblue','violet']);

		// Generate the pie
		var pie = d3.pie();

		// Generate the arcs
		var arc = d3.arc()
					.innerRadius(0)
					.outerRadius(radius/3*2);

		//Generate groups
		var arcs = g.selectAll("g")
					.data(pie(data))
					.enter()

		//Draw arc paths
		arcs.append("path")
			.attr("d", arc)
                        .attr("fill", function(d, i) {
				return color(i);
			});
	</script>
</body>
</html>



## Hello to my page!

Your can use the [->editor on GitHub](https://github.com/miketeufel1/movies/edit/gh-pages/index.md) to maintain and preview the content for your website in Markdown files.

Whenever you commit to this repository, GitHub Pages will run [Jekyll](https://jekyllrb.com/) to rebuild the pages in your site, from the content in your Markdown files.

### Markdown

Markdown is a lightweight and easy-to-use syntax for styling your writing. It includes conventions for

```markdown
Syntax highlighted code block

# Header 1
## Header 2
### Header 3

- Bulleted
- List

1. Numbered
2. List

**Bold** and _Italic_ and `Code` text

[Link](url) and ![Image](src)
```

For more details see [Basic writing and formatting syntax](https://docs.github.com/en/github/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax).

### Jekyll Themes

Your Pages site will use the layout and styles from the Jekyll theme you have selected in your [repository settings](https://github.com/miketeufel1/movies/settings/pages). The name of this theme is saved in the Jekyll `_config.yml` configuration file.

### Support or Contact

Having trouble with Pages? Check out our [documentation](https://docs.github.com/categories/github-pages-basics/) or [contact support](https://support.github.com/contact) and we’ll help you sort it out.
