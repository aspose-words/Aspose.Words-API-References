---
title: Font.Engrave
second_title: Aspose.Words for .NET API Referansı
description: Font mülk. Yazı tipi oyulmuş olarak biçimlendirilmişse doğrudur.
type: docs
weight: 120
url: /tr/net/aspose.words/font/engrave/
---
## Font.Engrave property

Yazı tipi oyulmuş olarak biçimlendirilmişse doğrudur.

```csharp
public bool Engrave { get; set; }
```

### Örnekler

Metne gravür/kabartma efektlerinin nasıl uygulanacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Size = 36;
builder.Font.Color = Color.LightBlue;

// Metne 3B benzeri bir efekt uygulamak için gölgeleri kullanmanın iki yolu aşağıdadır.
// 1 - Harfler sayfaya gömülmüş gibi görünmesi için metni kazıyın:
builder.Font.Engrave = true;

builder.Writeln("This text is engraved.");

// 2 - Harflerin sayfadan fırlıyormuş gibi görünmesi için metni kabartma:
builder.Font.Engrave = false;
builder.Font.Emboss = true;

builder.Writeln("This text is embossed.");

doc.Save(ArtifactsDir + "Font.EngraveEmboss.docx");
```

### Ayrıca bakınız

* class [Font](../)
* ad alanı [Aspose.Words](../../font/)
* toplantı [Aspose.Words](../../../)


