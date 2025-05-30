---
title: MailMerge.RestartListsAtEachSection
linktitle: RestartListsAtEachSection
articleTitle: RestartListsAtEachSection
second_title: Aspose.Words per .NET
description: Scopri la proprietà MailMerge RestartListsAtEachSection l'elenco di controllo viene reimpostato in ogni sezione per unioni di posta fluide. Migliora la precisione dei tuoi documenti oggi stesso!
type: docs
weight: 110
url: /it/net/aspose.words.mailmerging/mailmerge/restartlistsateachsection/
---
## MailMerge.RestartListsAtEachSection property

Ottiene o imposta un valore che indica se gli elenchi vengono riavviati a ogni sezione dopo l'esecuzione di una stampa unione.

```csharp
public bool RestartListsAtEachSection { get; set; }
```

## Osservazioni

Il valore predefinito è`VERO` .

## Esempi

Mostra come controllare se la numerazione degli elenchi viene riavviata o meno a ogni sezione quando si esegue la stampa unione.

```csharp
Document doc = new Document(MyDir + "Section breaks with numbering.docx");

doc.MailMerge.RestartListsAtEachSection = false;
doc.MailMerge.Execute(new string[0], new object[0]);

doc.Save(ArtifactsDir + "MailMerge.RestartListsAtEachSection.pdf");
```

### Guarda anche

* class [MailMerge](../)
* spazio dei nomi [Aspose.Words.MailMerging](../../../aspose.words.mailmerging/)
* assemblea [Aspose.Words](../../../)
