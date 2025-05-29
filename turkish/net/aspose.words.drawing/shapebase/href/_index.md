---
title: ShapeBase.HRef
linktitle: HRef
articleTitle: HRef
second_title: .NET için Aspose.Words
description: Şekillerinizin tam köprü adreslerini kolayca yönetmek, tasarımınızın etkileşimini ve işlevselliğini artırmak için ShapeBase HRef özelliğini keşfedin.
type: docs
weight: 250
url: /tr/net/aspose.words.drawing/shapebase/href/
---
## ShapeBase.HRef property

Bir şeklin tam köprü adresini alır veya ayarlar.

```csharp
public string HRef { get; set; }
```

## Notlar

Varsayılan değer boş bir dizedir.

Aşağıda bu özellik için geçerli değerlere dair örnekler verilmiştir:

Tam URI:`https://www.aspose.com/`.

Tam dosya adı:`C:\\Belgelerim\\SatışRaporu.doc`.

Bağıl URI:`../../../kaynak.txt`

Göreceli dosya adı:`..\\Belgelerim\\SatışRaporu.doc`.

Başka bir belge içerisinde yer imi:`https://www.aspose.com/Ürünler/Default.aspx#Suites`

Bu belge içinde yer imi:`#KitapMakerAdı`.

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
