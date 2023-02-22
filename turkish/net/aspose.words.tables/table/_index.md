---
title: Class Table
second_title: Aspose.Words for .NET API Referansı
description: Aspose.Words.Tables.Table sınıf. Word belgesindeki bir tabloyu temsil eder.
type: docs
weight: 6040
url: /tr/net/aspose.words.tables/table/
---
## Table class

Word belgesindeki bir tabloyu temsil eder.

```csharp
public class Table : CompositeNode
```

## yapıcılar

| İsim | Tanım |
| --- | --- |
| [Table](table/)(DocumentBase) | Yeni bir örneğini başlatır **Masa** sınıf. |

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [AbsoluteHorizontalDistance](../../aspose.words.tables/table/absolutehorizontaldistance/) { get; set; } | Tablo özellikleri tarafından noktalar olarak belirtilen mutlak yatay kayan tablo konumunu alır veya ayarlar. Varsayılan değer 0. |
| [AbsoluteVerticalDistance](../../aspose.words.tables/table/absoluteverticaldistance/) { get; set; } | Tablo özellikleri tarafından noktalar olarak belirtilen mutlak dikey kayan tablo konumunu alır veya ayarlar. Varsayılan değer 0. |
| [Alignment](../../aspose.words.tables/table/alignment/) { get; set; } | Bir satır içi tablonun belgede nasıl hizalanacağını belirtir. |
| [AllowAutoFit](../../aspose.words.tables/table/allowautofit/) { get; set; } | Microsoft Word ve Aspose.Words'ün tablodaki hücreleri içeriklerine uyacak şekilde otomatik olarak yeniden boyutlandırmasını sağlar. |
| [AllowCellSpacing](../../aspose.words.tables/table/allowcellspacing/) { get; set; } | "Hücreler arasında boşluk bırakmaya izin ver" seçeneğini alır veya ayarlar. |
| [AllowOverlap](../../aspose.words.tables/table/allowoverlap/) { get; } | Bir kayan tablonun, görüntülendiğinde belgesindeki diğer kayan nesnelerin uzantılarıyla çakışmasına izin verip vermeyeceğini alır. Varsayılan değer`doğru` . |
| [Bidi](../../aspose.words.tables/table/bidi/) { get; set; } | Bunun sağdan sola bir tablo olup olmadığını alır veya ayarlar. |
| [BottomPadding](../../aspose.words.tables/table/bottompadding/) { get; set; } | Hücre içeriğinin altına eklenecek boşluk miktarını (puan olarak) alır veya ayarlar. |
| [CellSpacing](../../aspose.words.tables/table/cellspacing/) { get; set; } | Hücreler arasındaki boşluk miktarını (nokta olarak) alır veya ayarlar. |
| [ChildNodes](../../aspose.words/compositenode/childnodes/) { get; } | Bu düğümün tüm acil alt düğümlerini alır. |
| [Count](../../aspose.words/compositenode/count/) { get; } | Bu düğümün acil alt öğelerinin sayısını alır. |
| [CustomNodeId](../../aspose.words/node/customnodeid/) { get; set; } | Özel düğüm tanımlayıcısını belirtir. |
| [Description](../../aspose.words.tables/table/description/) { get; set; } | Bu tablonun açıklamasını alır veya ayarlar. Tabloda yer alan bilgilerin alternatif bir metin gösterimini sağlar. |
| [DistanceBottom](../../aspose.words.tables/table/distancebottom/) { get; } | Tablo altı ile çevresindeki metin arasındaki mesafeyi nokta cinsinden alır. |
| [DistanceLeft](../../aspose.words.tables/table/distanceleft/) { get; } | Soldaki tablo ile çevresindeki metin arasındaki mesafeyi puan cinsinden alır. |
| [DistanceRight](../../aspose.words.tables/table/distanceright/) { get; } | Sağdaki tablo ile çevresindeki metin arasındaki mesafeyi nokta cinsinden alır. |
| [DistanceTop](../../aspose.words.tables/table/distancetop/) { get; } | Masa üstü ile çevresindeki metin arasındaki mesafeyi nokta cinsinden alır. |
| virtual [Document](../../aspose.words/node/document/) { get; } | Bu düğümün ait olduğu belgeyi alır. |
| [FirstChild](../../aspose.words/compositenode/firstchild/) { get; } | Düğümün ilk alt öğesini alır. |
| [FirstRow](../../aspose.words.tables/table/firstrow/) { get; } | İlkini döndürür **Sıra** tablodaki düğüm. |
| [HasChildNodes](../../aspose.words/compositenode/haschildnodes/) { get; } | Bu düğümün herhangi bir alt düğümü varsa doğru döndürür. |
| [HorizontalAnchor](../../aspose.words.tables/table/horizontalanchor/) { get; set; } | Kayan tablonun yatay konumunun hesaplanması gereken temel nesneyi alır. Varsayılan değerColumn . |
| override [IsComposite](../../aspose.words/compositenode/iscomposite/) { get; } | Bu düğümün alt düğümleri olabileceğinden true değerini döndürür. |
| [LastChild](../../aspose.words/compositenode/lastchild/) { get; } | Düğümün son alt öğesini alır. |
| [LastRow](../../aspose.words.tables/table/lastrow/) { get; } | Sonuncuyu döndürür **Sıra** tablodaki düğüm. |
| [LeftIndent](../../aspose.words.tables/table/leftindent/) { get; set; } | Tablonun sol girintisini temsil eden değeri alır veya ayarlar. |
| [LeftPadding](../../aspose.words.tables/table/leftpadding/) { get; set; } | Hücre içeriğinin soluna eklenecek boşluk miktarını (puan olarak) alır veya ayarlar. |
| [NextSibling](../../aspose.words/node/nextsibling/) { get; } | Bu düğümden hemen sonraki düğümü alır. |
| override [NodeType](../../aspose.words.tables/table/nodetype/) { get; } | İade **DüğümTürü.Tablo** . |
| [ParentNode](../../aspose.words/node/parentnode/) { get; } | Bu düğümün hemen üst öğesini alır. |
| [PreferredWidth](../../aspose.words.tables/table/preferredwidth/) { get; set; } | Tablonun tercih edilen genişliğini alır veya ayarlar. |
| [PreviousSibling](../../aspose.words/node/previoussibling/) { get; } | Bu düğümden hemen önceki düğümü alır. |
| [Range](../../aspose.words/node/range/) { get; } | Bir döndürür **Menzil** belgenin bu düğümde bulunan bölümünü temsil eden nesne. |
| [RelativeHorizontalAlignment](../../aspose.words.tables/table/relativehorizontalalignment/) { get; set; } | Kayan tablo göreli yatay hizalamayı alır veya ayarlar. |
| [RelativeVerticalAlignment](../../aspose.words.tables/table/relativeverticalalignment/) { get; set; } | Kayan tablo göreli dikey hizalamayı alır veya ayarlar. |
| [RightPadding](../../aspose.words.tables/table/rightpadding/) { get; set; } | Hücre içeriğinin sağına eklenecek boşluk miktarını (puan olarak) alır veya ayarlar. |
| [Rows](../../aspose.words.tables/table/rows/) { get; } | Tablonun satırlarına yazılı erişim sağlar. |
| [Style](../../aspose.words.tables/table/style/) { get; set; } | Bu tabloya uygulanan tablo stilini alır veya ayarlar. |
| [StyleIdentifier](../../aspose.words.tables/table/styleidentifier/) { get; set; } | Bu tabloya uygulanan tablo stilinin yerel ayardan bağımsız stil tanımlayıcısını alır veya ayarlar. |
| [StyleName](../../aspose.words.tables/table/stylename/) { get; set; } | Bu tabloya uygulanan tablo stilinin adını alır veya ayarlar. |
| [StyleOptions](../../aspose.words.tables/table/styleoptions/) { get; set; } | Bu tabloya bir tablo stilinin nasıl uygulanacağını belirten bit bayraklarını alır veya ayarlar. |
| [TextWrapping](../../aspose.words.tables/table/textwrapping/) { get; set; } | Alır veya ayarlar[`TextWrapping`](./textwrapping/) tablo için. |
| [Title](../../aspose.words.tables/table/title/) { get; set; } | Bu tablonun başlığını alır veya ayarlar. Tabloda yer alan bilgilerin alternatif bir metin gösterimini sağlar. |
| [TopPadding](../../aspose.words.tables/table/toppadding/) { get; set; } | Hücre içeriğinin üzerine eklenecek boşluk miktarını (puan olarak) alır veya ayarlar. |
| [VerticalAnchor](../../aspose.words.tables/table/verticalanchor/) { get; set; } | Kayan tablonun dikey konumunun hesaplanması gereken temel nesneyi alır. Varsayılan değerMargin . |

