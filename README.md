Interlinking service
====================

This code implements a REST-based interlinking service wrapping existing extraction and interlinking tools. Clients can query the tools available, getting info on the input format they support and the parameters to configure them. Then, they can issue calls and get suggested links to datasets in the Web of Data for potential inclusion in their contents or for other purposes.

This wrapped tools analyse text with the purpose of find matching terms in target datasets. Actually, the service is working, in general, with the dataset of Agrovoc. Agrovoc is a controlled vocabulary covering all areas of interest to FAO, including food, nutrition, agriculture, fisheries, forestry, environment etc. Tools like KEA uses this dataset to analyse a document of agriculture and find references to URIs in the agrovoc ontology, giving metrics in the process. However, tools like silk only can make relations between the words and the URIs and the metrics should be calculated in a post-process part. Anyway, all final responses of this API are designed to send the information in JSON with this format.
```JSON
{   
  “tool-id” : “<id of the tool invoked>”,
        “timestamp” : “<YYYY-MM-DDThh:mm:ssTZD>”
  “links” : [
    <Finded occurrences>
  ]
}
```
The interlinking service runs over ruby 1.8.7 or above.

### Contents:
* [API Design](https://github.com/ieru/interlinking/wiki/API-Design)
* [Install Guides](https://github.com/ieru/interlinking/wiki/Install-Guides)
* [Configuration](https://github.com/ieru/interlinking/wiki/Configuration)
* [FAQ](https://github.com/ieru/interlinking/wiki/FAQ)


