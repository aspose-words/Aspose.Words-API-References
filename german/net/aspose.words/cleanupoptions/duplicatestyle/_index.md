---
title: CleanupOptions.DuplicateStyle
linktitle: DuplicateStyle
articleTitle: DuplicateStyle
second_title: Aspose.Words für .NET
description: Optimieren Sie Ihre Dokumente mit der CleanupOptions DuplicateStyle-Eigenschaft – entfernen Sie doppelte Stile einfach für eine sauberere und effizientere Formatierung. Der Standardwert ist „false“.
type: docs
weight: 20
url: /de/net/aspose.words/cleanupoptions/duplicatestyle/
---
## CleanupOptions.DuplicateStyle property

Ruft ein Flag ab/setzt es, das angibt, ob doppelte Stile aus dem Dokument entfernt werden sollen. Der Standardwert ist`FALSCH` .

```csharp
public bool DuplicateStyle { get; set; }
```

## Beispiele

Zeigt, wie doppelte Stile aus dem Dokument entfernt werden.

```csharp
Document doc = new Document();

// Dem Dokument zwei Stile mit identischen Eigenschaften hinzufügen,
// aber unterschiedliche Namen. Der zweite Stil wird als Duplikat des ersten betrachtet.
Style myStyle = doc.Styles.Add(StyleType.Paragraph, "MyStyle1");
myStyle.Font.Size = 14;
myStyle.Font.Name = "Courier New";
myStyle.Font.Color = Color.Blue;

Style duplicateStyle = doc.Styles.Add(StyleType.Paragraph, "MyStyle2");
duplicateStyle.Font.Size = 14;
duplicateStyle.Font.Name = "Courier New";
duplicateStyle.Font.Color = Color.Blue;

Assert.AreEqual(6, doc.Styles.Count);

// Wenden Sie beide Stile auf verschiedene Absätze im Dokument an.
DocumentBuilder builder = new DocumentBuilder(doc);
builder.ParagraphFormat.StyleName = myStyle.Name;
builder.Writeln("Hello world!");

builder.ParagraphFormat.StyleName = duplicateStyle.Name;
builder.Writeln("Hello again!");

ParagraphCollection paragraphs = doc.FirstSection.Body.Paragraphs;

Assert.AreEqual(myStyle, paragraphs[0].ParagraphFormat.Style);
Assert.AreEqual(duplicateStyle, paragraphs[1].ParagraphFormat.Style);

// Konfigurieren Sie ein CleanOptions-Objekt und rufen Sie dann die Cleanup-Methode auf, um alle doppelten Stile zu ersetzen
// mit dem Original und entfernen Sie die Duplikate aus dem Dokument.
CleanupOptions cleanupOptions = new CleanupOptions { DuplicateStyle = true };

doc.Cleanup(cleanupOptions);

Assert.AreEqual(5, doc.Styles.Count);
Assert.AreEqual(myStyle, paragraphs[0].ParagraphFormat.Style);
Assert.AreEqual(myStyle, paragraphs[1].ParagraphFormat.Style);
```

### Siehe auch

* class [CleanupOptions](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
