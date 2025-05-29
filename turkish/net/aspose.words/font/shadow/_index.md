---
title: Font.Shadow
linktitle: Shadow
articleTitle: Shadow
second_title: .NET için Aspose.Words
description: Font Shadow özelliğini keşfedin, tasarımlarınızda çarpıcı bir görsel çekicilik için metninizi şık gölge efektleriyle zenginleştirin.
type: docs
weight: 340
url: /tr/net/aspose.words/font/shadow/
---
## Font.Shadow property

Yazı tipi gölgeli olarak biçimlendirilmişse doğrudur.

```csharp
public bool Shadow { get; set; }
```

## Örnekler

Gölgeli bir metin dizisinin nasıl oluşturulacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Gölge bayrağını ayarlayarak gölge efektini ofsetleyin.
// harflerin sayfanın üstünde yüzüyormuş gibi görünmesini sağlar.
builder.Font.Shadow = true;
builder.Font.Size = 36;

builder.Writeln("This text has a shadow.");

doc.Save(ArtifactsDir + "Font.Shadow.docx");
```

### Ayrıca bakınız

* class [Font](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
