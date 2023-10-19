---
title: ShapeBase.HRef
linktitle: HRef
articleTitle: HRef
second_title: Aspose.Words for .NET
description: ShapeBase HRef mülk. Bir şeklin tam köprü adresini alır veya ayarlar C#'da.
type: docs
weight: 230
url: /tr/net/aspose.words.drawing/shapebase/href/
---
## ShapeBase.HRef property

Bir şeklin tam köprü adresini alır veya ayarlar.

```csharp
public string HRef { get; set; }
```

## Notlar

Varsayılan değer boş bir dizedir.

Aşağıda bu özellik için geçerli değer örnekleri verilmiştir:

Tam URI:`https://www.aspose.com/`.

Tam dosya adı:`C:\\Belgelerim\\SalesReport.doc`.

Göreli URI:`../../../resource.txt`

Göreli dosya adı:`..\\Belgelerim\\SalesReport.doc`.

Başka bir belgeye yer işareti koyun:`https://www.aspose.com/Products/Default.aspx#Suites`

Bu belgedeki yer işareti:`#KitapmakAdı`.

## Örnekler

Görüntü içeren ve aynı zamanda köprü olan bir şeklin nasıl ekleneceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertImage(ImageDir + "Logo.jpg");
shape.HRef = "https://forum.aspose.com/";
shape.Target = "New Window";
shape.ScreenTip = "Aspose.Words Support Forums";

// Ctrl + Microsoft Word'deki şekle sol tıklamak yeni bir web tarayıcı penceresi açacaktır
// ve bizi "HRef" özelliğindeki köprüye götür.
doc.Save(ArtifactsDir + "Image.InsertImageWithHyperlink.docx");
```

### Ayrıca bakınız

* class [ShapeBase](../)
* ad alanı [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* toplantı [Aspose.Words](../../../)
