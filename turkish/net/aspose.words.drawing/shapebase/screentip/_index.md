---
title: ShapeBase.ScreenTip
linktitle: ScreenTip
articleTitle: ScreenTip
second_title: .NET için Aspose.Words
description: ShapeBase ScreenTip özelliğini keşfedin, şekillerin üzerine fareyle gelindiğinde görünen ipucu metnini özelleştirerek kullanıcı deneyimini geliştirin.
type: docs
weight: 510
url: /tr/net/aspose.words.drawing/shapebase/screentip/
---
## ShapeBase.ScreenTip property

Fare işaretçisi şeklin üzerine geldiğinde görüntülenen metni tanımlar.

```csharp
public string ScreenTip { get; set; }
```

## Notlar

Varsayılan değer boş bir dizedir.

## Örnekler

Bir resim içeren ve aynı zamanda bir köprü metni olan bir şeklin nasıl ekleneceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertImage(ImageDir + "Logo.jpg");
shape.HRef = "https://forum.aspose.com/";
shape.Target = "New Window";
shape.ScreenTip = "Aspose.Words Support Forums";

// Microsoft Word'de şekle Ctrl + sol tıklamak yeni bir web tarayıcısı penceresi açacaktır
// ve bizi "HRef" özelliğindeki köprü metnine götür.
doc.Save(ArtifactsDir + "Image.InsertImageWithHyperlink.docx");
```

### Ayrıca bakınız

* class [ShapeBase](../)
* ad alanı [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* toplantı [Aspose.Words](../../../)
