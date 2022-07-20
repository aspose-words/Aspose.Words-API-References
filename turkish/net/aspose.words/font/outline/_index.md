---
title: Outline
second_title: Aspose.Words for .NET API Referansı
description: Yazı tipi anahat olarak biçimlendirilmişse doğrudur.
type: docs
weight: 290
url: /tr/net/aspose.words/font/outline/
---
## Font.Outline property

Yazı tipi anahat olarak biçimlendirilmişse doğrudur.

```csharp
public bool Outline { get; set; }
```

### Örnekler

Anahat olarak biçimlendirilmiş bir metin dizisinin nasıl oluşturulacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Metnin dolgu rengini beyaz olarak değiştirmek için Anahat bayrağını ayarlayın ve
 // metnin orijinal renginde her karakterin etrafına ince bir çerçeve bırakın.
builder.Font.Outline = true;
builder.Font.Color = Color.Blue;
builder.Font.Size = 36;

builder.Writeln("This text has an outline.");

doc.Save(ArtifactsDir + "Font.Outline.docx");
```

### Ayrıca bakınız

* class [Font](../../font)
* ad alanı [Aspose.Words](../../font)
* toplantı [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->