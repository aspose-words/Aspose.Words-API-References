---
title: CompositeNode.GetChild
linktitle: GetChild
articleTitle: GetChild
second_title: .NET için Aspose.Words
description: Belirli bir türün N'inci alt düğümünü kolayca almak ve veri yönetimi verimliliğinizi artırmak için CompositeNode GetChild yöntemini keşfedin.
type: docs
weight: 100
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
| index | Int32 | Seçilecek alt düğümün sıfır tabanlı indeksi. Negatif indekslere de izin verilir ve sondan erişimi gösterir, yani -1 son düğüm anlamına gelir. |
| isDeep | Boolean | `doğru` tüm alt düğümlerden yinelemeli olarak seçim yapmak için; `YANLIŞ` sadece yakın çocuklar arasından seçim yapmak. Daha fazla bilgi için açıklamalara bakın. |

### Geri dönüş değeri

Kriterlere uyan alt düğüm veya`hükümsüz` eşleşen bir düğüm bulunamazsa.

## Notlar

Eğer endeks aralık dışındaysa,`hükümsüz` iade edilir.

İşaretleme düğümlerinin (StructuredDocumentTag VeSmartTag ) , şu durumlarda bile geçilir:*isDeep* =`YANLIŞ` Ve`GetChild` işaretleme olmayan düğüm türü için çağrılır. Örneğin, para içindeki ilk çalıştırma bir[`StructuredDocumentTag`](../../../aspose.words.markup/structureddocumenttag/) , yine de iade edilecektir`GetChild`(Run , 0,`YANLIŞ`).

## Örnekler

Bir tablonun stilinin özelliklerinin doğrudan tablonun elemanlarına nasıl uygulanacağını gösterir.

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

// Bu yöntem yukarıda belirlediğimiz gibi tablo stili özellikleriyle ilgilidir.
doc.ExpandTableStylesToDirectFormatting();

doc.Save(ArtifactsDir + "Document.TableStyleToDirectFormatting.docx");
```

Bir bileşik düğümün alt düğüm koleksiyonunda nasıl dolaşılacağını gösterir.

```csharp
Document doc = new Document();

// Bu belgenin ilk paragrafına iki çalışma ve bir şekil alt düğüm olarak ekleyin.
Paragraph paragraph = (Paragraph)doc.GetChild(NodeType.Paragraph, 0, true);
paragraph.AppendChild(new Run(doc, "Hello world! "));

Shape shape = new Shape(doc, ShapeType.Rectangle);
shape.Width = 200;
shape.Height = 200;
// 'CustomNodeId' öğesinin bir çıktı dosyasına kaydedilmediğini ve yalnızca düğümün yaşam süresi boyunca var olduğunu unutmayın.
shape.CustomNodeId = 100;
shape.WrapType = WrapType.Inline;
paragraph.AppendChild(shape);

paragraph.AppendChild(new Run(doc, "Hello again!"));

// Paragrafın hemen altındaki alt öğelerin koleksiyonunda yineleme yapın,
// ve içinde bulduğumuz herhangi bir koşuyu veya şekli yazdırırız.
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
