---
title: SaveOptions.UpdateLastSavedTimeProperty
linktitle: UpdateLastSavedTimeProperty
articleTitle: UpdateLastSavedTimeProperty
second_title: Aspose.Words for .NET
description: SaveOptions UpdateLastSavedTimeProperty mülk. Bir değer alır veya ayarlar.LastSavedTime özellik kaydedilmeden önce güncellenir C#'da.
type: docs
weight: 180
url: /tr/net/aspose.words.saving/saveoptions/updatelastsavedtimeproperty/
---
## SaveOptions.UpdateLastSavedTimeProperty property

Bir değer alır veya ayarlar.[`LastSavedTime`](../../../aspose.words.properties/builtindocumentproperties/lastsavedtime/) özellik kaydedilmeden önce güncellenir.

```csharp
public bool UpdateLastSavedTimeProperty { get; set; }
```

## Örnekler

Kaydederken belgenin "Son kaydedilen zaman" özelliğinin korunup korunmayacağının nasıl belirleneceğini gösterir.

```csharp
Document doc = new Document(MyDir + "Document.docx");

Assert.AreEqual(new DateTime(2021, 5, 11, 6, 32, 0), 
    doc.BuiltInDocumentProperties.LastSavedTime);

// Belgeyi OOXML formatında kaydettiğimizde bir OoxmlSaveOptions nesnesi oluşturabiliriz
// ve ardından belgeyi kaydetme şeklimizi değiştirmek için bunu belgenin kaydetme yöntemine aktarın.
// "UpdateLastSavedTimeProperty" özelliğini "true" olarak ayarlayın
// çıktı belgesinin "Son kaydedilen zaman" yerleşik özelliğini geçerli tarih/saat olarak ayarlayın.
// "UpdateLastSavedTimeProperty" özelliğini "false" olarak ayarlayın
// giriş belgesinin "Son kaydedilen zaman" yerleşik özelliğinin orijinal değerini koruyun.
OoxmlSaveOptions saveOptions = new OoxmlSaveOptions();
saveOptions.UpdateLastSavedTimeProperty = updateLastSavedTimeProperty;

doc.Save(ArtifactsDir + "OoxmlSaveOptions.LastSavedTime.docx", saveOptions);

doc = new Document(ArtifactsDir + "OoxmlSaveOptions.LastSavedTime.docx");
DateTime lastSavedTimeNew = doc.BuiltInDocumentProperties.LastSavedTime;

if (updateLastSavedTimeProperty)
    Assert.That(DateTime.Now, Is.EqualTo(lastSavedTimeNew).Within(1).Days);
else
    Assert.AreEqual(new DateTime(2021, 5, 11, 6, 32, 0), 
        lastSavedTimeNew);
```

### Ayrıca bakınız

* class [SaveOptions](../)
* ad alanı [Aspose.Words.Saving](../../../aspose.words.saving/)
* toplantı [Aspose.Words](../../../)
