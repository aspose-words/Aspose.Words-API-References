---
title: CleanupOptions.DuplicateStyle
linktitle: DuplicateStyle
articleTitle: DuplicateStyle
second_title: Aspose.Words för .NET
description: Optimera dina dokument med CleanupOptions DuplicateStyle-egenskap – ta enkelt bort dubbletter av formatering för en renare och effektivare formatering. Standardvärdet är falskt.
type: docs
weight: 20
url: /sv/net/aspose.words/cleanupoptions/duplicatestyle/
---
## CleanupOptions.DuplicateStyle property

Hämtar/ställer in en flagga som anger om dubbletter av stilar ska tas bort från dokumentet. Standardvärdet är`falsk` .

```csharp
public bool DuplicateStyle { get; set; }
```

## Exempel

Visar hur man tar bort duplicerade stilar från dokumentet.

```csharp
Document doc = new Document();

// Lägg till två stilar i dokumentet med identiska egenskaper,
// men olika namn. Den andra stilen anses vara en kopia av den första.
Style myStyle = doc.Styles.Add(StyleType.Paragraph, "MyStyle1");
myStyle.Font.Size = 14;
myStyle.Font.Name = "Courier New";
myStyle.Font.Color = Color.Blue;

Style duplicateStyle = doc.Styles.Add(StyleType.Paragraph, "MyStyle2");
duplicateStyle.Font.Size = 14;
duplicateStyle.Font.Name = "Courier New";
duplicateStyle.Font.Color = Color.Blue;

Assert.AreEqual(6, doc.Styles.Count);

// Använd båda stilarna på olika stycken i dokumentet.
DocumentBuilder builder = new DocumentBuilder(doc);
builder.ParagraphFormat.StyleName = myStyle.Name;
builder.Writeln("Hello world!");

builder.ParagraphFormat.StyleName = duplicateStyle.Name;
builder.Writeln("Hello again!");

ParagraphCollection paragraphs = doc.FirstSection.Body.Paragraphs;

Assert.AreEqual(myStyle, paragraphs[0].ParagraphFormat.Style);
Assert.AreEqual(duplicateStyle, paragraphs[1].ParagraphFormat.Style);

// Konfigurera ett CleanOptions-objekt och anropa sedan Cleanup-metoden för att ersätta alla dubbletter av format
// med originalet och ta bort dubbletterna från dokumentet.
CleanupOptions cleanupOptions = new CleanupOptions { DuplicateStyle = true };

doc.Cleanup(cleanupOptions);

Assert.AreEqual(5, doc.Styles.Count);
Assert.AreEqual(myStyle, paragraphs[0].ParagraphFormat.Style);
Assert.AreEqual(myStyle, paragraphs[1].ParagraphFormat.Style);
```

### Se även

* class [CleanupOptions](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
