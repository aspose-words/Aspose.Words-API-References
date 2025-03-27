---
title: TabStopCollection.add method
linktitle: add method
articleTitle: add method
second_title: Aspose.Words for NodeJs
description: "Aspose.Words.TabStopCollection.add method"
type: docs
weight: 40
url: /nodejs-net/Aspose.Words/tabstopcollection/add/
---

## add(tabStop) {#tabstop}

Adds or replaces a tab stop in the collection.


```js
add(tabStop: Aspose.Words.TabStop)
```

| Parameter | Type | Description |
| --- | --- | --- |
| tabStop | [TabStop](../../tabstop/) | A tab stop object to add. |

### Remarks

If a tab stop already exists at the specified position, it is replaced.




## add(position, alignment, leader) {#number_tabalignment_tableader}

Adds or replaces a tab stop in the collection.


```js
add(position: numberalignment: Aspose.Words.TabAlignmentleader: Aspose.Words.TabLeader)
```

| Parameter | Type | Description |
| --- | --- | --- |
| position | number | A position (in points) where to add the tab stop. |
| alignment | [TabAlignment](../../tabalignment/) | A [TabAlignment](../../tabalignment/) value that specifies the alignment of text at the tab stop. |
| leader | [TabLeader](../../tableader/) | A [TabLeader](../../tableader/) value that specifies the type of the leader line displayed under the tab character. |

### Remarks

If a tab stop already exists at the specified position, it is replaced.




## Examples

Shows how to add custom tab stops to a document.

```js
let doc = new aw.Document();
let paragraph = doc.getParagraph(0, true);

// Below are two ways of adding tab stops to a paragraph's collection of tab stops via the "ParagraphFormat" property.
// 1 -  Create a "TabStop" object, and then add it to the collection:
let tabStop = new aw.TabStop(aw.ConvertUtil.inchToPoint(3), aw.TabAlignment.Left, aw.TabLeader.Dashes);
paragraph.paragraphFormat.tabStops.add(tabStop);

// 2 -  Pass the values for properties of a new tab stop to the "Add" method:
paragraph.paragraphFormat.tabStops.add(aw.ConvertUtil.millimeterToPoint(100), aw.TabAlignment.Left,
  aw.TabLeader.Dashes);

// Add tab stops at 5 cm to all paragraphs.
for (var node of doc.getChildNodes(aw.NodeType.Paragraph, true))
{
  var para = node.asParagraph();
  para.paragraphFormat.tabStops.add(aw.ConvertUtil.millimeterToPoint(50), aw.TabAlignment.Left,
    aw.TabLeader.Dashes);
}

// Every "tab" character takes the builder's cursor to the location of the next tab stop.
let builder = new aw.DocumentBuilder(doc);
builder.writeln("Start\tTab 1\tTab 2\tTab 3\tTab 4");

doc.save(base.artifactsDir + "TabStopCollection.AddTabStops.docx");
```

## See Also

* module [Aspose.Words](../../)
* class [TabStopCollection](../)

