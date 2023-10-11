---
title: ShapeBase.IsLayoutInCell
second_title: Aspose.Words for .NET API Referansı
description: ShapeBase mülk. Şeklin tablonun içinde mi yoksa dışında mı görüntüleneceğini belirten bir bayrak alır veya ayarlar.
type: docs
weight: 310
url: /tr/net/aspose.words.drawing/shapebase/islayoutincell/
---
## ShapeBase.IsLayoutInCell property

Şeklin tablonun içinde mi yoksa dışında mı görüntüleneceğini belirten bir bayrak alır veya ayarlar.

```csharp
public bool IsLayoutInCell { get; set; }
```

### Notlar

Varsayılan değer:`doğru`.

Yalnızca üst düzey şekillere etki eder; özellik[`WrapType`](../wraptype/) bunlardan biri, dışında value olarak ayarlanmış[`Inline`](../../../aspose.words/inline/).

### Örnekler

Tablo hücresinde bir şeklin nasıl görüntüleneceğinin nasıl belirleneceğini gösterir.

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

// Şekli hücrenin paragrafının içinde satır içi öğe olarak görüntülemek için "IsLayoutInCell" özelliğini "true" olarak ayarlayın.
// Şeklin konumunu belirleyecek koordinat orijini, şeklin hücresinin sol üst köşesi olacaktır.
// Hücreyi yeniden boyutlandırırsak şekil, hücrenin sol üst köşesinden başlayarak aynı konumu koruyacak şekilde hareket edecektir.
// Şekli bağımsız bir kayan şekil olarak görüntülemek için "IsLayoutInCell" özelliğini "false" olarak ayarlayın.
// Şeklin konumunu belirleyecek koordinat orijini sayfanın sol üst köşesi olacaktır,
// ve şekil, hücresinin yeniden boyutlandırılmasına yanıt vermeyecektir.
shape.IsLayoutInCell = isLayoutInCell;

// "IsLayoutInCell" özelliğini yalnızca kayan şekillere uygulayabiliriz.
shape.WrapType = WrapType.None;

doc.Save(ArtifactsDir + "Shape.LayoutInTableCell.docx");
```

### Ayrıca bakınız

* class [ShapeBase](../)
* ad alanı [Aspose.Words.Drawing](../../shapebase/)
* toplantı [Aspose.Words](../../../)


