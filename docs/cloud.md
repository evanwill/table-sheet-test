# Create Cloud Visualizations

## Built-in clouds

The default one cloud visualization pre-configured in `_config.yml`.

These configuration options drive the pre-made page and use the layout value to add an _include via `foot.html`.
Modifying the config settings can easily transform the page into clouds based on any metadata field.

## Cloud include 

Clouds can also be added to any page using the `_include/js/cloud-js.html` include in the page stub content, with the variable `fields`, and optional variables `min` and `stopwords`. 
Cloud-js include assumes a div with `id="cloud"` exists on the page for the cloud to fill.
So putting them together, you can add a cloud anywhere in a page.
For example:

```
<div id="cloud" class="text-center my-4 bg-light border rounded p-2"></div>
{% include js/cloud-js.html fields="creator;publisher" min="2" stopwords="example;another" %}
```
