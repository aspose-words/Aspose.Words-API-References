---
title: BuiltInDocumentProperties.LastPrinted
linktitle: LastPrinted
articleTitle: LastPrinted
second_title: Aspose.Words for .NET
description: BuiltInDocumentProperties LastPrinted mülk. Belgenin en son UTCde yazdırıldığı tarihi alır veya ayarlar C#'da.
type: docs
weight: 150
url: /tr/net/aspose.words.properties/builtindocumentproperties/lastprinted/
---
## BuiltInDocumentProperties.LastPrinted property

Belgenin en son UTC'de yazdırıldığı tarihi alır veya ayarlar.

```csharp
public DateTime LastPrinted { get; set; }
```

## Notlar

RTF formatından oluşturulan belgeler için bu özellik, son yazdırma işleminin yerel saatini döndürür.

Belge hiç yazdırılmadıysa bu özellik DateTime.MinValue değerini döndürür.

Aspose.Words bu özelliği güncellemez.

## Örnekler

"Orijin" kategorisindeki belge özellikleriyle nasıl çalışılacağını gösterir.

```csharp
// Microsoft Word kullanarak oluşturduğumuz ve düzenlediğimiz bir belgeyi açın.
Document doc = new Document(MyDir + "Properties.docx");
BuiltInDocumentProperties properties = doc.BuiltInDocumentProperties;

// Aşağıdaki yerleşik özellikler bu belgenin oluşturulmasına ve düzenlenmesine ilişkin bilgiler içerir.
// Windows Explorer'da bu belgeye sağ tıklayıp bulabiliriz
// bu özellikler "Özellikler" aracılığıyla -> "Ayrıntılar" -> "Köken" kategorisi.
// PRINTDATE ve EDITTIME gibi alanlar bu değerleri belge gövdesinde görüntüleyebilir.
Console.WriteLine($"Created using {properties.NameOfApplication}, on {properties.CreatedTime}");
Console.WriteLine($"Minutes spent editing: {properties.TotalEditingTime}");
Console.WriteLine($"Date/time last printed: {properties.LastPrinted}");
Console.WriteLine($"Template document: {properties.Template}");

// Yerleşik özelliklerin değerlerini de değiştirebiliriz.
properties.Company = "Doe Ltd.";
properties.Manager = "Jane Doe";
properties.Version = 5;
properties.RevisionNumber++;

// Microsoft Word, belgeyi kaydettiğimizde aşağıdaki özellikleri otomatik olarak günceller.
// Bu özellikleri Aspose.Words ile kullanmak için değerleri manuel olarak ayarlamamız gerekecek.
properties.LastSavedBy = "John Doe";
properties.LastSavedTime = DateTime.Now;

// Windows Explorer'da bu belgeye sağ tıklayıp bulabiliriz these properties in "Properties" -> "Details" -> "Origin".
doc.Save(ArtifactsDir + "DocumentProperties.Origin.docx");
```

### Ayrıca bakınız

* class [BuiltInDocumentProperties](../)
* ad alanı [Aspose.Words.Properties](../../../aspose.words.properties/)
* toplantı [Aspose.Words](../../../)
