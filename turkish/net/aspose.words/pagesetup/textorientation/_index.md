---
title: PageSetup.TextOrientation
second_title: Aspose.Words for .NET API Referansı
description: PageSetup mülk. Belirtmeye izin verirTextOrientation tüm sayfa için. Varsayılan değerHorizontal
type: docs
weight: 420
url: /tr/net/aspose.words/pagesetup/textorientation/
---
## PageSetup.TextOrientation property

Belirtmeye izin verir`TextOrientation` tüm sayfa için. Varsayılan değerHorizontal

```csharp
public TextOrientation TextOrientation { get; set; }
```

### Notlar

Bu özellik yalnızca MS Word yerel biçimleri DOCX, WML, RTF ve DOC için desteklenir.

### Örnekler

Metin yönünün nasıl ayarlanacağını gösterir.

```csharp
Document doc = new Document();

DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Hello world!");

// Tüm metni 90 derece döndürmek için "TextOrientation" özelliğini "TextOrientation.Upward" olarak ayarlayın
// sağa, böylece soldan sağa tüm metinler artık yukarıdan aşağıya gider.
PageSetup pageSetup = doc.Sections[0].PageSetup;
pageSetup.TextOrientation = TextOrientation.Upward;

doc.Save(ArtifactsDir + "PageSetup.SetTextOrientation.docx");
```

### Ayrıca bakınız

* enum [TextOrientation](../../textorientation/)
* class [PageSetup](../)
* ad alanı [Aspose.Words](../../pagesetup/)
* toplantı [Aspose.Words](../../../)