## yöntemler

| İsim | Tanım |
| --- | --- |
| override [Accept](../../aspose.words.tables/table/accept/)(DocumentVisitor) | Bir ziyaretçiyi kabul eder. |
| [AppendChild](../../aspose.words/compositenode/appendchild/)(Node) | Belirtilen düğümü, bu düğüm için alt düğümler listesinin sonuna ekler. |
| [AutoFit](../../aspose.words.tables/table/autofit/)(AutoFitBehavior) | Belirtilen otomatik sığdırma davranışına göre tabloyu ve hücreleri yeniden boyutlandırır. |
| [ClearBorders](../../aspose.words.tables/table/clearborders/)() | Bu tablodaki tüm tablo ve hücre kenarlıklarını kaldırır. |
| [ClearShading](../../aspose.words.tables/table/clearshading/)() | Tablodaki tüm gölgelemeleri kaldırır. |
| [Clone](../../aspose.words/node/clone/)(bool) | Düğümün bir kopyasını oluşturur. |
| [ConvertToHorizontallyMergedCells](../../aspose.words.tables/table/converttohorizontallymergedcells/)() | Genişliğe göre yatay olarak birleştirilmiş hücreleri, genişliklerine göre birleştirilmiş hücrelere dönüştürür.[`HorizontalMerge`](../cellformat/horizontalmerge/) . |
| [CreateNavigator](../../aspose.words/compositenode/createnavigator/)() | Sistem kullanımı için ayrılmıştır. IXPathNavigable. |
| [EnsureMinimum](../../aspose.words.tables/table/ensureminimum/)() | Tabloda satır yoksa, bir satır oluşturur ve ekler **Sıra** . |
| [GetAncestor](../../aspose.words/node/getancestor/)(NodeType) | Belirtilenin ilk atasını alır[`NodeType`](../../aspose.words/nodetype/) . |
| [GetAncestor](../../aspose.words/node/getancestor/)(Type) | Belirtilen nesne türünün ilk üst öğesini alır. |
| [GetChild](../../aspose.words/compositenode/getchild/)(NodeType, int, bool) | Belirtilen türle eşleşen N. alt düğümü döndürür. |
| [GetChildNodes](../../aspose.words/compositenode/getchildnodes/)(NodeType, bool) | Belirtilen türle eşleşen canlı bir alt düğüm koleksiyonu döndürür. |
| [GetEnumerator](../../aspose.words/compositenode/getenumerator/)() | Bu düğümün alt düğümleri üzerinde her stil yinelemesi için destek sağlar. |
| override [GetText](../../aspose.words/compositenode/gettext/)() | Bu düğümün ve tüm alt öğelerinin metnini alır. |
| [IndexOf](../../aspose.words/compositenode/indexof/)(Node) | Alt düğüm dizisindeki belirtilen alt düğümün dizinini döndürür. |
| [InsertAfter](../../aspose.words/compositenode/insertafter/)(Node, Node) | Belirtilen referans düğümünden hemen sonra belirtilen düğümü ekler. |
| [InsertBefore](../../aspose.words/compositenode/insertbefore/)(Node, Node) | Belirtilen düğümü, belirtilen referans düğümünden hemen önce ekler. |
| [NextPreOrder](../../aspose.words/node/nextpreorder/)(Node) | Ön sipariş ağaç geçiş algoritmasına göre sonraki düğümü alır. |
| [PrependChild](../../aspose.words/compositenode/prependchild/)(Node) | Belirtilen düğümü, bu düğüm için alt düğümler listesinin başına ekler. |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder/)(Node) | Ön sipariş ağacı geçiş algoritmasına göre önceki düğümü alır. |
| [Remove](../../aspose.words/node/remove/)() | Kendini üst öğeden kaldırır. |
| [RemoveAllChildren](../../aspose.words/compositenode/removeallchildren/)() | Geçerli düğümün tüm alt düğümlerini kaldırır. |
| [RemoveChild](../../aspose.words/compositenode/removechild/)(Node) | Belirtilen alt düğümü kaldırır. |
| [RemoveSmartTags](../../aspose.words/compositenode/removesmarttags/)() | Tümünü kaldırır[`SmartTag`](../../aspose.words.markup/smarttag/) geçerli düğümün alt düğümleri. |
| [SelectNodes](../../aspose.words/compositenode/selectnodes/)(string) | XPath ifadesiyle eşleşen düğümlerin listesini seçer. |
| [SelectSingleNode](../../aspose.words/compositenode/selectsinglenode/)(string) | XPath ifadesiyle eşleşen ilk Düğümü seçer. |
| [SetBorder](../../aspose.words.tables/table/setborder/)(BorderType, LineStyle, double, Color, bool) | Belirtilen tablo kenarlığını belirtilen çizgi stili, genişlik ve renge ayarlar. |
| [SetBorders](../../aspose.words.tables/table/setborders/)(LineStyle, double, Color) | Tüm tablo kenarlıklarını belirtilen çizgi stili, genişlik ve renge ayarlar. |
| [SetShading](../../aspose.words.tables/table/setshading/)(TextureIndex, Color, Color) | Tüm tablo üzerinde belirtilen değerlere gölgeleme ayarlar. |
| [ToString](../../aspose.words/node/tostring/)(SaveFormat) | Düğümün içeriğini belirtilen biçimde bir dizeye aktarır. |
| [ToString](../../aspose.words/node/tostring/)(SaveOptions) | Belirtilen kaydetme seçeneklerini kullanarak düğümün içeriğini bir dizeye aktarır. |

