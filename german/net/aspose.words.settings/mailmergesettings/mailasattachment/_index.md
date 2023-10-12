---
title: MailMergeSettings.MailAsAttachment
second_title: Aspose.Words für .NET-API-Referenz
description: MailMergeSettings eigendom. Gibt an dass die während eines Seriendruckvorgangs erstellten Dokumente als Anhang und nicht als und nicht als Text der eigentlichen EMail per EMail gesendet werden sollen. Der Standardwert istFALSCH .
type: docs
weight: 120
url: /de/net/aspose.words.settings/mailmergesettings/mailasattachment/
---
## MailMergeSettings.MailAsAttachment property

Gibt an, dass die während eines Seriendruckvorgangs erstellten Dokumente als Anhang und nicht als und nicht als Text der eigentlichen E-Mail per E-Mail gesendet werden sollen. Der Standardwert ist`FALSCH` .

```csharp
public bool MailAsAttachment { get; set; }
```

### Beispiele

Zeigt, wie ein Serienbrief ausgeführt wird, während eine Verbindung zu einer externen Datenquelle hergestellt wird.

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

// Wir können diese Einstellungen zurücksetzen, indem wir sie löschen. Sobald wir das getan und das Dokument gespeichert haben,
// Microsoft Word führt keinen Serienbrief mehr aus, wenn wir es zum Laden des Dokuments verwenden.
settings.Clear();

doc.Save(ArtifactsDir + "MailMerge.OdsoEmail.docx");
```

### Siehe auch

* class [MailMergeSettings](../)
* namensraum [Aspose.Words.Settings](../../mailmergesettings/)
* Montage [Aspose.Words](../../../)


