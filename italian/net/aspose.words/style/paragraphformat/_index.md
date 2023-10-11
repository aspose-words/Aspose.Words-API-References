---
title: Style.ParagraphFormat
second_title: Aspose.Words per .NET API Reference
description: Style proprietà. Ottiene la formattazione del paragrafo dello stile.
type: docs
weight: 150
url: /it/net/aspose.words/style/paragraphformat/
---
## Style.ParagraphFormat property

Ottiene la formattazione del paragrafo dello stile.

```csharp
public ParagraphFormat ParagraphFormat { get; }
```

### Osservazioni

Per gli stili di carattere e di elenco questa proprietà restituisce`nullo`.

### Esempi

Mostra come creare e utilizzare uno stile di paragrafo con formattazione elenco.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Crea uno stile di paragrafo personalizzato.
Style style = doc.Styles.Add(StyleType.Paragraph, "MyStyle1");
style.Font.Size = 24;
style.Font.Name = "Verdana";
style.ParagraphFormat.SpaceAfter = 12;

// Crea un elenco e assicurati che i paragrafi che utilizzano questo stile utilizzino questo elenco.
style.ListFormat.List = doc.Lists.Add(ListTemplate.BulletDefault);
style.ListFormat.ListLevelNumber = 0;

// Applica lo stile di paragrafo al paragrafo corrente del generatore di documenti, quindi aggiunge del testo.
builder.ParagraphFormat.Style = style;
builder.Writeln("Hello World: MyStyle1, bulleted list.");

// Cambia lo stile del generatore di documenti in uno che non abbia formattazione di elenco e scrivi un altro paragrafo.
builder.ParagraphFormat.Style = doc.Styles["Normal"];
builder.Writeln("Hello World: Normal.");

builder.Document.Save(ArtifactsDir + "Styles.ParagraphStyleBulletedList.docx");
```

### Guarda anche

* class [ParagraphFormat](../../paragraphformat/)
* class [Style](../)
* spazio dei nomi [Aspose.Words](../../style/)
* assemblea [Aspose.Words](../../../)


