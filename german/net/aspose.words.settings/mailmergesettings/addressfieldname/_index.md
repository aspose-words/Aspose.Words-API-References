---
title: MailMergeSettings.AddressFieldName
linktitle: AddressFieldName
articleTitle: AddressFieldName
second_title: Aspose.Words für .NET
description: Entdecken Sie die MailMergeSettings AddressFieldName-Eigenschaft, um Ihre E-Mail-Adressspalte einfach in Datenquellen anzugeben und so nahtlose E-Mail-Zusammenführungen sicherzustellen.
type: docs
weight: 30
url: /de/net/aspose.words.settings/mailmergesettings/addressfieldname/
---
## MailMergeSettings.AddressFieldName property

Gibt die Spalte innerhalb der Datenquelle an, die E-Mail-Adressen enthält. Der Standardwert ist eine leere Zeichenfolge.

```csharp
public string AddressFieldName { get; set; }
```

## Beispiele

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
* namensraum [Aspose.Words.Settings](../../../aspose.words.settings/)
* Montage [Aspose.Words](../../../)
