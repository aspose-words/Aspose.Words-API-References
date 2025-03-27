---
title: Section.headersFooters property
linktitle: headersFooters property
articleTitle: headersFooters property
second_title: Aspose.Words for NodeJs
description: "Section.headersFooters property. Provides access to the headers and footers nodes of the section."
type: docs
weight: 30
url: /nodejs-net/Aspose.Words/section/headersFooters/
---

## Section.headersFooters property

Provides access to the headers and footers nodes of the section.


```js
get headersFooters(): Aspose.Words.HeaderFooterCollection
```

### Examples

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

Shows how to replace text in a document's footer.

```js
let doc = new aw.Document(base.myDir + "Footer.docx");

let headersFooters = doc.firstSection.headersFooters;
let footer = headersFooters.getByHeaderFooterType(aw.HeaderFooterType.FooterPrimary);

let options = new aw.Replacing.FindReplaceOptions();
options.matchCase = false;
options.findWholeWordsOnly = false;

let currentYear = new Date().getYear();
footer.range.replace("(C) 2006 Aspose Pty Ltd.", `Copyright (C) ${currentYear} by Aspose Pty Ltd.`, options);

doc.save(base.artifactsDir + "HeaderFooter.ReplaceText.docx");
```

### See Also

* module [Aspose.Words](../../)
* class [Section](../)

