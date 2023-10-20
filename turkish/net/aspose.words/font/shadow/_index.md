---
title: Font.Shadow
linktitle: Shadow
articleTitle: Shadow
second_title: Aspose.Words for .NET
description: Font Shadow mülk. Yazı tipi gölgeli olarak biçimlendirilmişse doğrudur C#'da.
type: docs
weight: 330
url: /tr/net/aspose.words/font/shadow/
---
## Font.Shadow property

Yazı tipi gölgeli olarak biçimlendirilmişse doğrudur.

```csharp
public bool Shadow { get; set; }
```

## Örnekler

Gölgeyle biçimlendirilmiş bir metin dizisinin nasıl oluşturulacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Gölge bayrağını ofset gölge efekti uygulayacak şekilde ayarlayın,
// harflerin sayfanın üzerinde yüzüyormuş gibi görünmesini sağlıyoruz.
builder.Font.Shadow = true;
builder.Font.Size = 36;

builder.Writeln("This text has a shadow.");

doc.Save(ArtifactsDir + "Font.Shadow.docx");
```

### Ayrıca bakınız

* class [Font](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
