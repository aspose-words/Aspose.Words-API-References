---
title: CleanupOptions.DuplicateStyle
second_title: Aspose.Words per .NET API Reference
description: CleanupOptions proprietà. Ottiene/imposta un flag che indica se gli stili duplicati devono essere rimossi dal documento. Il valore predefinito èfalso .
type: docs
weight: 20
url: /it/net/aspose.words/cleanupoptions/duplicatestyle/
---
## CleanupOptions.DuplicateStyle property

Ottiene/imposta un flag che indica se gli stili duplicati devono essere rimossi dal documento. Il valore predefinito è`falso` .

```csharp
public bool DuplicateStyle { get; set; }
```

### Esempi

Mostra come rimuovere gli stili duplicati dal documento.

```csharp
Document doc = new Document();

// Aggiunge due stili al documento con proprietà identiche,
// ma nomi diversi. Il secondo stile è considerato un duplicato del primo.
Style myStyle = doc.Styles.Add(StyleType.Paragraph, "MyStyle1");
myStyle.Font.Size = 14;
myStyle.Font.Name = "Courier New";
myStyle.Font.Color = Color.Blue;

Style duplicateStyle = doc.Styles.Add(StyleType.Paragraph, "MyStyle2");
duplicateStyle.Font.Size = 14;
duplicateStyle.Font.Name = "Courier New";
duplicateStyle.Font.Color = Color.Blue;

Assert.AreEqual(6, doc.Styles.Count);

// Applica entrambi gli stili a diversi paragrafi all'interno del documento.
DocumentBuilder builder = new DocumentBuilder(doc);
builder.ParagraphFormat.StyleName = myStyle.Name;
builder.Writeln("Hello world!");

builder.ParagraphFormat.StyleName = duplicateStyle.Name;
builder.Writeln("Hello again!");

ParagraphCollection paragraphs = doc.FirstSection.Body.Paragraphs;

Assert.AreEqual(myStyle, paragraphs[0].ParagraphFormat.Style);
Assert.AreEqual(duplicateStyle, paragraphs[1].ParagraphFormat.Style);

// Configura un oggetto CleanOptions, quindi chiama il metodo Cleanup per sostituire tutti gli stili duplicati
// con l'originale e rimuove i duplicati dal documento.
CleanupOptions cleanupOptions = new CleanupOptions { DuplicateStyle = true };

doc.Cleanup(cleanupOptions);

Assert.AreEqual(5, doc.Styles.Count);
Assert.AreEqual(myStyle, paragraphs[0].ParagraphFormat.Style);
Assert.AreEqual(myStyle, paragraphs[1].ParagraphFormat.Style);
```

### Guarda anche

* class [CleanupOptions](../)
* spazio dei nomi [Aspose.Words](../../cleanupoptions/)
* assemblea [Aspose.Words](../../../)


