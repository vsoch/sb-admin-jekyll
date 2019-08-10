---
layout: page
title: Getting Started
---

The sections in the navigation will show you want components look like, but
not how to easily include them in pages! This getting started section
will help you to do that.

## Navigation

The navigation is determined by the file [_data/toc.yml](https://github.com/vsoch/sb-admin-jekyll/blob/master/_data/toc.yml). There are three levels of nesting, and you can decide how you want your links to look
based on it. Let's look at examples.

### A single Link

If you want a single link to a page, you only need one level of nesting. You
will need to define a title, [font awesome icon](https://fontawesome.com/icons?d=gallery),
and a url. The example below shows the default link to the dashboard, followed
by this page. Notice that pages should be relative to "docs".

```yaml
- title: Dashboard
  icon: fa-tachometer-alt
  url: /
- title: Getting Started
  icon: fa-star-o
  url: docs/getting-started/
```

If you need to define an external url, you can do so with "external_url".

```
- title: GitHub
  icon: fa-github
  url: https://www.github.com/vsoch/sb-admin-jekyll
```

### A link with Children

In the case that you have a link with children, the way that the template
renders on the page is with an upperlevel link, and then a subsection (with an icon)
and the links below it. We represent that as follows:

```yaml
- title: Interface
  links:
    - title: Components
      icon: fa-cog
      children:
        - title: Buttons
          subtitle: "Custom Components:"
          url: "docs/interface/buttons/"
        - title: Cards
          url: "docs/interface/cards/"
    - title: "Utilities"
      icon: fa-wrench
      children:
        - title: Color
          subtitle: "Custom Utilities:"
          url: "docs/utilities/colors"
        - title: Borders
          url: "docs/utilities/borders"
        - title: Animations
          url: "docs/utilities/animations"
        - title: Other
          url: "docs/utilities/other"
```

Note that the "Interface" section has two nested sections, "Components" and "Utilities,"
and each has a list of children with titles and urls.

> What about the subtitle?

A subtitle added to a child indicates that you want a divider (with that label) directly
before the child. Take a look at the navigation on this page, for those sections, to
see an example.


## Charts

Charts are provided by Chart.js, and have been edited to be included as [includes](https://github.com/vsoch/sb-admin-jekyll/tree/master/_includes/charts).

### Pie Chart

You can include a pie chart in a page as follows:

```html
{% raw %}{% include charts/pie.html data="55,30,15" width=4 title="Candy Breakdown" labels="Snickers,Twix,Reeses" %}{% endraw %}
```

Including the chart will also include a card with title, and a dropdown with save button, so we need to provide a column width (4 in the example above, meaning we could fit 3 across). The data and labels should be the same length, and be separated by commas, and the title should be defined.
