---
title: PageSetup.differentFirstPageHeaderFooter property
linktitle: differentFirstPageHeaderFooter property
articleTitle: differentFirstPageHeaderFooter property
second_title: Aspose.Words for NodeJs
description: "PageSetup.differentFirstPageHeaderFooter property. True if a different header or footer is used on the first page."
type: docs
weight: 110
url: /nodejs-net/Aspose.Words/pagesetup/differentFirstPageHeaderFooter/
---

## PageSetup.differentFirstPageHeaderFooter property

True if a different header or footer is used on the first page.


```js
get differentFirstPageHeaderFooter(): boolean
```

### Examples

Shows how to enable or disable primary headers/footers.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);

// Below are two types of header/footers.
// 1 -  The "First" header/footer, which appears on the first page of the section.
builder.moveToHeaderFooter(aw.HeaderFooterType.HeaderFirst);
builder.writeln("First page header.");

builder.moveToHeaderFooter(aw.HeaderFooterType.FooterFirst);
builder.writeln("First page footer.");

// 2 -  The "Primary" header/footer, which appears on every page in the section.
// We can override the primary header/footer by a first and an even page header/footer. 
builder.moveToHeaderFooter(aw.HeaderFooterType.HeaderPrimary);
builder.writeln("Primary header.");

builder.moveToHeaderFooter(aw.HeaderFooterType.FooterPrimary);
builder.writeln("Primary footer.");

builder.moveToSection(0);
builder.writeln("Page 1.");
builder.insertBreak(aw.BreakType.PageBreak);
builder.writeln("Page 2.");
builder.insertBreak(aw.BreakType.PageBreak);
builder.writeln("Page 3.");

// Each section has a "PageSetup" object that specifies page appearance-related properties
// such as orientation, size, and borders.
// Set the "DifferentFirstPageHeaderFooter" property to "true" to apply the first header/footer to the first page.
// Set the "DifferentFirstPageHeaderFooter" property to "false"
// to make the first page display the primary header/footer.
builder.pageSetup.differentFirstPageHeaderFooter = differentFirstPageHeaderFooter;

doc.save(base.artifactsDir + "PageSetup.differentFirstPageHeaderFooter.docx");
```

Shows how to create headers and footers in a document using DocumentBuilder.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);

// Specify that we want different headers and footers for first, even and odd pages.
builder.pageSetup.differentFirstPageHeaderFooter = true;
builder.pageSetup.oddAndEvenPagesHeaderFooter = true;

// Create the headers, then add three pages to the document to display each header type.
builder.moveToHeaderFooter(aw.HeaderFooterType.HeaderFirst);
builder.write("Header for the first page");
builder.moveToHeaderFooter(aw.HeaderFooterType.HeaderEven);
builder.write("Header for even pages");
builder.moveToHeaderFooter(aw.HeaderFooterType.HeaderPrimary);
builder.write("Header for all other pages");

builder.moveToSection(0);
builder.writeln("Page1");
builder.insertBreak(aw.BreakType.PageBreak);
builder.writeln("Page2");
builder.insertBreak(aw.BreakType.PageBreak);
builder.writeln("Page3");

doc.save(base.artifactsDir + "DocumentBuilder.HeadersAndFooters.docx");
```

Shows how to track the order in which a text replacement operation traverses nodes.

```js
test.each([false,
  true])('Order', (differentFirstPageHeaderFooter) => {
  let doc = new aw.Document(base.myDir + "Header and footer types.docx");

  let firstPageSection = doc.firstSection;

  let logger = new ReplaceLog();
  let options = new aw.Replacing.FindReplaceOptions();
  options.replacingCallback = logger;

  // Using a different header/footer for the first page will affect the search order.
  firstPageSection.pageSetup.differentFirstPageHeaderFooter = differentFirstPageHeaderFooter;
  doc.range.replace(new Regex("(header|footer)"), "", options);

  if (differentFirstPageHeaderFooter)
    expect(logger.text.replace("\r", "")).toEqual("First header\nFirst footer\nSecond header\nSecond footer\nThird header\nThird footer\n");
  else
    expect(logger.text.replace("\r", "")).toEqual("Third header\nFirst header\nThird footer\nFirst footer\nSecond header\nSecond footer\n");
});


  /// <summary>
  /// During a find-and-replace operation, records the contents of every node that has text that the operation 'finds',
  /// in the state it is in before the replacement takes place.
  /// This will display the order in which the text replacement operation traverses nodes.
  /// </summary>
private class ReplaceLog : IReplacingCallback
{
  public ReplaceAction Replacing(ReplacingArgs args)
  {
    mTextBuilder.AppendLine(args.matchNode.getText());
    return aw.Replacing.ReplaceAction.Skip;
  }

  internal string Text => mTextBuilder.toString();

  private readonly StringBuilder mTextBuilder = new StringBuilder();
}
```

### See Also

* module [Aspose.Words](../../)
* class [PageSetup](../)

