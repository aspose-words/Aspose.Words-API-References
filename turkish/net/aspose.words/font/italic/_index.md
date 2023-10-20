---
title: Font.Italic
linktitle: Italic
articleTitle: Italic
second_title: Aspose.Words for .NET
description: Font Italic mülk. Yazı tipi italik olarak biçimlendirilmişse doğrudur C#'da.
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

Bir belge oluşturucu kullanılarak italik metnin nasıl yazılacağını gösterir.

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
