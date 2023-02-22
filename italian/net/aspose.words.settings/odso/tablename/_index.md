---
title: Odso.TableName
second_title: Aspose.Words per .NET API Reference
description: Odso proprietà. Specifica il particolare insieme di dati a cui unorigine deve essere collegata allinterno di unorigine dati esterna. Il valore predefinito è una stringa vuota.
type: docs
weight: 80
url: /it/net/aspose.words.settings/odso/tablename/
---
## Odso.TableName property

Specifica il particolare insieme di dati a cui un'origine deve essere collegata all'interno di un'origine dati esterna. Il valore predefinito è una stringa vuota.

```csharp
public string TableName { get; set; }
```

### Esempi

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

// Possiamo ripristinare queste impostazioni cancellandole. Dopo averlo fatto e salvato il documento,
// Microsoft Word non eseguirà più una stampa unione quando la utilizziamo per caricare il documento.
settings.Clear();

doc.Save(ArtifactsDir + "MailMerge.OdsoEmail.docx");
```

### Guarda anche

* class [Odso](../)
* spazio dei nomi [Aspose.Words.Settings](../../odso/)
* assemblea [Aspose.Words](../../../)


