---
title: HeaderFooterCollection class
linktitle: HeaderFooterCollection class
articleTitle: HeaderFooterCollection class
second_title: Aspose.Words for Node.js
description: "Aspose.Words.HeaderFooterCollection class. Provides typed access to [HeaderFooter](../headerfooter/) nodes of a [Section](../section/)"
type: docs
weight: 490
url: /nodejs-net/aspose.words/headerfootercollection/
---

## HeaderFooterCollection class

Provides typed access to [HeaderFooter](../headerfooter/) nodes of a [Section](../section/).
To learn more, visit the [Working with Headers and Footers](https://docs.aspose.com/words/nodejs-net/working-with-headers-and-footers/) documentation article.




### Remarks

There can be maximum of one [HeaderFooter](../headerfooter/)


 of each[HeaderFooterType](../headerfootertype/) per
[Section](../section/).
[HeaderFooter](../headerfooter/) objects can occur in any order in the collection.




**Inheritance:** [HeaderFooterCollection](./) → [NodeCollection](../nodecollection/)

### Properties

| Name | Description |
| --- | --- |
| [count](../nodecollection/count/) | Gets the number of nodes in the collection.<br>(Inherited from [NodeCollection](../nodecollection/)) |
| [footerEven](./footerEven/) | Retrieves a footer for even numbered pages. |
| [footerFirst](./footerFirst/) | Retrieves a footer for the first page of the section. |
| [footerPrimary](./footerPrimary/) | Retrieves a primary footer, also used for odd numbered pages. |
| [headerEven](./headerEven/) | Retrieves a header for even numbered pages. |
| [headerFirst](./headerFirst/) | Retrieves a header for the first page of the section. |
| [headerPrimary](./headerPrimary/) | Retrieves a primary header, also used for odd numbered pages. |
| [this[]](../nodecollection/this[]/) | <br>(Inherited from [NodeCollection](../nodecollection/)) |

### Methods

| Name | Description |
| --- | --- |
|[ add(node)](../nodecollection/add/#node) | Adds a node to the end of the collection.<br>(Inherited from [NodeCollection](../nodecollection/)) |
|[ clear()](../nodecollection/clear/#default) | Removes all nodes from this collection and from the document.<br>(Inherited from [NodeCollection](../nodecollection/)) |
|[ contains(node)](../nodecollection/contains/#node) | Determines whether a node is in the collection.<br>(Inherited from [NodeCollection](../nodecollection/)) |
|[ getByHeaderFooterType(headerFooterType)](./getByHeaderFooterType/#headerfootertype) | Retrieves a **HeaderFooter** of the specified type. |
|[ indexOf(node)](../nodecollection/indexOf/#node) | Returns the zero-based index of the specified node.<br>(Inherited from [NodeCollection](../nodecollection/)) |
|[ insert(index, node)](../nodecollection/insert/#number_node) | Inserts a node into the collection at the specified index.<br>(Inherited from [NodeCollection](../nodecollection/)) |
|[ linkToPrevious(isLinkToPrevious)](./linkToPrevious/#boolean) | Links or unlinks all headers and footers to the corresponding headers and footers in the previous section. |
|[ linkToPrevious(headerFooterType, isLinkToPrevious)](./linkToPrevious/#headerfootertype_boolean) | Links or unlinks the specified header or footer to the corresponding header or footer in the previous section. |
|[ remove(node)](../nodecollection/remove/#node) | Removes the node from the collection and from the document.<br>(Inherited from [NodeCollection](../nodecollection/)) |
|[ removeAt(index)](../nodecollection/removeAt/#number) | Removes the node at the specified index from the collection and from the document.<br>(Inherited from [NodeCollection](../nodecollection/)) |
|[ toArray()](./toArray/#default) | Copies all ``HeaderFooter`` s from the collection to a new array of ``HeaderFooter`` s. |

### Examples

Shows how to create a header and a footer.

```js
let doc = new aw.Document();

// Create a header and append a paragraph to it. The text in that paragraph
// will appear at the top of every page of this section, above the main body text.
let header = new aw.HeaderFooter(doc, aw.HeaderFooterType.HeaderPrimary);
doc.firstSection.headersFooters.add(header);

let para = header.appendParagraph("My header.");

expect(header.isHeader).toEqual(true);
expect(para.isEndOfHeaderFooter).toEqual(true);

// Create a footer and append a paragraph to it. The text in that paragraph
// will appear at the bottom of every page of this section, below the main body text.
let footer = new aw.HeaderFooter(doc, aw.HeaderFooterType.FooterPrimary);
doc.firstSection.headersFooters.add(footer);

para = footer.appendParagraph("My footer.");

expect(footer.isHeader).toEqual(false);
expect(para.isEndOfHeaderFooter).toEqual(true);

expect(para.parentStory.referenceEquals(footer)).toEqual(true);
expect(para.parentSection.referenceEquals(footer.parentSection)).toEqual(true);
expect(header.parentSection.referenceEquals(footer.parentSection)).toEqual(true);

doc.save(base.artifactsDir + "HeaderFooter.create.docx");
```

Shows how to delete all footers from a document.

```js
let doc = new aw.Document(base.myDir + "Header and footer types.docx");

// Iterate through each section and remove footers of every kind.
for (let section of doc.sections.toArray())
{
  // There are three kinds of footer and header types.
  // 1 -  The "First" header/footer, which only appears on the first page of a section.
  let footer = section.headersFooters.getByHeaderFooterType(aw.HeaderFooterType.FooterFirst);
  footer.remove();

  // 2 -  The "Primary" header/footer, which appears on odd pages.
  footer = section.headersFooters.getByHeaderFooterType(aw.HeaderFooterType.FooterPrimary);
  footer.remove();

  // 3 -  The "Even" header/footer, which appears on even pages. 
  footer = section.headersFooters.getByHeaderFooterType(aw.HeaderFooterType.FooterEven);
  footer.remove();

  let count = section.headersFooters.toArray().filter((hf) => !hf.isHeader).length;
  expect(count).toEqual(0);
}

doc.save(base.artifactsDir + "HeaderFooter.RemoveFooters.docx");
```

### See Also

* module [Aspose.Words](../)
* class [NodeCollection](../nodecollection/)

