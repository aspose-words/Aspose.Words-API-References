---
title: ParagraphFormat.StyleIdentifier
linktitle: StyleIdentifier
articleTitle: StyleIdentifier
second_title: Aspose.Words per .NET
description: Scopri la proprietà StyleIdentifier di ParagraphFormat per gestire e personalizzare facilmente gli stili di paragrafo, migliorando la formattazione e la leggibilità del tuo documento.
type: docs
weight: 360
url: /it/net/aspose.words/paragraphformat/styleidentifier/
---
## ParagraphFormat.StyleIdentifier property

Ottiene o imposta l'identificatore di stile indipendente dalle impostazioni locali dello stile di paragrafo applicato a questa formattazione.

```csharp
public StyleIdentifier StyleIdentifier { get; set; }
```

## Esempi

Mostra come inserire un indice (TOC) in un documento utilizzando gli stili di intestazione come voci.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Inserire un indice per la prima pagina del documento.
// Configura la tabella in modo che selezioni i paragrafi con titoli di livello da 1 a 3.
// Inoltre, imposta le sue voci come collegamenti ipertestuali che ci porteranno
// alla posizione dell'intestazione quando si fa clic con il pulsante sinistro del mouse in Microsoft Word.
builder.InsertTableOfContents("\\o \"1-3\" \\h \\z \\u");
builder.InsertBreak(BreakType.PageBreak);

// Popola il sommario aggiungendo paragrafi con stili di intestazione.
// Ciascuna intestazione con un livello compreso tra 1 e 3 creerà una voce nella tabella.
builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading1;
builder.Writeln("Heading 1");

builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading2;
builder.Writeln("Heading 1.1");
builder.Writeln("Heading 1.2");

builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading1;
builder.Writeln("Heading 2");
builder.Writeln("Heading 3");

builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading2;
builder.Writeln("Heading 3.1");

builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading3;
builder.Writeln("Heading 3.1.1");
builder.Writeln("Heading 3.1.2");
builder.Writeln("Heading 3.1.3");

builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading4;
builder.Writeln("Heading 3.1.3.1");
builder.Writeln("Heading 3.1.3.2");

builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading2;
builder.Writeln("Heading 3.2");
builder.Writeln("Heading 3.3");

// Un indice è un campo di un tipo che deve essere aggiornato per mostrare un risultato aggiornato.
doc.UpdateFields();
doc.Save(ArtifactsDir + "DocumentBuilder.InsertToc.docx");
```

### Guarda anche

* enum [StyleIdentifier](../../styleidentifier/)
* class [ParagraphFormat](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
