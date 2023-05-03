---
title: MailMergeSettings.AddressFieldName
linktitle: AddressFieldName
second_title: Aspose.Words for .NET API Reference
description: MailMergeSettings AddressFieldName property. Specifies the column within the data source that contains email addresses. The default value is an empty string in C#.
type: docs
weight: 30
url: /net/aspose.words.settings/mailmergesettings/addressfieldname/
---
## MailMergeSettings.AddressFieldName property

Specifies the column within the data source that contains e-mail addresses. The default value is an empty string.

```csharp
public string AddressFieldName { get; set; }
```

## Examples

Shows how to execute a mail merge while connecting to an external data source.

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

// We can reset these settings by clearing them. Once we do that and save the document,
// Microsoft Word will no longer execute a mail merge when we use it to load the document.
settings.Clear();

doc.Save(ArtifactsDir + "MailMerge.OdsoEmail.docx");
```

### See Also

* class [MailMergeSettings](../)
* namespace [Aspose.Words.Settings](../../mailmergesettings/)
* assembly [Aspose.Words](../../../)
