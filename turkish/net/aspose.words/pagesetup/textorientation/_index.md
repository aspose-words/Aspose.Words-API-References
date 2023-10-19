---
title: PageSetup.TextOrientation
linktitle: TextOrientation
articleTitle: TextOrientation
second_title: Aspose.Words for .NET
description: PageSetup TextOrientation mülk. Belirlemeye izin verirTextOrientation tüm sayfa için. Varsayılan değerHorizontal C#'da.
type: docs
weight: 430
url: /tr/net/aspose.words/pagesetup/textorientation/
---
## PageSetup.TextOrientation property

Belirlemeye izin verir`TextOrientation` tüm sayfa için. Varsayılan değer:Horizontal

```csharp
public TextOrientation TextOrientation { get; set; }
```

## Notlar

Bu özellik yalnızca MS Word yerel biçimleri DOCX, WML, RTF ve DOC için desteklenir.

## Örnekler

Metin yönünün nasıl ayarlanacağını gösterir.

```csharp
Document doc = new Document();

DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Hello world!");

// Metnin tamamını 90 derece döndürmek için "TextOrientation" özelliğini "TextOrientation.Upward" olarak ayarlayın
// sağa doğru, böylece tüm soldan sağa metinler artık yukarıdan aşağıya doğru gidiyor.
PageSetup pageSetup = doc.Sections[0].PageSetup;
pageSetup.TextOrientation = TextOrientation.Upward;

doc.Save(ArtifactsDir + "PageSetup.SetTextOrientation.docx");
```

### Ayrıca bakınız

* enum [TextOrientation](../../textorientation/)
* class [PageSetup](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
