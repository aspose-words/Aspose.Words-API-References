---
title: MailMerge.TrimWhitespaces
linktitle: TrimWhitespaces
articleTitle: TrimWhitespaces
second_title: Aspose.Words per .NET
description: MailMerge TrimWhitespaces proprietà. Ottiene o imposta un valore che indica se gli spazi finali e iniziali vengono eliminati dai valori di stampa unione in C#.
type: docs
weight: 130
url: /it/net/aspose.words.mailmerging/mailmerge/trimwhitespaces/
---
## MailMerge.TrimWhitespaces property

Ottiene o imposta un valore che indica se gli spazi finali e iniziali vengono eliminati dai valori di stampa unione.

```csharp
public bool TrimWhitespaces { get; set; }
```

## Osservazioni

Il valore predefinito è`VERO` .

## Esempi

Mostra come eliminare gli spazi dai valori di un'origine dati durante l'esecuzione di una stampa unione.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.InsertField("MERGEFIELD myMergeField", null);

doc.MailMerge.TrimWhitespaces = trimWhitespaces;
doc.MailMerge.Execute(new[] { "myMergeField" }, new object[] { "\t hello world! " });

Assert.AreEqual(trimWhitespaces ? "hello world!\f" : "\t hello world! \f", doc.GetText());
```

### Guarda anche

* class [MailMerge](../)
* spazio dei nomi [Aspose.Words.MailMerging](../../../aspose.words.mailmerging/)
* assemblea [Aspose.Words](../../../)
