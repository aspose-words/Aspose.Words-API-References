---
title: Font.Emboss
linktitle: Emboss
articleTitle: Emboss
second_title: .NET için Aspose.Words
description: Göz alıcı tasarımlar için metninizi şık bir kabartma efektiyle geliştiren Font Emboss özelliğini keşfedin. Tipografinizi bugün yükseltin!
type: docs
weight: 100
url: /tr/net/aspose.words/font/emboss/
---
## Font.Emboss property

Yazı tipi kabartmalı olarak biçimlendirilmişse doğrudur.

```csharp
public bool Emboss { get; set; }
```

## Örnekler

Metne gravür/kabartma efektlerinin nasıl uygulanacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Size = 36;
builder.Font.Color = Color.LightBlue;

// Aşağıda metne 3 boyutlu efekt vermek için gölgelerin kullanıldığı iki yol gösterilmektedir.
// 1 - Harflerin sayfaya gömülmüş gibi görünmesi için metni kazıyın:
builder.Font.Engrave = true;

builder.Writeln("This text is engraved.");

// 2 - Harflerin sayfadan fırlayacakmış gibi görünmesi için metni kabartın:
builder.Font.Engrave = false;
builder.Font.Emboss = true;

builder.Writeln("This text is embossed.");

doc.Save(ArtifactsDir + "Font.EngraveEmboss.docx");
```

### Ayrıca bakınız

* class [Font](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
