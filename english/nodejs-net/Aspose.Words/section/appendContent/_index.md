---
title: Section.appendContent method
linktitle: appendContent method
articleTitle: appendContent method
second_title: Aspose.Words for Node.js
description: "Section.appendContent method. Inserts a copy of content of the source section at the end of this section."
type: docs
weight: 80
url: /nodejs-net/aspose.words/section/appendContent/
---

## appendContent(sourceSection) {#section}

Inserts a copy of content of the source section at the end of this section.


```js
appendContent(sourceSection: Aspose.Words.Section)
```

| Parameter | Type | Description |
| --- | --- | --- |
| sourceSection | [Section](../) | The section to copy content from. |

### Remarks

Only content of [Section.body](../body/) of the source section is copied, page setup,
headers and footers are not copied.

The nodes are automatically imported if the source section belongs to a different document.

No new section is created in the destination document.




### Examples

Shows how to append the contents of a section to another section.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);

builder.write("Section 1");
builder.insertBreak(aw.BreakType.SectionBreakNewPage);
builder.write("Section 2");
builder.insertBreak(aw.BreakType.SectionBreakNewPage);
builder.write("Section 3");

let section = doc.sections.at(2);

expect(section.getText()).toEqual("Section 3" + aw.ControlChar.sectionBreak);

// Insert the contents of the first section to the beginning of the third section.
let sectionToPrepend = doc.sections.at(0);
section.prependContent(sectionToPrepend);

// Insert the contents of the second section to the end of the third section.
let sectionToAppend = doc.sections.at(1);
section.appendContent(sectionToAppend);

// The "PrependContent" and "AppendContent" methods did not create any new sections.
expect(doc.sections.count).toEqual(3);
expect(section.getText()).toEqual("Section 1" + aw.ControlChar.paragraphBreak +
  "Section 3" + aw.ControlChar.paragraphBreak +
  "Section 2" + aw.ControlChar.sectionBreak);
```

### See Also

* module [Aspose.Words](../../)
* class [Section](../)

