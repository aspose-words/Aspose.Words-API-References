---
title: ShapeBase.IsLayoutInCell
second_title: Aspose.Words for .NET API Referansı
description: ShapeBase mülk. Şeklin bir tablonun içinde mi yoksa dışında mı görüntülendiğini belirten bir bayrak alır veya ayarlar.
type: docs
weight: 300
url: /tr/net/aspose.words.drawing/shapebase/islayoutincell/
---
## ShapeBase.IsLayoutInCell property

Şeklin bir tablonun içinde mi yoksa dışında mı görüntülendiğini belirten bir bayrak alır veya ayarlar.

```csharp
public bool IsLayoutInCell { get; set; }
```

### Notlar

Varsayılan değer **doğru**.

Yalnızca üst düzey şekiller için etkilidir, özellik[`WrapType`](../wraptype/) bunun dışında value olarak ayarlanan[`Inline`](../../../aspose.words/inline/).

### Örnekler

Tablo hücresinde bir şeklin nasıl görüntüleneceğini belirlemeyi gösterir.

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

// Şekli hücrenin paragrafında satır içi bir öğe olarak görüntülemek için "IsLayoutInCell" özelliğini "true" olarak ayarlayın.
// Şeklin konumunu belirleyecek olan koordinat orijini, şeklin hücresinin sol üst köşesi olacaktır.
// Hücreyi yeniden boyutlandırırsak, şekil hücrenin sol üst köşesinden başlayarak aynı konumu koruyacak şekilde hareket edecektir.
// Şekli bağımsız bir kayan şekil olarak görüntülemek için "IsLayoutInCell" özelliğini "false" olarak ayarlayın.
// Şeklin konumunu belirleyecek olan koordinat orijini sayfanın sol üst köşesi olacak,
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


