---
title: BuiltInDocumentProperties.RevisionNumber
linktitle: RevisionNumber
articleTitle: RevisionNumber
second_title: Aspose.Words for .NET
description: BuiltInDocumentProperties RevisionNumber mülk. Belge revizyon numarasını alır veya ayarlar C#'da.
type: docs
weight: 240
url: /tr/net/aspose.words.properties/builtindocumentproperties/revisionnumber/
---
## BuiltInDocumentProperties.RevisionNumber property

Belge revizyon numarasını alır veya ayarlar.

```csharp
public int RevisionNumber { get; set; }
```

## Notlar

Aspose.Words bu özelliği güncellemez.

## Örnekler

REVNUM alanlarıyla nasıl çalışılacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Current revision #");

// Belgenin geçerli revizyon numarası özelliğini görüntüleyen bir REVNUM alanı ekleyin.
FieldRevNum field = (FieldRevNum)builder.InsertField(FieldType.FieldRevisionNum, true);

Assert.AreEqual(" REVNUM ", field.GetFieldCode());
Assert.AreEqual("1", field.Result);
Assert.AreEqual(1, doc.BuiltInDocumentProperties.RevisionNumber);

// Bu özellik bir belgenin Microsoft Word'de kaç kez kaydedildiğini sayar,
// ve izlenen revizyonlarla ilgisi yoktur. Windows Gezgini'nde belgeye sağ tıklayarak bulabiliriz
// Özellikler aracılığıyla -> Detaylar. Bu özelliği manuel olarak güncelleyebiliriz.
doc.BuiltInDocumentProperties.RevisionNumber++;
field.Update();

Assert.AreEqual("2", field.Result);
```

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
