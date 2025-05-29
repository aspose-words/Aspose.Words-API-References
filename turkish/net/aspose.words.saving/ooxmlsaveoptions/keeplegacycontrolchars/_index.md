---
title: OoxmlSaveOptions.KeepLegacyControlChars
linktitle: KeepLegacyControlChars
articleTitle: KeepLegacyControlChars
second_title: .NET için Aspose.Words
description: Sorunsuz belge dönüşümü için eski denetim karakterlerinin orijinal biçimini korumak amacıyla OoxmlSaveOptions' KeepLegacyControlChars özelliğini keşfedin.
type: docs
weight: 50
url: /tr/net/aspose.words.saving/ooxmlsaveoptions/keeplegacycontrolchars/
---
## OoxmlSaveOptions.KeepLegacyControlChars property

Eski kontrol karakterlerinin orijinal gösterimini korur.

```csharp
public bool KeepLegacyControlChars { get; set; }
```

## Örnekler

.docx'e dönüştürürken eski kontrol karakterlerinin nasıl destekleneceğini gösterir.

```csharp
Document doc = new Document(MyDir + "Legacy control character.doc");

// Belgeyi OOXML biçiminde kaydettiğimizde, bir OoxmlSaveOptions nesnesi oluşturabiliriz
// ve ardından belgenin nasıl kaydedileceğini değiştirmek için bunu belgenin kaydetme yöntemine geçiriyoruz.
// "KeepLegacyControlChars" özelliğini korumak için "true" olarak ayarlayın
// Kaydederken "ShortDateTime" eski karakteri.
// "KeepLegacyControlChars" özelliğini kaldırmak için "false" olarak ayarlayın
// çıktı belgesindeki "ShortDateTime" eski karakteri.
OoxmlSaveOptions so = new OoxmlSaveOptions(SaveFormat.Docx);
so.KeepLegacyControlChars = keepLegacyControlChars;

doc.Save(ArtifactsDir + "OoxmlSaveOptions.KeepLegacyControlChars.docx", so);

doc = new Document(ArtifactsDir + "OoxmlSaveOptions.KeepLegacyControlChars.docx");

Assert.AreEqual(keepLegacyControlChars ? "\u0013date \\@ \"MM/dd/yyyy\"\u0014\u0015\f" : "\u001e\f",
    doc.FirstSection.Body.GetText());
```

### Ayrıca bakınız

* class [OoxmlSaveOptions](../)
* ad alanı [Aspose.Words.Saving](../../../aspose.words.saving/)
* toplantı [Aspose.Words](../../../)
