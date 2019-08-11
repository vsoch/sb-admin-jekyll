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

### Area Chart

An area chart is a line chart that can include one or more lines.

```
{% raw %}{% include charts/area.html width=8 labels="Jan,Feb,Mar,Apr,May,Jun,Jul,Aug,Sep,Oct,Nov,Dec" title="Candy Sales" datasets="Earnings:0,10000,5000,15000,10000,20000,15000,25000,20000,30000,25000,40000" currency='true' %}{% endraw %}
```

You can include multiple datasets, each should be in the format "title1:points1|title2:points2" where a
":" separates the title for a set of points, and then the two datasets are separated by a pipe "|".
The labels would be shared on the X axis by both.

If your dataset is monetary, set currency equal to anything. Otherwise, remove it.


### Bar Chart

Finally, a bar chart is easy to include with the following:

```
{% raw %}{% include charts/bar.html title="Total Revenue" width=12 labels="January,February,March,April,May,June" datasets="Revenue:4215,5312,6251,7841,9821,14984," currency="true" %}{% endraw %}
```

The variables are the same as they are for the area chart!


## Cards

A card can hold a statistic, a progress bar, or general text.

### Statistic

A single statistic might look like this:

<div class="row">
{% include cards/statistic.html icon="fa-calendar" value="$40,000" title="Earnings (Monthly)" style="primary" %}
{% include cards/statistic.html icon="fa-dollar-sign" value="$215,000" title="Earnings (Annual)" style="success" %}
</div>

The code looks like this - notice we've put them both inside a row. Most fields are self-explanatory.

```html
{% raw %}<div class="row">{% include cards/statistic.html icon="fa-calendar" value="$40,000" title="Earnings (Monthly)" style="primary" %}
{% include cards/statistic.html icon="fa-dollar-sign" value="$215,000" title="Earnings (Annual)" style="success" %}</div>{% endraw %}
```

### Progress

The same kind of statistic can also be for a progress bar, like this:

{% include cards/progress.html title="Tasks" icon="fa-clipboard-list" value="50" %}

```html
{% raw %}{% include cards/progress.html title="Tasks" icon="fa-clipboard-list" percent="50" %}{% endraw %}
```

The main difference is providing a percent instead of a value.


### Bars

For a group of bars (in a card) you can do the following:

```
{% raw %}{% include cards/bars.html title="Projects" data="Server Migration,20,danger|Sales Tracking,40,warning|Payout Details,80,info|Account Setup,100,success" width=12 %}{% endraw %}
```

Where each entry in data has three values:

 1. The bar title
 2. The bar percentage filled
 3. The bootstrap type (warning, primary, danger, info, success, secondary, etc.)


## Tables

A table can be read in directly from a csv file in the _data folder, or yaml if you prefer.
The file in `_data/tables/example.csv` is an export of candy from [Kaggle](https://www.kaggle.com/fivethirtyeight/the-ultimate-halloween-candy-power-ranking) and we render it on the page like this:

```
{% raw %}{% include datatable.html title="Datatable Example" file="table-example" %}{% endraw %}
```

## Buttons

Buttons are easy to include, here are split buttons:

{% include buttons/split-button.html style="primary" title="Split Button Primary" icon="fa-flag"%}
{% include buttons/split-button.html style="success" title="Split Button Success" icon="fa-check"%}
{% include buttons/split-button.html style="info" title="Split Button Info" icon="fa-info-circle"%}
{% include buttons/split-button.html style="warning" title="Split Button Warning" icon="fa-exclamation-triangle"%}
{% include buttons/split-button.html style="danger" title="Split Button Danger" icon="fa-trash"%}
{% include buttons/split-button.html style="secondary" title="Split Button Secondary" icon="fa-arrow-right"%}
{% include buttons/split-button.html style="light" title="Split Button Primary" icon="fa-arrow-right"%}


The code looks like this, and if you add a url parameter, the buttons will link there.

```html{% raw %}
{% include buttons/split-button.html style="primary" title="Split Button Primary" icon="fa-flag"%}
{% include buttons/split-button.html style="success" title="Split Button Success" icon="fa-check"%}
{% include buttons/split-button.html style="info" title="Split Button Info" icon="fa-info-circle"%}
{% include buttons/split-button.html style="warning" title="Split Button Warning" icon="fa-exclamation-triangle"%}
{% include buttons/split-button.html style="danger" title="Split Button Danger" icon="fa-trash"%}
{% include buttons/split-button.html style="secondary" title="Split Button Secondary" icon="fa-arrow-right"%}
{% include buttons/split-button.html style="light" title="Split Button Primary" icon="fa-arrow-right"%}
{% endraw %}
```
