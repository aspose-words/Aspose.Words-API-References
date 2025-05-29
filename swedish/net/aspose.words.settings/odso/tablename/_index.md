---
title: Odso.TableName
linktitle: TableName
articleTitle: TableName
second_title: Aspose.Words för .NET
description: Upptäck egenskapen Odso TableName, anslut enkelt till specifika datamängder i externa källor och förbättra dataintegrationen med lätthet.
type: docs
weight: 80
url: /sv/net/aspose.words.settings/odso/tablename/
---
## Odso.TableName property

Anger den specifika datamängd som en källa ska vara kopplad till inom en extern datakälla. Standardvärdet är en tom sträng.

```csharp
public string TableName { get; set; }
```

## Exempel

Visar hur man utför en dokumentkoppling när man ansluter till en extern datakälla.

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

// Vi kan återställa dessa inställningar genom att rensa dem. När vi har gjort det och sparat dokumentet,
// Microsoft Word kommer inte längre att köra en dokumentkoppling när vi använder det för att läsa in dokumentet.
settings.Clear();

doc.Save(ArtifactsDir + "MailMerge.OdsoEmail.docx");
```

### Se även

* class [Odso](../)
* namnutrymme [Aspose.Words.Settings](../../../aspose.words.settings/)
* hopsättning [Aspose.Words](../../../)
