---
title: GradientStopCollection class
linktitle: GradientStopCollection class
articleTitle: GradientStopCollection class
second_title: Aspose.Words for Node.js
description: "Aspose.Words.Drawing.GradientStopCollection class. Contains a collection of [GradientStop](../gradientstop/) objects"
type: docs
weight: 140
url: /nodejs-net/aspose.words.drawing/gradientstopcollection/
---

## GradientStopCollection class

Contains a collection of [GradientStop](../gradientstop/) objects.
To learn more, visit the [Working with Graphic Elements](https://docs.aspose.com/words/nodejs-net/working-with-graphic-elements/) documentation article.




### Remarks

You do not create instances of this class directly.
Use the [Fill.gradientStops](../fill/gradientStops/) property to access gradient stops of fill objects.



### Properties

| Name | Description |
| --- | --- |
| [count](./count/) | Gets an integer value indicating the number of items in the collection. |
| [this[]](./this[]/) |  |

### Methods

| Name | Description |
| --- | --- |
|[ add(gradientStop)](./add/#gradientstop) | Adds a specified [GradientStop](../gradientstop/) to a gradient. |
|[ insert(index, gradientStop)](./insert/#number_gradientstop) | Inserts a [GradientStop](../gradientstop/) to the collection at a specified index. |
|[ remove(gradientStop)](./remove/#gradientstop) | Removes a specified [GradientStop](../gradientstop/) from the collection. |
|[ removeAt(index)](./removeAt/#number) | Removes a [GradientStop](../gradientstop/) from the collection at a specified index. |

### Examples

Shows how to add gradient stops to the gradient fill.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);

let shape = builder.insertShape(aw.Drawing.ShapeType.Rectangle, 80, 80);
shape.fill.twoColorGradient("#008000", "#FF0000", aw.Drawing.GradientStyle.Horizontal, aw.Drawing.GradientVariant.Variant2);

// Get gradient stops collection.
let gradientStops = shape.fill.gradientStops;

// Change first gradient stop.
gradientStops.at(0).color = "#00FFFF";
gradientStops.at(0).position = 0.1;
gradientStops.at(0).transparency = 0.25;

// Add new gradient stop to the end of collection.
let gradientStop = new aw.Drawing.GradientStop("#A52A2A", 0.5);
gradientStops.add(gradientStop);

// Remove gradient stop at index 1.
gradientStops.removeAt(1);
// And insert new gradient stop at the same index 1.
gradientStops.insert(1, new aw.Drawing.GradientStop("#D2691E", 0.75, 0.3));

// Remove last gradient stop in the collection.
gradientStop = gradientStops.at(2);
gradientStops.remove(gradientStop);

expect(gradientStops.count).toEqual(2);

//expect(gradientStops.at(0).baseColor).toEqual("#FF00FFFF");
expect(gradientStops.at(0).color).toEqual("#00FFFF");
expect(gradientStops.at(0).position).toBeCloseTo(0.1, 2);
expect(gradientStops.at(0).transparency).toBeCloseTo(0.25, 2);

expect(gradientStops.at(1).color).toEqual("#D2691E");
expect(gradientStops.at(1).position).toBeCloseTo(0.75, 2);
expect(gradientStops.at(1).transparency).toBeCloseTo(0.3, 2);

// Use the compliance option to define the shape using DML
// if you want to get "GradientStops" property after the document saves.
let saveOptions = new aw.Saving.OoxmlSaveOptions();
saveOptions.compliance = aw.Saving.OoxmlCompliance.Iso29500_2008_Strict;

doc.save(base.artifactsDir + "Shape.gradientStops.docx", saveOptions);
```

### See Also

* module [Aspose.Words.Drawing](../)

