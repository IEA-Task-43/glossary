# Transformation

An operation in which data is transformed from one form to another. The resulting form is entirely general but may be (for example):

* A re-expression of the same fundamental data (eg rewriting with a different data structure or file format)
* A combination of data sources (eg add wind direction to wind speed, to form a combined time series)
* A result of the application of an algorithm (eg getting mean wind speed by averaging a time series)
* An expression or visualisation (eg an HTML file to display a chart of wind speed time series and a table of monthly averages)

Data transformation as a term is often used with reference to [pipelines](pipeline.md), which can be used to execute an arbitrary number and sequence of transformations.

{% hint style="warning" %}
**Disambiguation**

The term **"Transformation"** could be perceived as meaning **"Translation"** of data (eg a re-expression of the same fundamental data in a different way). Translation, however, represents only one of the many kinds of operation that could be a transformation [(see below)](transformation.md#kinds-of-transformation).


{% endhint %}

## Kinds of transformation

In the discussion that led to this entry, a range of other terms were discussed surrounding the "transformation" terminology, with some viewing other terms as more helpful. "Data Analysis" and "Data Translation" in particular were thought of.&#x20;

However, such terms **have a connotation regarding the purpose of the transformation**, which can result in confusion when attempting to think clearly about the data engineering required to implement a transformation, particularly since an output of a given translation might have multiple uses.

In general though, it may be helpful to have a shorthand to discuss different specific kinds of translation.  Corresponding with the above examples:

* A **translation** might constitute a re-expression of the same fundamental data in a different form
* A **view** might constitute the creation of a bridge between two data tables, combining two data sources to appear as one
* An **analysis** might constitute application of some scientific algorithm to extract results or insight (which themselves constitute the output data of the transformation)
* A **render** might constitute the expression or visualisation of data in a way which may not be well suited for ongoing use in an automated pipeline, but is good for human consumption (like an automated report).

{% hint style="danger" %}
**Why use the word "might"?**

The boundaries blur between these items, particularly because it can't be known _a priori_ how the output of any given transformation will be used.

* For example, using a[ jupyter notebook](https://jupyter.org/) to average some data and plot the result would combine algorithm implementation with visualisation. This would be colloquially called a "data analysis", but when moving to a production scenario, averaging of the data and the visualisation of the result would likely be in entirely different domains.
{% endhint %}

{% hint style="info" %}
**Tip**

Thinking simply in terms of transformations (as opposed to the different kinds and their purposes) will help you think more objectively about the separation of concerns between, and the role of, each step in a pipeline.
{% endhint %}
