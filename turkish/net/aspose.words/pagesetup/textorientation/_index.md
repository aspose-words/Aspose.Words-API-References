---
title: PageSetup.TextOrientation
linktitle: TextOrientation
articleTitle: TextOrientation
second_title: .NET için Aspose.Words
description: Sayfa metin yönünü kolayca ayarlamak için PageSetup TextOrientation özelliğini keşfedin. Varsayılan Yatay'ın ötesinde seçeneklerle düzeninizi özelleştirin.
type: docs
weight: 430
url: /tr/net/aspose.words/pagesetup/textorientation/
---
## PageSetup.TextOrientation property

Belirtmeye izin verir`TextOrientation` tüm sayfa için. Varsayılan değerHorizontal

```csharp
public TextOrientation TextOrientation { get; set; }
```

## Notlar

Bu özellik yalnızca MS Word'ün yerel biçimleri olan DOCX, WML, RTF ve DOC için desteklenir.

## Örnekler

Metin yönünün nasıl ayarlanacağını gösterir.

```csharp
Document doc = new Document();

DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Hello world!");

// Tüm metni 90 derece döndürmek için "TextOrientation" özelliğini "TextOrientation.Upward" olarak ayarlayın
// böylece tüm soldan sağa metinler yukarıdan aşağıya doğru gidecek.
PageSetup pageSetup = doc.Sections[0].PageSetup;
pageSetup.TextOrientation = TextOrientation.Upward;

doc.Save(ArtifactsDir + "PageSetup.SetTextOrientation.docx");
```

### Ayrıca bakınız

* enum [TextOrientation](../../textorientation/)
* class [PageSetup](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
