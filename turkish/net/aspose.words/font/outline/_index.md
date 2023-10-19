---
title: Font.Outline
linktitle: Outline
articleTitle: Outline
second_title: Aspose.Words for .NET
description: Font Outline mülk. Yazı tipi anahat olarak biçimlendirilmişse doğrudur C#'da.
type: docs
weight: 290
url: /tr/net/aspose.words/font/outline/
---
## Font.Outline property

Yazı tipi anahat olarak biçimlendirilmişse doğrudur.

```csharp
public bool Outline { get; set; }
```

## Örnekler

Anahat olarak biçimlendirilmiş bir metin dizisinin nasıl oluşturulacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Metnin dolgu rengini beyaza değiştirmek için Anahat bayrağını ayarlayın ve
 // her karakterin etrafına metnin orijinal renginde ince bir çerçeve bırakın.
builder.Font.Outline = true;
builder.Font.Color = Color.Blue;
builder.Font.Size = 36;

builder.Writeln("This text has an outline.");

doc.Save(ArtifactsDir + "Font.Outline.docx");
```

### Ayrıca bakınız

* class [Font](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