### Notlar

**Masa**blok düzeyinde bir düğümdür ve türetilen sınıfların çocuğu olabilir **Hikaye** or  **satır içi hikaye**.

**Masa** bir veya daha fazlasını içerebilir **Sıra** düğümler.

Minimum geçerli bir tablonun en az bir tane olması gerekir **Sıra**.

### Örnekler

Bir tablonun nasıl oluşturulacağını gösterir.

```csharp
Document doc = new Document();
Table table = new Table(doc);
doc.FirstSection.Body.AppendChild(table);

// Tablolar, paragraflar içerebilen hücreler içeren satırlar içerir
// koşular, şekiller ve hatta diğer tablolar gibi tipik öğelerle.
// Bir tabloda "EnsureMinimum" yöntemini çağırmak,
// tabloda en az bir satır, hücre ve paragraf var.
Row firstRow = new Row(doc);
table.AppendChild(firstRow);

Cell firstCell = new Cell(doc);
firstRow.AppendChild(firstCell);

Paragraph paragraph = new Paragraph(doc);
firstCell.AppendChild(paragraph);

// Tablonun ilk satırındaki ilk aramaya metin ekleyin.
Run run = new Run(doc, "Hello world!");
paragraph.AppendChild(run);

doc.Save(ArtifactsDir + "Table.CreateTable.docx");
```

