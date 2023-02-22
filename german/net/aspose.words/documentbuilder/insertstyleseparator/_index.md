---
title: DocumentBuilder.InsertStyleSeparator
second_title: Aspose.Words für .NET-API-Referenz
description: DocumentBuilder methode. Fügt Stiltrennzeichen in das Dokument ein.
type: docs
weight: 430
url: /de/net/aspose.words/documentbuilder/insertstyleseparator/
---
## DocumentBuilder.InsertStyleSeparator method

Fügt Stiltrennzeichen in das Dokument ein.

```csharp
public void InsertStyleSeparator()
```

### Bemerkungen

Diese Methode ermöglicht es, unterschiedliche Absatzstile auf zwei verschiedene Teile einer Textzeile anzuwenden.

### Beispiele

Zeigt, wie Sie mit Stiltrennzeichen arbeiten.

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

// Der Aufruf der InsertStyleSeparator-Methode erstellt einen weiteren Absatz,
// die einen anderen Stil als die vorherige haben kann. Es wird keine Unterbrechung zwischen den Absätzen geben.
// Der Text im Ausgabedokument sieht aus wie ein Absatz mit zwei Stilen.
Assert.AreEqual(2, doc.FirstSection.Body.Paragraphs.Count);
Assert.AreEqual("Heading 1", doc.FirstSection.Body.Paragraphs[0].ParagraphFormat.Style.Name);
Assert.AreEqual("MyParaStyle", doc.FirstSection.Body.Paragraphs[1].ParagraphFormat.Style.Name);

doc.Save(ArtifactsDir + "DocumentBuilder.InsertStyleSeparator.docx");
```

### Siehe auch

* class [DocumentBuilder](../)
* namensraum [Aspose.Words](../../documentbuilder/)
* Montage [Aspose.Words](../../../)


