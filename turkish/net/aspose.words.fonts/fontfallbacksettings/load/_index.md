---
title: FontFallbackSettings.Load
linktitle: Load
articleTitle: Load
second_title: .NET için Aspose.Words
description: Sorunsuz tipografi entegrasyonu için FontFallbackSettings Yükleme yöntemi ile XML dosyalarından yazı tipi yedek ayarlarını zahmetsizce yükleyin ve yönetin.
type: docs
weight: 20
url: /tr/net/aspose.words.fonts/fontfallbacksettings/load/
---
## Load(*string*) {#load_1}

XML dosyasından yazı tipi yedek ayarlarını yükler.

```csharp
public void Load(string fileName)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| fileName | String | Dosya adını girin. |

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

---

## Load(*Stream*) {#load}

XML akışından yedek ayarları yükler.

```csharp
public void Load(Stream stream)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| stream | Stream | Giriş akışı. |

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
