---
title: "DifferentFirstPageHeaderFooter"
second_title: Aspose.Words for .NET API Reference
description: ""
type: docs
weight: 30
url: /net/aspose.words/pagesetup/differentfirstpageheaderfooter/
---
## PageSetup.DifferentFirstPageHeaderFooter property

True if a different header or footer is used on the first page.

```csharp
public bool DifferentFirstPageHeaderFooter { get; set; }
```

### Examples

Shows how to create headers and footers in a document using DocumentBuilder.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Specify that we want different headers and footers for first, even and odd pages.
builder.PageSetup.DifferentFirstPageHeaderFooter = true;
builder.PageSetup.OddAndEvenPagesHeaderFooter = true;

// Create the headers, then add three pages to the document to display each header type.
builder.MoveToHeaderFooter(HeaderFooterType.HeaderFirst);
builder.Write("Header for the first page");
builder.MoveToHeaderFooter(HeaderFooterType.HeaderEven);
builder.Write("Header for even pages");
builder.MoveToHeaderFooter(HeaderFooterType.HeaderPrimary);
builder.Write("Header for all other pages");

builder.MoveToSection(0);
builder.Writeln("Page1");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Page2");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Page3");

doc.Save(ArtifactsDir + "DocumentBuilder.HeadersAndFooters.docx");
```

Shows how to enable or disable primary headers/footers.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Below are two types of header/footers.
// 1 -  The "First" header/footer, which appears on the first page of the section.
builder.MoveToHeaderFooter(HeaderFooterType.HeaderFirst);
builder.Writeln("First page header.");

builder.MoveToHeaderFooter(HeaderFooterType.FooterFirst);
builder.Writeln("First page footer.");

// 2 -  The "Primary" header/footer, which appears on every page in the section.
// We can override the primary header/footer by a first and an even page header/footer. 
builder.MoveToHeaderFooter(HeaderFooterType.HeaderPrimary);
builder.Writeln("Primary header.");

builder.MoveToHeaderFooter(HeaderFooterType.FooterPrimary);
builder.Writeln("Primary footer.");

builder.MoveToSection(0);
builder.Writeln("Page 1.");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Page 2.");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Page 3.");

// Each section has a "PageSetup" object that specifies page appearance-related properties
// such as orientation, size, and borders.
// Set the "DifferentFirstPageHeaderFooter" property to "true" to apply the first header/footer to the first page.
// Set the "DifferentFirstPageHeaderFooter" property to "false"
// to make the first page display the primary header/footer.
builder.PageSetup.DifferentFirstPageHeaderFooter = differentFirstPageHeaderFooter;

doc.Save(ArtifactsDir + "PageSetup.DifferentFirstPageHeaderFooter.docx");
```

Shows how to track the order in which a text replacement operation traverses nodes.

```csharp
public void Order(bool differentFirstPageHeaderFooter)
        {
            Document doc = new Document(MyDir + "Header and footer types.docx");

            Section firstPageSection = doc.FirstSection;

            ReplaceLog logger = new ReplaceLog();
            FindReplaceOptions options = new FindReplaceOptions { ReplacingCallback = logger };

            // Using a different header/footer for the first page will affect the search order.
            firstPageSection.PageSetup.DifferentFirstPageHeaderFooter = differentFirstPageHeaderFooter;
            doc.Range.Replace(new Regex("(header|footer)"), "", options);

#if NET48 || NET5_0 || JAVA
            if (differentFirstPageHeaderFooter)
                Assert.AreEqual("First header\nFirst footer\nSecond header\nSecond footer\nThird header\nThird footer\n", 
                    logger.Text.Replace("\r", ""));
            else
                Assert.AreEqual("Third header\nFirst header\nThird footer\nFirst footer\nSecond header\nSecond footer\n", 
                    logger.Text.Replace("\r", ""));
#elif __MOBILE__
            if (differentFirstPageHeaderFooter)
                Assert.AreEqual("First header\nFirst footer\nSecond header\nSecond footer\nThird header\nThird footer\n", logger.Text);
            else
                Assert.AreEqual("Third header\nFirst header\nThird footer\nFirst footer\nSecond header\nSecond footer\n", logger.Text);
#endif
        }

        /// <summary>
        /// During a find-and-replace operation, records the contents of every node that has text that the operation 'finds',
        /// in the state it is in before the replacement takes place.
        /// This will display the order in which the text replacement operation traverses nodes.
        /// </summary>
        private class ReplaceLog : IReplacingCallback
        {
            public ReplaceAction Replacing(ReplacingArgs args)
            {
                mTextBuilder.AppendLine(args.MatchNode.GetText());
                return ReplaceAction.Skip;
            }

            internal string Text => mTextBuilder.ToString();

            private readonly StringBuilder mTextBuilder = new StringBuilder();
        }
```

### See Also

* class [PageSetup](../../pagesetup)
* namespace [Aspose.Words](../../pagesetup)
* assembly [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
