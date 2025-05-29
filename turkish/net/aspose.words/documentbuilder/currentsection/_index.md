---
title: DocumentBuilder.CurrentSection
linktitle: CurrentSection
articleTitle: CurrentSection
second_title: .NET için Aspose.Words
description: Belgenizdeki seçili bölüme kolayca erişmek ve yönetmek için DocumentBuilder CurrentSection özelliğini keşfedin; böylece düzenleme deneyiminizi geliştirin.
type: docs
weight: 60
url: /tr/net/aspose.words/documentbuilder/currentsection/
---
## DocumentBuilder.CurrentSection property

Bu bölümde şu anda seçili olan bölümü alır[`DocumentBuilder`](../) .

```csharp
public Section CurrentSection { get; }
```

## Örnekler

Kayan bir resmin nasıl ekleneceğini, konumunun ve boyutunun nasıl belirleneceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertImage(ImageDir + "Logo.jpg");
shape.WrapType = WrapType.None;

// Şeklin "RelativeHorizontalPosition" özelliğini "Left" özelliğinin değerini işleyecek şekilde yapılandırın
 // şeklin sayfanın sol tarafından yatay uzaklığı, nokta cinsinden.
shape.RelativeHorizontalPosition = RelativeHorizontalPosition.Page;

// Şeklin sayfanın sol tarafından yatay uzaklığını 100 olarak ayarlayın.
shape.Left = 100;

// Şekli sayfanın üstünden 80pt aşağıya yerleştirmek için benzer şekilde "RelativeVerticalPosition" özelliğini kullanın.
shape.RelativeVerticalPosition = RelativeVerticalPosition.Page;
shape.Top = 80;

// Şeklin yüksekliğini ayarlayın, bu sayede boyutlar korunarak genişlik otomatik olarak ölçeklenir.
shape.Height = 125;

Assert.AreEqual(125.0d, shape.Width);

// "Alt" ve "Sağ" özellikleri, görüntünün alt ve sağ kenarlarını içerir.
Assert.AreEqual(shape.Top + shape.Height, shape.Bottom);
Assert.AreEqual(shape.Left + shape.Width, shape.Right);

doc.Save(ArtifactsDir + "Image.CreateFloatingPositionSize.docx");
```

### Ayrıca bakınız

* class [Section](../../section/)
* class [DocumentBuilder](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
