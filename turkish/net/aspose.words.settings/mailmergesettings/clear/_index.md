---
title: MailMergeSettings.Clear
linktitle: Clear
articleTitle: Clear
second_title: Aspose.Words for .NET
description: MailMergeSettings Clear yöntem. Adresmektup birleştirme ayarlarını belge kaydedildiğinde hiçbir adresmektup birleştirme ayarı kaydedilmeyecek ve normal bir belge haline gelecek şekilde temizler C#'da.
type: docs
weight: 180
url: /tr/net/aspose.words.settings/mailmergesettings/clear/
---
## MailMergeSettings.Clear method

Adres-mektup birleştirme ayarlarını, belge kaydedildiğinde hiçbir adres-mektup birleştirme ayarı kaydedilmeyecek ve normal bir belge haline gelecek şekilde temizler.

```csharp
public void Clear()
```

## Örnekler

Dış veri kaynağına bağlanırken adres-mektup birleştirmenin nasıl yürütüleceğini gösterir.

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

// Bu ayarları temizleyerek sıfırlayabiliriz. Bunu yapıp belgeyi kaydettikten sonra,
// Microsoft Word artık belgeyi yüklemek için kullandığımızda adres-mektup birleştirme işlemini gerçekleştirmeyecek.
settings.Clear();

doc.Save(ArtifactsDir + "MailMerge.OdsoEmail.docx");
```

### Ayrıca bakınız

* class [MailMergeSettings](../)
* ad alanı [Aspose.Words.Settings](../../../aspose.words.settings/)
* toplantı [Aspose.Words](../../../)
