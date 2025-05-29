---
title: BuiltInDocumentProperties.Template
linktitle: Template
articleTitle: Template
second_title: .NET için Aspose.Words
description: Gelişmiş organizasyon ve verimlilik için belgenizin bilgilendirici adını kolayca yönetmek üzere BuiltInDocumentProperties Şablon özelliğini keşfedin.
type: docs
weight: 300
url: /tr/net/aspose.words.properties/builtindocumentproperties/template/
---
## BuiltInDocumentProperties.Template property

Belge şablonunun bilgilendirici adını alır veya ayarlar.

```csharp
public string Template { get; set; }
```

## Notlar

Microsoft Word'de bu özellik yalnızca bilgilendirme amaçlıdır ve genellikle yolu belirtmeden yalnızca şablonun dosya adını içerir.

Boş dize, belgenin Normal şablonuna eklendiği anlamına gelir.

Ekli şablonun gerçek adını almak veya ayarlamak için the kullanın[`AttachedTemplate`](../../../aspose.words/document/attachedtemplate/) mülk.

## Örnekler

"Origin" kategorisindeki belge özellikleriyle nasıl çalışılacağını gösterir.

```csharp
// Microsoft Word kullanarak oluşturduğumuz ve düzenlediğimiz bir belgeyi açalım.
Document doc = new Document(MyDir + "Properties.docx");
BuiltInDocumentProperties properties = doc.BuiltInDocumentProperties;

// Aşağıdaki yerleşik özellikler, bu belgenin oluşturulması ve düzenlenmesiyle ilgili bilgileri içerir.
// Bu belgeye Windows Gezgini'nde sağ tıklayıp bulabiliriz
// bu özellikler "Özellikler" -> "Ayrıntılar" -> "Köken" kategorisi aracılığıyla.
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
// Bu özellikleri Aspose.Words ile kullanmak için, bunlara manuel olarak değer ayarlamamız gerekecek.
properties.LastSavedBy = "John Doe";
properties.LastSavedTime = DateTime.Now;

// Bu belgeye Windows Gezgini'nde sağ tıklayıp bulabiliriz these properties in "Properties" -> "Details" -> "Origin".
doc.Save(ArtifactsDir + "DocumentProperties.Origin.docx");
```

### Ayrıca bakınız

* class [BuiltInDocumentProperties](../)
* ad alanı [Aspose.Words.Properties](../../../aspose.words.properties/)
* toplantı [Aspose.Words](../../../)
