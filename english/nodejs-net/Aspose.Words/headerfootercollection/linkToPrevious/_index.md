---
title: HeaderFooterCollection.linkToPrevious method
linktitle: linkToPrevious method
articleTitle: linkToPrevious method
second_title: Aspose.Words for NodeJs
description: "Aspose.Words.HeaderFooterCollection.linkToPrevious method"
type: docs
weight: 80
url: /nodejs-net/aspose.words/headerfootercollection/linkToPrevious/
---

## linkToPrevious(isLinkToPrevious) {#boolean}

Links or unlinks all headers and footers to the corresponding
headers and footers in the previous section.


```js
linkToPrevious(isLinkToPrevious: boolean)
```

| Parameter | Type | Description |
| --- | --- | --- |
| isLinkToPrevious | boolean | ``true`` to link the headers and footers to the previous section; ``false`` to unlink them. |

### Remarks

If any of the headers or footers do not exist, creates them automatically.




## linkToPrevious(headerFooterType, isLinkToPrevious) {#headerfootertype_boolean}

Links or unlinks the specified header or footer to the corresponding
header or footer in the previous section.


```js
linkToPrevious(headerFooterType: Aspose.Words.HeaderFooterTypeisLinkToPrevious: boolean)
```

| Parameter | Type | Description |
| --- | --- | --- |
| headerFooterType | [HeaderFooterType](../../headerfootertype/) | A [HeaderFooterType](../../headerfootertype/) value that specifies the header or footer to link/unlink. |
| isLinkToPrevious | boolean | ``true`` to link the header or footer to the previous section; ``false`` to unlink. |

### Remarks

If the header or footer of the specified type does not exist, creates it automatically.




## Examples

Shows how to link headers and footers between sections.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);

builder.write("Section 1");
builder.insertBreak(aw.BreakType.SectionBreakNewPage);
builder.write("Section 2");
builder.insertBreak(aw.BreakType.SectionBreakNewPage);
builder.write("Section 3");

// Move to the first section and create a header and a footer. By default,
// the header and the footer will only appear on pages in the section that contains them.
builder.moveToSection(0);

builder.moveToHeaderFooter(aw.HeaderFooterType.HeaderPrimary);
builder.write("This is the header, which will be displayed in sections 1 and 2.");

builder.moveToHeaderFooter(aw.HeaderFooterType.FooterPrimary);
builder.write("This is the footer, which will be displayed in sections 1, 2 and 3.");

// We can link a section's headers/footers to the previous section's headers/footers
// to allow the linking section to display the linked section's headers/footers.
doc.sections.at(1).headersFooters.linkToPrevious(true);

// Each section will still have its own header/footer objects. When we link sections,
// the linking section will display the linked section's header/footers while keeping its own.
expect(doc.sections.at(0).headersFooters.at(0).referenceEquals(
  doc.sections.at(1).headersFooters.at(0))).toEqual(false);
expect(doc.sections.at(0).headersFooters.at(0).parentSection.referenceEquals(
  doc.sections.at(1).headersFooters.at(0).parentSection)).toEqual(false);

  // Link the headers/footers of the third section to the headers/footers of the second section.
// The second section already links to the first section's header/footers,
// so linking to the second section will create a link chain.
// The first, second, and now the third sections will all display the first section's headers.
doc.sections.at(2).headersFooters.linkToPrevious(true);

// We can un-link a previous section's header/footers by passing "false" when calling the LinkToPrevious method.
doc.sections.at(2).headersFooters.linkToPrevious(false);

// We can also select only a specific type of header/footer to link using this method.
// The third section now will have the same footer as the second and first sections, but not the header.
doc.sections.at(2).headersFooters.linkToPrevious(aw.HeaderFooterType.FooterPrimary, true);

// The first section's header/footers cannot link themselves to anything because there is no previous section.
expect(doc.sections.at(0).headersFooters.count).toEqual(2);
let count = doc.sections.at(0).headersFooters.toArray().filter((hf) => !hf.isLinkedToPrevious).length;
expect(count).toEqual(2);

// All the second section's header/footers are linked to the first section's headers/footers.
expect(doc.sections.at(1).headersFooters.count).toEqual(6);
count = doc.sections.at(1).headersFooters.toArray().filter((hf) => hf.isLinkedToPrevious).length;
expect(count).toEqual(6);

// In the third section, only the footer is linked to the first section's footer via the second section.
expect(doc.sections.at(2).headersFooters.count).toEqual(6);
count = doc.sections.at(2).headersFooters.toArray().filter((hf) => !hf.isLinkedToPrevious).length;
expect(count).toEqual(5);
expect(doc.sections.at(2).headersFooters.at(3).isLinkedToPrevious).toEqual(true);

doc.save(base.artifactsDir + "HeaderFooter.link.docx");
```

## See Also

* module [Aspose.Words](../../)
* class [HeaderFooterCollection](../)

