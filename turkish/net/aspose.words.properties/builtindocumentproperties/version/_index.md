---
title: BuiltInDocumentProperties.Version
second_title: Aspose.Words for .NET API Referansı
description: BuiltInDocumentProperties mülk. Belgeyi oluşturan uygulamanın sürüm numarasını temsil eder.
type: docs
weight: 320
url: /tr/net/aspose.words.properties/builtindocumentproperties/version/
---
## BuiltInDocumentProperties.Version property

Belgeyi oluşturan uygulamanın sürüm numarasını temsil eder.

```csharp
public int Version { get; set; }
```

### Notlar

Bir belge Microsoft Word tarafından oluşturulduğunda, yüksek 16 bit ana sürümü temsil eder ve düşük 16 bit ise yapı numarasını temsil eder.

### Örnekler

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
* ad alanı [Aspose.Words.Properties](../../builtindocumentproperties/)
* toplantı [Aspose.Words](../../../)


