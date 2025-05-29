---
title: Style.ParagraphFormat
linktitle: ParagraphFormat
articleTitle: ParagraphFormat
second_title: Aspose.Words per .NET
description: Scopri come accedere e personalizzare la formattazione dei paragrafi degli stili per una presentazione migliore dei documenti e una formattazione professionale.
type: docs
weight: 150
url: /it/net/aspose.words/style/paragraphformat/
---
## Style.ParagraphFormat property

Ottiene la formattazione del paragrafo dello stile.

```csharp
public ParagraphFormat ParagraphFormat { get; }
```

## Osservazioni

Per gli stili di carattere e di elenco questa proprietà restituisce`null`.

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

* class [ParagraphFormat](../../paragraphformat/)
* class [Style](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
