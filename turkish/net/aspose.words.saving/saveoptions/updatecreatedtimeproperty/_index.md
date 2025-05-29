---
title: SaveOptions.UpdateCreatedTimeProperty
linktitle: UpdateCreatedTimeProperty
articleTitle: UpdateCreatedTimeProperty
second_title: .NET için Aspose.Words
description: SaveOptions'ınızı UpdateCreatedTimeProperty ile optimize edin. Kaydetmeden önce CreatedTime güncellemelerini kontrol edin, veri doğruluğunu artırın. Varsayılan, false.
type: docs
weight: 160
url: /tr/net/aspose.words.saving/saveoptions/updatecreatedtimeproperty/
---
## SaveOptions.UpdateCreatedTimeProperty property

Bir değeri alır veya ayarlar.[`CreatedTime`](../../../aspose.words.properties/builtindocumentproperties/createdtime/) özellik kaydedilmeden önce güncellenir. Varsayılan değer`YANLIŞ` ;

```csharp
public bool UpdateCreatedTimeProperty { get; set; }
```

## Örnekler

Bir belgenin "CreatedTime" özelliğinin kaydedilirken nasıl güncelleneceğini gösterir.

```csharp
Document doc = new Document();

DateTime createdTime = new DateTime(2019, 12, 20);
doc.BuiltInDocumentProperties.CreatedTime = createdTime;

// Bu bayrak, yerleşik bir özellik olan oluşturulan zamanın güncellenip güncellenmeyeceğini belirler.
// Eğer öyleyse, belgenin en son kaydedilme işleminin tarihi
// Parametre olarak geçirilen bu SaveOptions nesnesi oluşturulma zamanı olarak kullanılır.
DocSaveOptions saveOptions = new DocSaveOptions();
saveOptions.UpdateCreatedTimeProperty = isUpdateCreatedTimeProperty;

doc.Save(ArtifactsDir + "DocSaveOptions.UpdateCreatedTimeProperty.docx", saveOptions);

// Kaydedilen belgeyi açın, ardından özelliğin değerini doğrulayın.
doc = new Document(ArtifactsDir + "DocSaveOptions.UpdateCreatedTimeProperty.docx");

if (isUpdateCreatedTimeProperty)
    Assert.AreNotEqual(createdTime, doc.BuiltInDocumentProperties.CreatedTime);
else
    Assert.AreEqual(createdTime, doc.BuiltInDocumentProperties.CreatedTime);
```

### Ayrıca bakınız

* class [SaveOptions](../)
* ad alanı [Aspose.Words.Saving](../../../aspose.words.saving/)
* toplantı [Aspose.Words](../../../)
