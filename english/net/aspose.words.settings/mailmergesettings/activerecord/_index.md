---
title: MailMergeSettings.ActiveRecord
linktitle: ActiveRecord
articleTitle: ActiveRecord
second_title: Aspose.Words for .NET
description: Discover MailMergeSettings. Customize your Microsoft Word documents by selecting the desired record index from your data source. Start with ease!
type: docs
weight: 20
url: /net/aspose.words.settings/mailmergesettings/activerecord/
---
## MailMergeSettings.ActiveRecord property

Specifies the one-based index of the record from the data source which shall be displayed in Microsoft Word. The default value is 1.

```csharp
public int ActiveRecord { get; set; }
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
* namespace [Aspose.Words.Settings](../../../aspose.words.settings/)
* assembly [Aspose.Words](../../../)
