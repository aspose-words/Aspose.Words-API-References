---
title: MailMergeSettings.MailAsAttachment
linktitle: MailAsAttachment
articleTitle: MailAsAttachment
second_title: Aspose.Words för .NET
description: MailMergeSettings MailAsAttachment fast egendom. Anger att dokumenten som skapas under en sammankopplingsåtgärd ska skickas som en bilaga via epost snarare än själva epostmeddelandets brödtext. Standardvärdet ärfalsk  i C#.
type: docs
weight: 120
url: /sv/net/aspose.words.settings/mailmergesettings/mailasattachment/
---
## MailMergeSettings.MailAsAttachment property

Anger att dokumenten som skapas under en sammankopplingsåtgärd ska skickas som en bilaga via e-post snarare än själva e-postmeddelandets brödtext. Standardvärdet är`falsk` .

```csharp
public bool MailAsAttachment { get; set; }
```

## Exempel

Visar hur man kör en sammankoppling av brev samtidigt som man ansluter till en extern datakälla.

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
// Microsoft Word kommer inte längre att köra en e-postsammanfogning när vi använder den för att ladda dokumentet.
settings.Clear();

doc.Save(ArtifactsDir + "MailMerge.OdsoEmail.docx");
```

### Se även

* class [MailMergeSettings](../)
* namnutrymme [Aspose.Words.Settings](../../../aspose.words.settings/)
* hopsättning [Aspose.Words](../../../)
