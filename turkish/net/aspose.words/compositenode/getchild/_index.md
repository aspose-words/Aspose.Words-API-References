---
title: CompositeNode.GetChild
linktitle: GetChild
articleTitle: GetChild
second_title: Aspose.Words for .NET
description: CompositeNode GetChild yöntem. Belirtilen türle eşleşen Ninci alt düğümü döndürür C#'da.
type: docs
weight: 80
url: /tr/net/aspose.words/compositenode/getchild/
---
## CompositeNode.GetChild method

Belirtilen türle eşleşen N'inci alt düğümü döndürür.

```csharp
public Node GetChild(NodeType nodeType, int index, bool isDeep)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| nodeType | NodeType | Alt düğümün türünü belirtir. |
| index | Int32 | Seçilecek alt düğümün sıfır tabanlı dizini. Negatif dizinlere de izin verilir ve uçtan erişimi belirtir, yani -1 son düğüm anlamına gelir. |
| isDeep | Boolean | `doğru` tüm alt düğümlerden yinelemeli olarak seçim yapmak için; `YANLIŞ`yalnızca yakın çocuklar arasından seçim yapmak. Daha fazla bilgi için açıklamalara bakın. |

### Geri dönüş değeri

Kriterlerle eşleşen alt düğüm veya`hükümsüz` eşleşen düğüm bulunamazsa.

## Notlar

Dizin aralık dışındaysa,`hükümsüz` Geri döndü.

İşaretleme düğümlerinin (StructuredDocumentTag VeSmartTag ) geçildiğinde bile*isDeep* =`YANLIŞ` Ve`GetChild` biçimlendirme dışı düğüm türü için çağrılır. Örneğin para 'deki ilk çalıştırma bir içine sarılmışsa[`StructuredDocumentTag`](../../../aspose.words.markup/structureddocumenttag/) , yine de iade edilecek`GetChild`(Run 0,`YANLIŞ`).

## Örnekler

Bir tablonun stilinin özelliklerinin doğrudan tablonun öğelerine nasıl uygulanacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Table table = builder.StartTable();
builder.InsertCell();
builder.Write("Hello world!");
builder.EndTable();

TableStyle tableStyle = (TableStyle)doc.Styles.Add(StyleType.Table, "MyTableStyle1");
tableStyle.RowStripe = 3;
tableStyle.CellSpacing = 5;
tableStyle.Shading.BackgroundPatternColor = Color.AntiqueWhite;
tableStyle.Borders.Color = Color.Blue;
tableStyle.Borders.LineStyle = LineStyle.DotDash;

table.Style = tableStyle;

// Bu yöntem yukarıda belirlediğimiz tablo stili özellikleriyle ilgilidir.
doc.ExpandTableStylesToDirectFormatting();

doc.Save(ArtifactsDir + "Document.TableStyleToDirectFormatting.docx");
```

Bileşik bir düğümün alt düğüm koleksiyonunda nasıl geçiş yapılacağını gösterir.

```csharp
Document doc = new Document();

// Bu belgenin ilk paragrafına alt düğümler olarak iki işlem ve bir şekil ekleyin.
Paragraph paragraph = (Paragraph)doc.GetChild(NodeType.Paragraph, 0, true);
paragraph.AppendChild(new Run(doc, "Hello world! "));

Shape shape = new Shape(doc, ShapeType.Rectangle);
shape.Width = 200;
shape.Height = 200;
// 'CustomNodeId'in bir çıktı dosyasına kaydedilmediğini ve yalnızca düğümün ömrü boyunca mevcut olduğunu unutmayın.
shape.CustomNodeId = 100;
shape.WrapType = WrapType.Inline;
paragraph.AppendChild(shape);

paragraph.AppendChild(new Run(doc, "Hello again!"));

// Paragrafın yakın alt öğelerinin toplanması yoluyla yineleme yapın,
// ve içinde bulduğumuz tüm sayıları veya şekilleri yazdırıyoruz.
NodeCollection children = paragraph.GetChildNodes(NodeType.Any, false);

Assert.AreEqual(3, paragraph.GetChildNodes(NodeType.Any, false).Count);

foreach (Node child in children)
    switch (child.NodeType)
    {
        case NodeType.Run:
            Console.WriteLine("Run contents:");
            Console.WriteLine($"\t\"{child.GetText().Trim()}\"");
            break;
        case NodeType.Shape:
            Shape childShape = (Shape)child;
            Console.WriteLine("Shape:");
            Console.WriteLine($"\t{childShape.ShapeType}, {childShape.Width}x{childShape.Height}");
            break;
    }
```

### Ayrıca bakınız

* class [Node](../../node/)
* enum [NodeType](../../nodetype/)
* class [CompositeNode](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
