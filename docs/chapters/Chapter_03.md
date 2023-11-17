## Scenario 7: Integrating TeSS widgets on your web site

  Widgets are chunks of JavaScript code that can be copied into website source code to display TeSS content. There are several different styles and functionalities available from our configurable widget suite. Widgets can be used to enhance your site and offer your community lists of relevant events or training resources. There are examples of code on [this page](https://elixirtess.github.io/TeSS_widgets/).



You can use these widgets to enhance your site and offer your community lists of relevant events or training resources! Check the examples of code on the [widget examples page](https://elixirtess.github.io/TeSS_widgets/). We will provide one example below.

**How to implement a tabular layout:**

1. Choose the specific widget type **Events table with a sidebar**. A working example is shown on the github pages from the ELIXIR TeSS team at https://elixirtess.github.io/TeSS_widgets. 

2.	Manually annotate the HTML web site e.g. index.html with the code snippet for the TeSS widget. More specifically, enter the code snippet as shown below as a sibling of a div element.

```html
<link rel="stylesheet" property="stylesheet" href="https://elixirtess.github.io/TeSS_widgets/css/tess-widget.css"/>
<div id="tess-widget-events-table" class="tess-widget tess-widget-faceted-table"></div>
<script>
function initTeSSWidgets() {
    TessWidget.Events(document.getElementById('tess-widget-events-table'),
        'FacetedTable',
        {
            opts: {
                columns: [{name: 'Date', field: 'start'},
                    {name: 'Name', field: 'title'},
                    {name: 'Location', field: 'location'}],
                allowedFacets: ['scientific-topics', 'country', 'city', 'target-audience'],
                facetOptionLimit: 5
            },
            params: {
                q: 'Python',
                country: ['Belgium', 'United Kingdom']
            }
        });
}
</script>
<script async="" defer="" src="https://elixirtess.github.io/TeSS_widgets/js/tess-widget-standalone.js" onload="initTeSSWidgets()"></script> 
```

3.	Save the HTML page and serve the HTML page for visual inspection.

4.	Validate visually that the rendered HTML page includes a table with the Events extracted from TeSS. It will show a filtered list according to the values in the params section (see snippet from step 2). In this case, all future courses aggregated in TeSS will be live filtered on the general search term ‘Python’ and display only the courses from ‘Belgium’ and ‘United Kingdom’.

5. You can adapt the code:
- Remove the term ‘Python’ from the general search. Now, the table underneath should be updated with all the up-coming courses from Belgium and the United Kingdom. 
- By adapting other facets like ‘Scientific Topics’ and ‘Target audience’, other filtering schemes can be established. 

At any time you may remove any of the filters you applied to reduce stringency of your search. If you would like to include past events in your search, click on the Show past events button.

If you'd like to use these widgets for training materials, investigate the example for training materials on the [same website](https://elixirtess.github.io/TeSS_widgets/).

In the next step, we will show how to VIB Technology Training has implemented the widgets on their home page.


*********************

TODO: find an events widget

If you'd like to see an implementation of the TeSS widget for materials, please browse to [https://technologytraining.sites.vib.be/en/overview-offering](https://technologytraining.sites.vib.be/en/overview-offering) and scroll to the bottom of the page.

*********************