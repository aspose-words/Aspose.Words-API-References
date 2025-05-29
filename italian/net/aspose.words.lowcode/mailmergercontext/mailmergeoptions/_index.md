---
title: MailMergerContext.MailMergeOptions
linktitle: MailMergeOptions
articleTitle: MailMergeOptions
second_title: Aspose.Words per .NET
description: Scopri la funzionalità MailMergeContext MailMergeOptions per semplificare l'automazione dei tuoi documenti e migliorare l'efficienza del tuo flusso di lavoro senza sforzo.
type: docs
weight: 20
url: /it/net/aspose.words.lowcode/mailmergercontext/mailmergeoptions/
---
## MailMergerContext.MailMergeOptions property

Opzioni di unione posta.

```csharp
public MailMergeOptions MailMergeOptions { get; }
```

## Esempi

Mostra come eseguire un'operazione di stampa unione per un singolo record utilizzando il contesto.

```csharp
// Esistono diversi modi per eseguire un'operazione di unione di posta:
string doc = MyDir + "Mail merge.doc";

string[] fieldNames = new string[] { "FirstName", "Location", "SpecialCharsInName()" };
string[] fieldValues = new string[] { "James Bond", "London", "Classified" };

MailMergerContext mailMergerContext = new MailMergerContext();
mailMergerContext.SetSimpleDataSource(fieldNames, fieldValues);
mailMergerContext.MailMergeOptions.TrimWhitespaces = true;

MailMerger.Create(mailMergerContext)
    .From(doc)
    .To(ArtifactsDir + "LowCode.MailMergeContext.docx")
    .Execute();
```

Mostra come eseguire un'operazione di stampa unione per un singolo record dal flusso utilizzando il contesto.

```csharp
// Esistono diversi modi per eseguire un'operazione di unione di posta utilizzando i documenti dal flusso:
string[] fieldNames = new string[] { "FirstName", "Location", "SpecialCharsInName()" };
string[] fieldValues = new string[] { "James Bond", "London", "Classified" };

using (FileStream streamIn = new FileStream(MyDir + "Mail merge.doc", FileMode.Open, FileAccess.Read))
{
    MailMergerContext mailMergerContext = new MailMergerContext();
    mailMergerContext.SetSimpleDataSource(fieldNames, fieldValues);
    mailMergerContext.MailMergeOptions.TrimWhitespaces = true;

    using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.MailMergeContextStream.docx", FileMode.Create, FileAccess.ReadWrite))
        MailMerger.Create(mailMergerContext)
            .From(streamIn)
            .To(streamOut, SaveFormat.Docx)
            .Execute();
}
```

### Guarda anche

* class [MailMergeOptions](../../mailmergeoptions/)
* class [MailMergerContext](../)
* spazio dei nomi [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* assemblea [Aspose.Words](../../../)
