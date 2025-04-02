---
title: PageSetup.suppressEndnotes property
linktitle: suppressEndnotes property
articleTitle: suppressEndnotes property
second_title: Aspose.Words for NodeJs
description: "PageSetup.suppressEndnotes property. True if endnotes are printed at the end of the next section that doesn't suppress endnotes"
type: docs
weight: 410
url: /nodejs-net/Aspose.Words/pagesetup/suppressEndnotes/
---

## PageSetup.suppressEndnotes property

True if endnotes are printed at the end of the next section that doesn't suppress endnotes.
Suppressed endnotes are printed before the endnotes in that section.


```js
get suppressEndnotes(): boolean
```

### Examples

Shows how to store endnotes at the end of each section, and modify their positions.

```js
test('SuppressEndnotes', () => {
  let doc = new aw.Document();
  doc.removeAllChildren();

  // By default, a document compiles all endnotes at its end. 
  expect(doc.endnoteOptions.position).toEqual(aw.Notes.EndnotePosition.EndOfDocument);

  // We use the "Position" property of the document's "EndnoteOptions" object
  // to collect endnotes at the end of each section instead. 
  doc.endnoteOptions.position = aw.Notes.EndnotePosition.EndOfSection;

  insertSectionWithEndnote(doc, "Section 1", "Endnote 1, will stay in section 1");
  insertSectionWithEndnote(doc, "Section 2", "Endnote 2, will be pushed down to section 3");
  insertSectionWithEndnote(doc, "Section 3", "Endnote 3, will stay in section 3");

  // While getting sections to display their respective endnotes, we can set the "SuppressEndnotes" flag
  // of a section's "PageSetup" object to "true" to revert to the default behavior and pass its endnotes
  // onto the next section.
  let pageSetup = doc.sections.at(1).pageSetup;
  pageSetup.suppressEndnotes = true;

  doc.save(base.artifactsDir + "PageSetup.suppressEndnotes.docx");
});


/// <summary>
/// Append a section with text and an endnote to a document.
/// </summary>
function insertSectionWithEndnote(doc, sectionBodyText, endnoteText)
{
  let section = new aw.Section(doc);

  doc.appendChild(section);

  let body = new aw.Body(doc);
  section.appendChild(body);

  expect(body.parentNode.referenceEquals(section)).toEqual(true);

  let para = new aw.Paragraph(doc);
  body.appendChild(para);

  expect(para.parentNode.referenceEquals(body)).toEqual(true);

  let builder = new aw.DocumentBuilder(doc);
  builder.moveTo(para);
  builder.write(sectionBodyText);
  builder.insertFootnote(aw.Notes.FootnoteType.Endnote, endnoteText);
}
```

### See Also

* module [Aspose.Words](../../)
* class [PageSetup](../)

