---
title: FontFallbackSettings.Save
second_title: Aspose.Words for .NET API Referansı
description: FontFallbackSettings yöntem. Geçerli geri dönüş ayarlarını akışa kaydeder.
type: docs
weight: 50
url: /tr/net/aspose.words.fonts/fontfallbacksettings/save/
---
## Save(Stream) {#save}

Geçerli geri dönüş ayarlarını akışa kaydeder.

```csharp
public void Save(Stream outputStream)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| outputStream | Stream | Çıkış akışı. |

### Örnekler

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
* ad alanı [Aspose.Words.Fonts](../../fontfallbacksettings/)
* toplantı [Aspose.Words](../../../)

---

## Save(string) {#save_1}

Geçerli geri dönüş ayarlarını dosyaya kaydeder.

```csharp
public void Save(string fileName)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| fileName | String | Çıkış dosyası adı. |

### Örnekler

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
* ad alanı [Aspose.Words.Fonts](../../fontfallbacksettings/)
* toplantı [Aspose.Words](../../../)


