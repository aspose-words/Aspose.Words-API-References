---
title: MailMergeSettings.AddressFieldName
linktitle: AddressFieldName
articleTitle: AddressFieldName
second_title: .NET için Aspose.Words
description: Sorunsuz e-posta birleştirmelerini garantilemek için veri kaynaklarında e-posta adresi sütununuzu kolayca belirtmek üzere MailMergeSettings AddressFieldName özelliğini keşfedin.
type: docs
weight: 30
url: /tr/net/aspose.words.settings/mailmergesettings/addressfieldname/
---
## MailMergeSettings.AddressFieldName property

Veri kaynağında e-posta adreslerini içeren sütunu belirtir. Varsayılan değer boş bir dizedir.

```csharp
public string AddressFieldName { get; set; }
```

## Örnekler

Harici bir veri kaynağına bağlanırken posta birleştirmenin nasıl gerçekleştirileceğini gösterir.

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
// Belgeyi yüklemek için Microsoft Word kullanıldığında artık posta birleştirme işlemi gerçekleştirilmeyecek.
settings.Clear();

doc.Save(ArtifactsDir + "MailMerge.OdsoEmail.docx");
```

### Ayrıca bakınız

* class [MailMergeSettings](../)
* ad alanı [Aspose.Words.Settings](../../../aspose.words.settings/)
* toplantı [Aspose.Words](../../../)
