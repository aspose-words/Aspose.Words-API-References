---
title: Section.clearContent method
linktitle: clearContent method
articleTitle: clearContent method
second_title: Aspose.Words for NodeJs
description: "Section.clearContent method. Clears the section."
type: docs
weight: 90
url: /nodejs-net/aspose.words/section/clearContent/
---

## clearContent() {#default}

Clears the section.


```js
clearContent()
```

### Remarks

The text of [Section.body](../body/) is cleared, only one empty paragraph is left that represents the section break.

The text of all headers and footers is cleared, but [HeaderFooter](../../headerfooter/) objects themselves are not removed.




### Examples

Shows how to clear the contents of a section.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);

builder.write("Hello world!");

expect(doc.getText().trim()).toEqual("Hello world!");
expect(doc.firstSection.body.paragraphs.count).toEqual(1);

// Running the "ClearContent" method will remove all the section contents
// but leave a blank paragraph to add content again.
doc.firstSection.clearContent();

expect(doc.getText().trim()).toEqual('');
expect(doc.firstSection.body.paragraphs.count).toEqual(1);
```

### See Also

* module [Aspose.Words](../../)
* class [Section](../)

