---
title: DocumentBuilder.InsertStyleSeparator
linktitle: InsertStyleSeparator
articleTitle: InsertStyleSeparator
second_title: Aspose.Words für .NET
description: DocumentBuilder InsertStyleSeparator methode. Fügt Stiltrennzeichen in das Dokument ein in C#.
type: docs
weight: 450
url: /de/net/aspose.words/documentbuilder/insertstyleseparator/
---
## DocumentBuilder.InsertStyleSeparator method

Fügt Stiltrennzeichen in das Dokument ein.

```csharp
public void InsertStyleSeparator()
```

## Bemerkungen

Mit dieser Methode können Sie unterschiedliche Absatzstile auf zwei verschiedene Teile einer Textzeile anwenden.

## Beispiele

Zeigt, wie mit Stiltrennzeichen gearbeitet wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Jeder Absatz kann nur einen Stil haben.
// Mit der Methode „InsertStyleSeparator“ können wir diese Einschränkung umgehen.
builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading1;
builder.Write("This text is in a Heading style. ");
builder.InsertStyleSeparator();

Style paraStyle = builder.Document.Styles.Add(StyleType.Paragraph, "MyParaStyle");
paraStyle.Font.Bold = false;
paraStyle.Font.Size = 8;
paraStyle.Font.Name = "Arial";

builder.ParagraphFormat.StyleName = paraStyle.Name;
builder.Write("This text is in a custom style. ");

// Durch Aufrufen der InsertStyleSeparator-Methode wird ein weiterer Absatz erstellt.
// der einen anderen Stil als der vorherige haben kann. Es wird keine Pause zwischen den Absätzen geben.
// Der Text im Ausgabedokument sieht aus wie ein Absatz mit zwei Stilen.
Assert.AreEqual(2, doc.FirstSection.Body.Paragraphs.Count);
Assert.AreEqual("Heading 1", doc.FirstSection.Body.Paragraphs[0].ParagraphFormat.Style.Name);
Assert.AreEqual("MyParaStyle", doc.FirstSection.Body.Paragraphs[1].ParagraphFormat.Style.Name);

doc.Save(ArtifactsDir + "DocumentBuilder.InsertStyleSeparator.docx");
```

### Siehe auch

* class [DocumentBuilder](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
