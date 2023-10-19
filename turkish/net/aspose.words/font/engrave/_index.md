---
title: Font.Engrave
linktitle: Engrave
articleTitle: Engrave
second_title: Aspose.Words for .NET
description: Font Engrave mülk. Yazı tipi gravür olarak biçimlendirilmişse doğrudur C#'da.
type: docs
weight: 120
url: /tr/net/aspose.words/font/engrave/
---
## Font.Engrave property

Yazı tipi gravür olarak biçimlendirilmişse doğrudur.

```csharp
public bool Engrave { get; set; }
```

## Örnekler

Metne gravür/kabartma efektlerinin nasıl uygulanacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Size = 36;
builder.Font.Color = Color.LightBlue;

// Aşağıda metne 3B benzeri bir efekt uygulamak için gölgeleri kullanmanın iki yolu verilmiştir.
// 1 - Harflerin sayfaya gömülmüş gibi görünmesini sağlamak için metni kazıyın:
builder.Font.Engrave = true;

builder.Writeln("This text is engraved.");

// 2 - Harflerin sayfadan fırlamış gibi görünmesini sağlamak için metni kabartın:
builder.Font.Engrave = false;
builder.Font.Emboss = true;

builder.Writeln("This text is embossed.");

doc.Save(ArtifactsDir + "Font.EngraveEmboss.docx");
```

### Ayrıca bakınız

* class [Font](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
