---
title: Odso.UdlConnectString
linktitle: UdlConnectString
articleTitle: UdlConnectString
second_title: .NET için Aspose.Words
description: UDL kullanarak harici veri kaynaklarına sorunsuz bağlantılar için Odso UdlConnectString özelliğini keşfedin. Veri entegrasyonunu kolaylıkla ve verimli bir şekilde açın!
type: docs
weight: 90
url: /tr/net/aspose.words.settings/odso/udlconnectstring/
---
## Odso.UdlConnectString property

Harici bir veri kaynağına bağlanmak için kullanılan Evrensel Veri Bağlantısı (UDL) bağlantı dizesini belirtir. Varsayılan değer boş bir dizedir.

```csharp
public string UdlConnectString { get; set; }
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

* class [Odso](../)
* ad alanı [Aspose.Words.Settings](../../../aspose.words.settings/)
* toplantı [Aspose.Words](../../../)