Belgedeki tüm tabloların nasıl yineleneceğini ve her hücrenin içeriğinin nasıl yazdırılacağını gösterir.

```csharp
Document doc = new Document(MyDir + "Tables.docx");
TableCollection tables = doc.FirstSection.Body.Tables;

Assert.AreEqual(2, tables.ToArray().Length);

for (int i = 0; i < tables.Count; i++)
{
    Console.WriteLine($"Start of Table {i}");

    RowCollection rows = tables[i].Rows;

    // Bir diziye klonlamak için bir satır koleksiyonunda "ToArray" yöntemini kullanabiliriz.
    Assert.AreEqual(rows, rows.ToArray());
    Assert.AreNotSame(rows, rows.ToArray());

    for (int j = 0; j < rows.Count; j++)
    {
        Console.WriteLine($"\tStart of Row {j}");

        CellCollection cells = rows[j].Cells;

        // Bir hücre koleksiyonunu bir diziye klonlamak için "ToArray" yöntemini kullanabiliriz.
        Assert.AreEqual(cells, cells.ToArray());
        Assert.AreNotSame(cells, cells.ToArray());

        for (int k = 0; k < cells.Count; k++)
        {
            string cellText = cells[k].ToString(SaveFormat.Text).Trim();
            Console.WriteLine($"\t\tContents of Cell:{k} = \"{cellText}\"");
        }

        Console.WriteLine($"\tEnd of Row {j}");
    }

    Console.WriteLine($"End of Table {i}\n");
}
```

