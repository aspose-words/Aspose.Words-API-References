---
title: ParagraphFormat.ClearFormatting
linktitle: ClearFormatting
articleTitle: ClearFormatting
second_title: Aspose.Words per .NET
description: ParagraphFormat ClearFormatting metodo. Ripristina la formattazione del paragrafo predefinita in C#.
type: docs
weight: 420
url: /it/net/aspose.words/paragraphformat/clearformatting/
---
## ParagraphFormat.ClearFormatting method

Ripristina la formattazione del paragrafo predefinita.

```csharp
public void ClearFormatting()
```

## Osservazioni

La formattazione predefinita del paragrafo è lo stile Normale, allineato a sinistra, senza rientro, senza spaziatura, senza bordi e senza ombreggiatura.

## Esempi

Mostra come nidificare un elenco all'interno di un altro elenco.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Un elenco ci consente di organizzare e decorare insiemi di paragrafi con simboli di prefisso e rientri.
 // Possiamo creare elenchi nidificati aumentando il livello di rientro.
 // Possiamo iniziare e terminare un elenco utilizzando la proprietà "ListFormat" del generatore di documenti.
// Ogni paragrafo che aggiungiamo tra l'inizio e la fine di un elenco diventerà un elemento nell'elenco.
// Crea un elenco struttura per le intestazioni.
List outlineList = doc.Lists.Add(ListTemplate.OutlineNumbers);
builder.ListFormat.List = outlineList;
builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading1;
builder.Writeln("This is my Chapter 1");

// Crea un elenco numerato.
List numberedList = doc.Lists.Add(ListTemplate.NumberDefault);
builder.ListFormat.List = numberedList;
builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Normal;
builder.Writeln("Numbered list item 1.");

// Ogni paragrafo che comprende un elenco avrà questo flag.
Assert.True(builder.CurrentParagraph.IsListItem);
Assert.True(builder.ParagraphFormat.IsListItem);

// Crea un elenco puntato.
List bulletedList = doc.Lists.Add(ListTemplate.BulletDefault);
builder.ListFormat.List = bulletedList;
builder.ParagraphFormat.LeftIndent = 72;
builder.Writeln("Bulleted list item 1.");
builder.Writeln("Bulleted list item 2.");
builder.ParagraphFormat.ClearFormatting();

// Ripristina l'elenco numerato.
builder.ListFormat.List = numberedList;
builder.Writeln("Numbered list item 2.");
builder.Writeln("Numbered list item 3.");

// Ripristina l'elenco delle strutture.
builder.ListFormat.List = outlineList;
builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading1;
builder.Writeln("This is my Chapter 2");

builder.ParagraphFormat.ClearFormatting();

builder.Document.Save(ArtifactsDir + "Lists.NestedLists.docx");
```

### Guarda anche

* class [ParagraphFormat](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
