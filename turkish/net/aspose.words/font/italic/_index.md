---
title: Font.Italic
second_title: Aspose.Words for .NET API Referansı
description: Font mülk. Yazı tipi italik olarak biçimlendirilmişse doğrudur.
type: docs
weight: 160
url: /tr/net/aspose.words/font/italic/
---
## Font.Italic property

Yazı tipi italik olarak biçimlendirilmişse doğrudur.

```csharp
public bool Italic { get; set; }
```

### Örnekler

Belge oluşturucu kullanarak italik metnin nasıl yazılacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Size = 36;
builder.Font.Italic = true;
builder.Writeln("Hello world!");

doc.Save(ArtifactsDir + "Font.Italic.docx");
```

### Ayrıca bakınız

* class [Font](../)
* ad alanı [Aspose.Words](../../font/)
* toplantı [Aspose.Words](../../../)


