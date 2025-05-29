---
title: ShapeBase.Target
linktitle: Target
articleTitle: Target
second_title: .NET için Aspose.Words
description: Şekilleriniz için köprü hedef çerçevelerini kolayca ayarlamak veya almak için ShapeBase Target özelliğini keşfedin, böylece kullanıcı gezintisini ve deneyimini geliştirin.
type: docs
weight: 560
url: /tr/net/aspose.words.drawing/shapebase/target/
---
## ShapeBase.Target property

Şekil köprüsü için hedef çerçeveyi alır veya ayarlar.

```csharp
public string Target { get; set; }
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
