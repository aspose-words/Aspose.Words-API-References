---
title: FontFallbackSettings.Save
linktitle: Save
articleTitle: Save
second_title: .NET için Aspose.Words
description: Sezgisel Kaydetme yöntemimizle FontFallbackSettings'inizi zahmetsizce kaydedin. Sorunsuz font yönetimi için özel yedek ayarlarınızı koruyun.
type: docs
weight: 50
url: /tr/net/aspose.words.fonts/fontfallbacksettings/save/
---
## Save(*Stream*) {#save}

Mevcut yedek ayarları akışa kaydeder.

```csharp
public void Save(Stream outputStream)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| outputStream | Stream | Çıkış akışı. |

## Örnekler

Bir akışa yazı tipi yedek ayarlarının nasıl yükleneceğini ve kaydedileceğini gösterir.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

// Bir dizi yazı tipi geri dönüş ayarını tanımlayan bir XML belgesi yükleyin.
using (FileStream fontFallbackStream = new FileStream(MyDir + "Font fallback rules.xml", FileMode.Open))
{
    FontSettings fontSettings = new FontSettings();
    fontSettings.FallbackSettings.Load(fontFallbackStream);

    doc.FontSettings = fontSettings;
}

doc.Save(ArtifactsDir + "FontSettings.LoadFontFallbackSettingsFromStream.pdf");

// Belgemizin geçerli yazı tipi yedek ayarlarını XML belgesi olarak kaydetmek için bir akış kullanın.
using (FileStream fontFallbackStream =
    new FileStream(ArtifactsDir + "FallbackSettings.xml", FileMode.Create))
{
    doc.FontSettings.FallbackSettings.Save(fontFallbackStream);
}
```

### Ayrıca bakınız

* class [FontFallbackSettings](../)
* ad alanı [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* toplantı [Aspose.Words](../../../)

---

## Save(*string*) {#save_1}

Mevcut geri dönüş ayarlarını dosyaya kaydeder.

```csharp
public void Save(string fileName)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| fileName | String | Çıktı dosya adı. |

## Örnekler

Yerel dosya sistemindeki bir XML belgesine yazı tipi yedek ayarlarının nasıl yükleneceğini ve kaydedileceğini gösterir.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

// Bir dizi yazı tipi geri dönüş ayarını tanımlayan bir XML belgesi yükleyin.
FontSettings fontSettings = new FontSettings();
fontSettings.FallbackSettings.Load(MyDir + "Font fallback rules.xml");

doc.FontSettings = fontSettings;
doc.Save(ArtifactsDir + "FontSettings.LoadFontFallbackSettingsFromFile.pdf");

// Belgemizin geçerli yazı tipi yedek ayarlarını XML belgesi olarak kaydedelim.
doc.FontSettings.FallbackSettings.Save(ArtifactsDir + "FallbackSettings.xml");
```

### Ayrıca bakınız

* class [FontFallbackSettings](../)
* ad alanı [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* toplantı [Aspose.Words](../../../)