Biçimlendirilmiş bir 2x2 tablonun nasıl oluşturulacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Table table = builder.StartTable();
builder.InsertCell();
builder.CellFormat.VerticalAlignment = CellVerticalAlignment.Center;
builder.Write("Row 1, cell 1.");
builder.InsertCell();
builder.Write("Row 1, cell 2.");
builder.EndRow();

// Tabloyu oluştururken, belge oluşturucu mevcut RowFormat/CellFormat özellik değerlerini uygulayacaktır
// imlecinin içinde bulunduğu geçerli satıra/hücreye ve bunları oluştururken yeni satırlara/hücrelere.
Assert.AreEqual(CellVerticalAlignment.Center, table.Rows[0].Cells[0].CellFormat.VerticalAlignment);
Assert.AreEqual(CellVerticalAlignment.Center, table.Rows[0].Cells[1].CellFormat.VerticalAlignment);

builder.InsertCell();
builder.RowFormat.Height = 100;
builder.RowFormat.HeightRule = HeightRule.Exactly;
builder.CellFormat.Orientation = TextOrientation.Upward;
builder.Write("Row 2, cell 1.");
builder.InsertCell();
builder.CellFormat.Orientation = TextOrientation.Downward;
builder.Write("Row 2, cell 2.");
builder.EndRow();
builder.EndTable();

// Önceden eklenen satırlar ve hücreler, oluşturucunun biçimlendirmesindeki değişikliklerden geriye dönük olarak etkilenmez.
Assert.AreEqual(0, table.Rows[0].RowFormat.Height);
Assert.AreEqual(HeightRule.Auto, table.Rows[0].RowFormat.HeightRule);
Assert.AreEqual(100, table.Rows[1].RowFormat.Height);
Assert.AreEqual(HeightRule.Exactly, table.Rows[1].RowFormat.HeightRule);
Assert.AreEqual(TextOrientation.Upward, table.Rows[1].Cells[0].CellFormat.Orientation);
Assert.AreEqual(TextOrientation.Downward, table.Rows[1].Cells[1].CellFormat.Orientation);

doc.Save(ArtifactsDir + "DocumentBuilder.BuildTable.docx");
```

Belge oluşturucu kullanmadan iç içe tablonun nasıl oluşturulacağını gösterir.

```csharp
public void CreateNestedTable()
{
    Document doc = new Document();

    // Üç satır ve dört sütunlu dış tabloyu oluşturun ve ardından belgeye ekleyin.
    Table outerTable = CreateTable(doc, 3, 4, "Outer Table");
    doc.FirstSection.Body.AppendChild(outerTable);

    // İki satır ve iki sütun içeren başka bir tablo oluşturun ve ardından bunu ilk tablonun ilk hücresine ekleyin.
    Table innerTable = CreateTable(doc, 2, 2, "Inner Table");
    outerTable.FirstRow.FirstCell.AppendChild(innerTable);

    doc.Save(ArtifactsDir + "Table.CreateNestedTable.docx");
}

/// <summary>
/// Her hücrede verilen boyutlar ve metin ile belgede yeni bir tablo oluşturur.
/// </summary>
private static Table CreateTable(Document doc, int rowCount, int cellCount, string cellText)
{
    Table table = new Table(doc);

    for (int rowId = 1; rowId <= rowCount; rowId++)
    {
        Row row = new Row(doc);
        table.AppendChild(row);

        for (int cellId = 1; cellId <= cellCount; cellId++)
        {
            Cell cell = new Cell(doc);
            cell.AppendChild(new Paragraph(doc));
            cell.FirstParagraph.AppendChild(new Run(doc, cellText));

            row.AppendChild(cell);
        }
    }

    // Tablonuza sırasıyla başlık ve açıklama eklemek için "Title" ve "Description" özelliklerini kullanabilirsiniz.
    // Bu özellikleri kullanabilmemiz için tablonun en az bir satırı olmalıdır.
    // Bu özellikler, ISO/IEC 29500 uyumlu .docx belgeleri için anlamlıdır (bkz. OoxmlCompliance sınıfı).
    // Belgeyi ISO/IEC 29500 öncesi formatlarda kaydedersek, Microsoft Word bu özellikleri yok sayar.
    table.Title = "Aspose table title";
    table.Description = "Aspose table description";

    return table;
}
```

### Ayrıca bakınız

* class [CompositeNode](../../aspose.words/compositenode/)
* ad alanı [Aspose.Words.Tables](../../aspose.words.tables/)
* toplantı [Aspose.Words](../../)


