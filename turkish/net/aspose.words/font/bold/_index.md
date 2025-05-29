---
title: Font.Bold
linktitle: Bold
articleTitle: Bold
second_title: .NET için Aspose.Words
description: Font Bold özelliğini keşfedin, metninizin kalın olup olmadığını kolayca belirleyin, web tasarım projeleriniz için okunabilirliği ve stili artırın.
type: docs
weight: 40
url: /tr/net/aspose.words/font/bold/
---
## Font.Bold property

Yazı tipi kalın olarak biçimlendirilmişse doğrudur.

```csharp
public bool Bold { get; set; }
```

## Örnekler

DocumentBuilder kullanılarak biçimlendirilmiş metnin nasıl ekleneceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Yazı tipi biçimlendirmesini belirtin, ardından metni ekleyin.
Aspose.Words.Font font = builder.Font;
font.Size = 16;
font.Bold = true;
font.Color = Color.Blue;
font.Name = "Courier New";
font.Underline = Underline.Dash;

builder.Write("Hello world!");
```

### Ayrıca bakınız

* class [Font](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
