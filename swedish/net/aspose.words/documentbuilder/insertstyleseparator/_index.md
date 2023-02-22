---
title: DocumentBuilder.InsertStyleSeparator
second_title: Aspose.Words för .NET API Referens
description: DocumentBuilder metod. Infogar stilavgränsare i dokumentet.
type: docs
weight: 430
url: /sv/net/aspose.words/documentbuilder/insertstyleseparator/
---
## DocumentBuilder.InsertStyleSeparator method

Infogar stilavgränsare i dokumentet.

```csharp
public void InsertStyleSeparator()
```

### Anmärkningar

Den här metoden gör det möjligt att tillämpa olika styckestilar på två olika delar av en textrad.

### Exempel

Visar hur man arbetar med stilavgränsare.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Varje stycke kan bara ha en stil.
// Metoden InsertStyleSeparator tillåter oss att kringgå denna begränsning.
builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading1;
builder.Write("This text is in a Heading style. ");
builder.InsertStyleSeparator();

Style paraStyle = builder.Document.Styles.Add(StyleType.Paragraph, "MyParaStyle");
paraStyle.Font.Bold = false;
paraStyle.Font.Size = 8;
paraStyle.Font.Name = "Arial";

builder.ParagraphFormat.StyleName = paraStyle.Name;
builder.Write("This text is in a custom style. ");

// Genom att anropa metoden InsertStyleSeparator skapas ytterligare ett stycke,
// som kan ha en annan stil än föregående. Det blir ingen paus mellan styckena.
// Texten i utdatadokumentet kommer att se ut som ett stycke med två stilar.
Assert.AreEqual(2, doc.FirstSection.Body.Paragraphs.Count);
Assert.AreEqual("Heading 1", doc.FirstSection.Body.Paragraphs[0].ParagraphFormat.Style.Name);
Assert.AreEqual("MyParaStyle", doc.FirstSection.Body.Paragraphs[1].ParagraphFormat.Style.Name);

doc.Save(ArtifactsDir + "DocumentBuilder.InsertStyleSeparator.docx");
```

### Se även

* class [DocumentBuilder](../)
* namnutrymme [Aspose.Words](../../documentbuilder/)
* hopsättning [Aspose.Words](../../../)


