---
title: MailMergeSettings.Clear
linktitle: Clear
articleTitle: Clear
second_title: Aspose.Words per .NET
description: Reimposta senza sforzo le impostazioni di stampa unione con il metodo Clear di MailMergeSettings, trasformando il tuo documento in un formato standard per un utilizzo senza interruzioni.
type: docs
weight: 180
url: /it/net/aspose.words.settings/mailmergesettings/clear/
---
## MailMergeSettings.Clear method

Cancella le impostazioni di stampa unione in modo che quando il documento viene salvato, nessuna impostazione di stampa unione verrà salvata e diventerà un documento normale.

```csharp
public void Clear()
```

## Esempi

Mostra come eseguire una stampa unione durante la connessione a un'origine dati esterna.

```csharp
Document doc = new Document(MyDir + "Odso data.docx");
MailMergeSettings settings = doc.MailMergeSettings;

Console.WriteLine($"Connection string:\n\t{settings.ConnectString}");
Console.WriteLine($"Mail merge docs as attachment:\n\t{settings.MailAsAttachment}");
Console.WriteLine($"Mail merge doc e-mail subject:\n\t{settings.MailSubject}");
Console.WriteLine($"Column that contains e-mail addresses:\n\t{settings.AddressFieldName}");
Console.WriteLine($"Active record:\n\t{settings.ActiveRecord}");

Odso odso = settings.Odso;

Console.WriteLine($"File will connect to data source located in:\n\t\"{odso.DataSource}\"");
Console.WriteLine($"Source type:\n\t{odso.DataSourceType}");
Console.WriteLine($"UDL connection string:\n\t{odso.UdlConnectString}");
Console.WriteLine($"Table:\n\t{odso.TableName}");
Console.WriteLine($"Query:\n\t{doc.MailMergeSettings.Query}");

// Possiamo ripristinare queste impostazioni cancellandole. Una volta fatto questo e salvato il documento,
// Microsoft Word non eseguirà più una stampa unione quando lo utilizziamo per caricare il documento.
settings.Clear();

doc.Save(ArtifactsDir + "MailMerge.OdsoEmail.docx");
```

### Guarda anche

* class [MailMergeSettings](../)
* spazio dei nomi [Aspose.Words.Settings](../../../aspose.words.settings/)
* assemblea [Aspose.Words](../../../)
