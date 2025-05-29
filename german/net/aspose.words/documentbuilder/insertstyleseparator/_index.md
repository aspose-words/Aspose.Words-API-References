---
title: DocumentBuilder.InsertStyleSeparator
linktitle: InsertStyleSeparator
articleTitle: InsertStyleSeparator
second_title: Aspose.Words für .NET
description: Verbessern Sie Ihre Dokumente mit der InsertStyleSeparator-Methode von DocumentBuilder, indem Sie mühelos Stiltrennzeichen für eine verbesserte Formatierung und Organisation hinzufügen.
type: docs
weight: 490
url: /de/net/aspose.words/documentbuilder/insertstyleseparator/
---
## DocumentBuilder.InsertStyleSeparator method

Fügt einen Stiltrenner in das Dokument ein.

```csharp
public void InsertStyleSeparator()
```

## Bemerkungen

Mit dieser Methode können Sie zwei verschiedenen Teilen einer Textzeile unterschiedliche Absatzstile zuweisen.

## Beispiele

Zeigt, wie mit Stiltrennzeichen gearbeitet wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Jeder Absatz kann nur einen Stil haben.
// Mit der Methode InsertStyleSeparator können wir diese Einschränkung umgehen.
builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading1;
builder.Write("This text is in a Heading style. ");
builder.InsertStyleSeparator();

Style paraStyle = builder.Document.Styles.Add(StyleType.Paragraph, "MyParaStyle");
paraStyle.Font.Bold = false;
paraStyle.Font.Size = 8;
paraStyle.Font.Name = "Arial";

builder.ParagraphFormat.StyleName = paraStyle.Name;
builder.Write("This text is in a custom style. ");

// Durch Aufruf der Methode InsertStyleSeparator wird ein weiterer Absatz erstellt,
// der einen anderen Stil als der vorherige haben kann. Es wird keinen Umbruch zwischen den Absätzen geben.
// Der Text im Ausgabedokument sieht wie ein Absatz mit zwei Stilen aus.
Assert.AreEqual(2, doc.FirstSection.Body.Paragraphs.Count);
Assert.AreEqual("Heading 1", doc.FirstSection.Body.Paragraphs[0].ParagraphFormat.Style.Name);
Assert.AreEqual("MyParaStyle", doc.FirstSection.Body.Paragraphs[1].ParagraphFormat.Style.Name);

doc.Save(ArtifactsDir + "DocumentBuilder.InsertStyleSeparator.docx");
```

### Siehe auch

* class [DocumentBuilder](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
