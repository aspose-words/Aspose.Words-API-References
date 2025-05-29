---
title: DocumentBuilder.InsertStyleSeparator
linktitle: InsertStyleSeparator
articleTitle: InsertStyleSeparator
second_title: Aspose.Words per .NET
description: Migliora i tuoi documenti con il metodo InsertStyleSeparator di DocumentBuilder, aggiungendo senza sforzo separatori di stile per una formattazione e un'organizzazione migliori.
type: docs
weight: 490
url: /it/net/aspose.words/documentbuilder/insertstyleseparator/
---
## DocumentBuilder.InsertStyleSeparator method

Inserisce un separatore di stile nel documento.

```csharp
public void InsertStyleSeparator()
```

## Osservazioni

Questo metodo consente di applicare stili di paragrafo diversi a due parti diverse di una riga di testo.

## Esempi

Mostra come lavorare con i separatori di stile.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Ogni paragrafo può avere un solo stile.
// Il metodo InsertStyleSeparator ci consente di aggirare questa limitazione.
builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading1;
builder.Write("This text is in a Heading style. ");
builder.InsertStyleSeparator();

Style paraStyle = builder.Document.Styles.Add(StyleType.Paragraph, "MyParaStyle");
paraStyle.Font.Bold = false;
paraStyle.Font.Size = 8;
paraStyle.Font.Name = "Arial";

builder.ParagraphFormat.StyleName = paraStyle.Name;
builder.Write("This text is in a custom style. ");

// La chiamata al metodo InsertStyleSeparator crea un altro paragrafo,
// che può avere uno stile diverso dal precedente. Non ci saranno interruzioni tra i paragrafi.
// Il testo nel documento di output apparirà come un paragrafo con due stili.
Assert.AreEqual(2, doc.FirstSection.Body.Paragraphs.Count);
Assert.AreEqual("Heading 1", doc.FirstSection.Body.Paragraphs[0].ParagraphFormat.Style.Name);
Assert.AreEqual("MyParaStyle", doc.FirstSection.Body.Paragraphs[1].ParagraphFormat.Style.Name);

doc.Save(ArtifactsDir + "DocumentBuilder.InsertStyleSeparator.docx");
```

### Guarda anche

* class [DocumentBuilder](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
