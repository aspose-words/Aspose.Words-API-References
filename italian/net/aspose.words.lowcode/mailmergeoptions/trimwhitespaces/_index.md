---
title: MailMergeOptions.TrimWhitespaces
linktitle: TrimWhitespaces
articleTitle: TrimWhitespaces
second_title: Aspose.Words per .NET
description: Ottimizza la tua stampa unione con la proprietà TrimWhitespaces. Gestisci facilmente gli spazi iniziali e finali per documenti più puliti e professionali.
type: docs
weight: 110
url: /it/net/aspose.words.lowcode/mailmergeoptions/trimwhitespaces/
---
## MailMergeOptions.TrimWhitespaces property

Ottiene o imposta un valore che indica se gli spazi vuoti iniziali e finali vengono tagliati dai valori di unione di posta.

```csharp
public bool TrimWhitespaces { get; set; }
```

## Osservazioni

Il valore predefinito è`VERO` .

## Esempi

Mostra come eseguire un'operazione di stampa unione per un singolo record.

```csharp
// Esistono diversi modi per eseguire un'operazione di unione di posta:
string doc = MyDir + "Mail merge.doc";

string[] fieldNames = new string[] { "FirstName", "Location", "SpecialCharsInName()" };
string[] fieldValues = new string[] { "James Bond", "London", "Classified" };

MailMerger.Execute(doc, ArtifactsDir + "LowCode.MailMerge.1.docx", fieldNames, fieldValues);
MailMerger.Execute(doc, ArtifactsDir + "LowCode.MailMerge.2.docx", SaveFormat.Docx, fieldNames, fieldValues);
MailMergeOptions mailMergeOptions = new MailMergeOptions();
mailMergeOptions.TrimWhitespaces = true;
MailMerger.Execute(doc, ArtifactsDir + "LowCode.MailMerge.3.docx", SaveFormat.Docx, fieldNames, fieldValues, mailMergeOptions);
```

### Guarda anche

* class [MailMergeOptions](../)
* spazio dei nomi [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* assemblea [Aspose.Words](../../../)
