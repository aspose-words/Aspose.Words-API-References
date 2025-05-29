---
title: ParagraphFormat.Style
linktitle: Style
articleTitle: Style
second_title: Aspose.Words per .NET
description: Scopri la proprietà Stile ParagraphFormat per personalizzare e migliorare facilmente lo stile dei paragrafi del tuo documento, migliorandone la leggibilità e la presentazione.
type: docs
weight: 350
url: /it/net/aspose.words/paragraphformat/style/
---
## ParagraphFormat.Style property

Ottiene o imposta lo stile di paragrafo applicato a questa formattazione.

```csharp
public Style Style { get; set; }
```

## Esempi

Mostra come creare e utilizzare uno stile di paragrafo con formattazione elenco.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Crea uno stile di paragrafo personalizzato.
Style style = doc.Styles.Add(StyleType.Paragraph, "MyStyle1");
style.Font.Size = 24;
style.Font.Name = "Verdana";
style.ParagraphFormat.SpaceAfter = 12;

// Crea un elenco e assicurati che i paragrafi che utilizzano questo stile utilizzeranno questo elenco.
style.ListFormat.List = doc.Lists.Add(ListTemplate.BulletDefault);
style.ListFormat.ListLevelNumber = 0;

// Applica lo stile paragrafo al paragrafo corrente del generatore di documenti, quindi aggiungi del testo.
builder.ParagraphFormat.Style = style;
builder.Writeln("Hello World: MyStyle1, bulleted list.");

// Modificare lo stile del generatore di documenti scegliendone uno che non abbia formattazione di elenco e scrivere un altro paragrafo.
builder.ParagraphFormat.Style = doc.Styles["Normal"];
builder.Writeln("Hello World: Normal.");

builder.Document.Save(ArtifactsDir + "Styles.ParagraphStyleBulletedList.docx");
```

### Guarda anche

* class [Style](../../style/)
* class [ParagraphFormat](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
