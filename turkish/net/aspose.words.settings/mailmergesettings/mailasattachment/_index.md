---
title: MailMergeSettings.MailAsAttachment
linktitle: MailAsAttachment
articleTitle: MailAsAttachment
second_title: .NET için Aspose.Words
description: MailMergeSettings'deki MailAsAttachment özelliğinin, birleştirilmiş belgeleri daha iyi etkileşim için ek olarak göndererek e-posta kampanyalarınızı nasıl geliştirdiğini keşfedin.
type: docs
weight: 120
url: /tr/net/aspose.words.settings/mailmergesettings/mailasattachment/
---
## MailMergeSettings.MailAsAttachment property

Bir posta birleştirme işlemi sırasında üretilen belgelerin gerçek e-postanın gövdesi yerine eki olarak e-postayla gönderilmesi gerektiğini belirtir. Varsayılan değer`YANLIŞ` .

```csharp
public bool MailAsAttachment { get; set; }
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
