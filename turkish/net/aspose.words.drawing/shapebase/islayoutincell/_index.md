---
title: ShapeBase.IsLayoutInCell
linktitle: IsLayoutInCell
articleTitle: IsLayoutInCell
second_title: .NET için Aspose.Words
description: ShapeBase IsLayoutInCell özelliğini keşfedin, gelişmiş tasarım esnekliği ve iyileştirilmiş düzen yönetimi için tablolardaki şekil yerleşimini kontrol edin.
type: docs
weight: 330
url: /tr/net/aspose.words.drawing/shapebase/islayoutincell/
---
## ShapeBase.IsLayoutInCell property

Şeklin bir tablonun içinde mi yoksa dışında mı görüntüleneceğini belirten bir bayrak alır veya ayarlar.

```csharp
public bool IsLayoutInCell { get; set; }
```

## Notlar

Varsayılan değer:`doğru`.

Sadece en üst düzey şekiller için geçerli olan özellik[`WrapType`](../wraptype/) bunlardan biri value olarak ayarlanmıştır, aksi takdirde[`Inline`](../../../aspose.words/inline/).

## Örnekler

Bir şeklin tablo hücresinde nasıl görüntüleneceğini belirlemeyi gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Table table = builder.StartTable();
builder.InsertCell();
builder.InsertCell();
builder.EndTable();

TableStyle tableStyle = (TableStyle)doc.Styles.Add(StyleType.Table, "MyTableStyle1");
tableStyle.BottomPadding = 20;
tableStyle.LeftPadding = 10;
tableStyle.RightPadding = 10;
tableStyle.TopPadding = 20;
tableStyle.Borders.Color = Color.Black;
tableStyle.Borders.LineStyle = LineStyle.Single;

table.Style = tableStyle;

builder.MoveTo(table.FirstRow.FirstCell.FirstParagraph);

Shape shape = builder.InsertShape(ShapeType.Rectangle, RelativeHorizontalPosition.LeftMargin, 50,
    RelativeVerticalPosition.TopMargin, 100, 100, 100, WrapType.None);

// Şekli hücrenin paragrafı içerisinde satır içi bir öğe olarak görüntülemek için "IsLayoutInCell" özelliğini "true" olarak ayarlayın.
// Şeklin yerini belirleyecek koordinat başlangıcı, şeklin hücresinin sol üst köşesi olacaktır.
// Hücreyi yeniden boyutlandırdığımızda şekil, hücrenin sol üst köşesinden başlayarak aynı pozisyonu koruyarak hareket edecektir.
// Şekli bağımsız bir yüzen şekil olarak görüntülemek için "IsLayoutInCell" özelliğini "false" olarak ayarlayın.
// Şeklin yerini belirleyecek koordinat başlangıcı sayfanın sol üst köşesi olacak,
// ve şekil hücresinin yeniden boyutlandırılmasına yanıt vermeyecektir.
shape.IsLayoutInCell = isLayoutInCell;

// "IsLayoutInCell" özelliğini yalnızca yüzen şekillere uygulayabiliriz.
shape.WrapType = WrapType.None;

doc.Save(ArtifactsDir + "Shape.LayoutInTableCell.docx");
```

### Ayrıca bakınız

* class [ShapeBase](../)
* ad alanı [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* toplantı [Aspose.Words](../../../)
