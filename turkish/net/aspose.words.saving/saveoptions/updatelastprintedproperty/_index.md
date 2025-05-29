---
title: SaveOptions.UpdateLastPrintedProperty
linktitle: UpdateLastPrintedProperty
articleTitle: UpdateLastPrintedProperty
second_title: .NET için Aspose.Words
description: SaveOptions UpdateLastPrintedProperty ile belge yönetimini optimize edin. Verimli kaydetme ve gelişmiş iş akışı için LastPrinted güncellemelerini kontrol edin.
type: docs
weight: 180
url: /tr/net/aspose.words.saving/saveoptions/updatelastprintedproperty/
---
## SaveOptions.UpdateLastPrintedProperty property

Bir değeri alır veya ayarlar.[`LastPrinted`](../../../aspose.words.properties/builtindocumentproperties/lastprinted/) özellik kaydedilmeden önce güncellenir.

```csharp
public bool UpdateLastPrintedProperty { get; set; }
```

## Örnekler

Bir belgenin kaydedilirken "Son yazdırılan" özelliğinin nasıl güncelleneceğini gösterir.

```csharp
Document doc = new Document();

DateTime lastPrinted = new DateTime(2019, 12, 20);
doc.BuiltInDocumentProperties.LastPrinted = lastPrinted;

// Bu bayrak, yerleşik bir özellik olan son yazdırılan tarihin güncellenip güncellenmeyeceğini belirler.
// Eğer öyleyse, belgenin en son kaydedilme işleminin tarihi
// Parametre olarak geçirilen bu SaveOptions nesnesi baskı tarihi olarak kullanılır.
DocSaveOptions saveOptions = new DocSaveOptions();
saveOptions.UpdateLastPrintedProperty = isUpdateLastPrintedProperty;

// Microsoft Word 2003'te bu özellik Dosya -> Özellikler -> İstatistikler -> Yazdırılan yoluyla bulunabilir.
// PRINTDATE alanı kullanılarak belgenin gövdesinde de görüntülenebilir.
doc.Save(ArtifactsDir + "DocSaveOptions.UpdateLastPrintedProperty.doc", saveOptions);

// Kaydedilen belgeyi açın, ardından özelliğin değerini doğrulayın.
doc = new Document(ArtifactsDir + "DocSaveOptions.UpdateLastPrintedProperty.doc");

if (isUpdateLastPrintedProperty)
    Assert.AreNotEqual(lastPrinted, doc.BuiltInDocumentProperties.LastPrinted);
else
    Assert.AreEqual(lastPrinted, doc.BuiltInDocumentProperties.LastPrinted);
```

### Ayrıca bakınız

* class [SaveOptions](../)
* ad alanı [Aspose.Words.Saving](../../../aspose.words.saving/)
* toplantı [Aspose.Words](../../../)
