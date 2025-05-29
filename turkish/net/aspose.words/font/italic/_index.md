---
title: Font.Italic
linktitle: Italic
articleTitle: Italic
second_title: .NET için Aspose.Words
description: Font Italic özelliğini keşfedin! Tasarımlarınızda okunabilirliği ve stili geliştirmek için metni kolayca italik olarak biçimlendirin. Tipografinizi bugün güçlendirin!
type: docs
weight: 160
url: /tr/net/aspose.words/font/italic/
---
## Font.Italic property

Yazı tipi italik olarak biçimlendirilmişse doğrudur.

```csharp
public bool Italic { get; set; }
```

## Örnekler

Belge oluşturucuyu kullanarak italik metin yazmanın nasıl yapılacağını gösterir.

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
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
