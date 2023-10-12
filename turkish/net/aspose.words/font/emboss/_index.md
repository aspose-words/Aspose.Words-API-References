---
title: Font.Emboss
second_title: Aspose.Words for .NET API Referansı
description: Font mülk. Yazı tipi kabartmalı olarak biçimlendirilmişse doğrudur.
type: docs
weight: 100
url: /tr/net/aspose.words/font/emboss/
---
## Font.Emboss property

Yazı tipi kabartmalı olarak biçimlendirilmişse doğrudur.

```csharp
public bool Emboss { get; set; }
```

### Örnekler

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
* ad alanı [Aspose.Words](../../font/)
* toplantı [Aspose.Words](../../../)


