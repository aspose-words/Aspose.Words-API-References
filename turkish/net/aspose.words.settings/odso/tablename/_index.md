---
title: Odso.TableName
second_title: Aspose.Words for .NET API Referansı
description: Odso mülk. Bir kaynağın harici bir veri kaynağı içinde bağlanacağı belirli veri kümesini belirtir. Varsayılan değer boş bir dizedir.
type: docs
weight: 80
url: /tr/net/aspose.words.settings/odso/tablename/
---
## Odso.TableName property

Bir kaynağın harici bir veri kaynağı içinde bağlanacağı belirli veri kümesini belirtir. Varsayılan değer boş bir dizedir.

```csharp
public string TableName { get; set; }
```

### Örnekler

Harici bir veri kaynağına bağlanırken adres mektup birleştirmenin nasıl yürütüleceğini gösterir.

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

// Bu ayarları temizleyerek sıfırlayabiliriz. Bunu yaptıktan ve belgeyi kaydettikten sonra,
// Microsoft Word, belgeyi yüklemek için kullandığımızda artık adres mektup birleştirme gerçekleştirmeyecek.
settings.Clear();

doc.Save(ArtifactsDir + "MailMerge.OdsoEmail.docx");
```

### Ayrıca bakınız

* class [Odso](../)
* ad alanı [Aspose.Words.Settings](../../odso/)
* toplantı [Aspose.Words](../../../)


