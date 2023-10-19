---
title: DocumentBuilder.CurrentSection
linktitle: CurrentSection
articleTitle: CurrentSection
second_title: Aspose.Words for .NET
description: DocumentBuilder CurrentSection mülk. Bu bölümde o anda seçili olan bölümü döndürürDocumentBuilder  C#'da.
type: docs
weight: 60
url: /tr/net/aspose.words/documentbuilder/currentsection/
---
## DocumentBuilder.CurrentSection property

Bu bölümde o anda seçili olan bölümü döndürür[`DocumentBuilder`](../) .

```csharp
public Section CurrentSection { get; }
```

## Örnekler

Kayan bir görüntünün nasıl ekleneceğini ve konumunun ve boyutunun nasıl belirleneceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertImage(ImageDir + "Logo.jpg");
shape.WrapType = WrapType.None;

// "Left" özelliğinin değerini işlemek için şeklin "RelativeHorizontalPosition" özelliğini yapılandırın
 // şeklin sayfanın sol tarafına nokta cinsinden yatay uzaklığı olarak.
shape.RelativeHorizontalPosition = RelativeHorizontalPosition.Page;

// Şeklin sayfanın sol tarafından yatay uzaklığını 100 olarak ayarlayın.
shape.Left = 100;

// Şekli sayfanın üst kısmının 80pt altına konumlandırmak için "RelativeVerticalPosition" özelliğini benzer şekilde kullanın.
shape.RelativeVerticalPosition = RelativeVerticalPosition.Page;
shape.Top = 80;

// Boyutu korumak için genişliği otomatik olarak ölçeklendirecek şekilde şeklin yüksekliğini ayarlayın.
shape.Height = 125;

Assert.AreEqual(125.0d, shape.Width);

// "Bottom" ve "Right" özellikleri görüntünün alt ve sağ kenarlarını içerir.
Assert.AreEqual(shape.Top + shape.Height, shape.Bottom);
Assert.AreEqual(shape.Left + shape.Width, shape.Right);

doc.Save(ArtifactsDir + "Image.CreateFloatingPositionSize.docx");
```

### Ayrıca bakınız

* class [Section](../../section/)
* class [DocumentBuilder](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
