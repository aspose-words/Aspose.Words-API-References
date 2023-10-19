---
title: FontFallbackSettings.Load
linktitle: Load
articleTitle: Load
second_title: Aspose.Words for .NET
description: FontFallbackSettings Load yöntem. XML dosyasından yazı tipi yedek ayarlarını yükler C#'da.
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

Yazı tipi geri dönüş ayarlarının yerel dosya sistemindeki bir XML belgesine/bir XML belgesinden nasıl yükleneceğini ve kaydedileceğini gösterir.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

// Bir dizi yazı tipi geri dönüş ayarını tanımlayan bir XML belgesi yükleyin.
FontSettings fontSettings = new FontSettings();
fontSettings.FallbackSettings.Load(MyDir + "Font fallback rules.xml");

doc.FontSettings = fontSettings;
doc.Save(ArtifactsDir + "FontSettings.LoadFontFallbackSettingsFromFile.pdf");

// Belgemizin mevcut yazı tipi yedek ayarlarını XML belgesi olarak kaydedin.
doc.FontSettings.FallbackSettings.Save(ArtifactsDir + "FallbackSettings.xml");
```

### Ayrıca bakınız

* class [FontFallbackSettings](../)
* ad alanı [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* toplantı [Aspose.Words](../../../)

---

## Load(*Stream*) {#load}

XML akışından geri dönüş ayarlarını yükler.

```csharp
public void Load(Stream stream)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| stream | Stream | Giriş akışı. |

## Örnekler

Yazı tipi geri dönüş ayarlarının bir akışa nasıl yüklenip kaydedileceğini gösterir.

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

// Belgemizin mevcut yazı tipi geri dönüş ayarlarını XML belgesi olarak kaydetmek için bir akış kullanın.
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
