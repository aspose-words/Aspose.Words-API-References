---
title: Section.clone method
linktitle: clone method
articleTitle: clone method
second_title: Aspose.Words for NodeJs
description: "Section.clone method. Creates a duplicate of this section."
type: docs
weight: 110
url: /nodejs-net/Aspose.Words/section/clone/
---

## clone() {#default}

Creates a duplicate of this section.


```js
clone()
```

### Examples

Shows how to add and remove sections in a document.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);

builder.write("Section 1");
builder.insertBreak(aw.BreakType.SectionBreakNewPage);
builder.write("Section 2");

expect(doc.getText().trim()).toEqual("Section 1\u000cSection 2");

// Delete the first section from the document.
doc.sections.removeAt(0);

expect(doc.getText().trim()).toEqual("Section 2");

// Append a copy of what is now the first section to the end of the document.
let lastSectionIdx = doc.sections.count - 1;
let newSection = doc.sections.at(lastSectionIdx).clone();
doc.sections.add(newSection);

expect(doc.getText().trim()).toEqual("Section 2\u000cSection 2");
```

### See Also

* module [Aspose.Words](../../)
* class [Section](../)

