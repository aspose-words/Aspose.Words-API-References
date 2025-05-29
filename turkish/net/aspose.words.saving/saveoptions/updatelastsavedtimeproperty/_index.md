---
title: SaveOptions.UpdateLastSavedTimeProperty
linktitle: UpdateLastSavedTimeProperty
articleTitle: UpdateLastSavedTimeProperty
second_title: .NET için Aspose.Words
description: SaveOptions'ınızı UpdateLastSavedTimeProperty ile optimize edin. Verimli veri yönetimi ve gelişmiş performans için LastSavedTime güncellemelerini kontrol edin.
type: docs
weight: 190
url: /tr/net/aspose.words.saving/saveoptions/updatelastsavedtimeproperty/
---
## SaveOptions.UpdateLastSavedTimeProperty property

Bir değeri alır veya ayarlar.[`LastSavedTime`](../../../aspose.words.properties/builtindocumentproperties/lastsavedtime/) özellik kaydedilmeden önce güncellenir.

```csharp
public bool UpdateLastSavedTimeProperty { get; set; }
```

## Örnekler

Kaydederken belgenin "Son kaydedildiği zaman" özelliğinin korunup korunmayacağının nasıl belirleneceğini gösterir.

```csharp
Document doc = new Document(MyDir + "Document.docx");

Assert.AreEqual(new DateTime(2021, 5, 11, 6, 32, 0), 
    doc.BuiltInDocumentProperties.LastSavedTime);

// Belgeyi OOXML biçiminde kaydettiğimizde, bir OoxmlSaveOptions nesnesi oluşturabiliriz
// ve ardından belgenin nasıl kaydedileceğini değiştirmek için bunu belgenin kaydetme yöntemine geçiriyoruz.
// "UpdateLastSavedTimeProperty" özelliğini "true" olarak ayarlayın
// çıktı belgesinin "Son kaydedilen zaman" yerleşik özelliğini geçerli tarih/saate ayarla.
// "UpdateLastSavedTimeProperty" özelliğini "false" olarak ayarlayın
// Giriş belgesinin "Son kaydedilen zaman" yerleşik özelliğinin orijinal değerini koru.
OoxmlSaveOptions saveOptions = new OoxmlSaveOptions();
saveOptions.UpdateLastSavedTimeProperty = updateLastSavedTimeProperty;

doc.Save(ArtifactsDir + "OoxmlSaveOptions.LastSavedTime.docx", saveOptions);

doc = new Document(ArtifactsDir + "OoxmlSaveOptions.LastSavedTime.docx");
DateTime lastSavedTimeNew = doc.BuiltInDocumentProperties.LastSavedTime;

if (updateLastSavedTimeProperty)
    Assert.IsTrue((DateTime.Now - lastSavedTimeNew).Days < 1);
else
    Assert.AreEqual(new DateTime(2021, 5, 11, 6, 32, 0), 
        lastSavedTimeNew);
```

### Ayrıca bakınız

* class [SaveOptions](../)
* ad alanı [Aspose.Words.Saving](../../../aspose.words.saving/)
* toplantı [Aspose.Words](../../../)
