---
title: Table Class
linktitle: Table
articleTitle: Table
second_title: .NET için Aspose.Words
description: Word belgelerinde tabloları kolayca oluşturmak ve yönetmek, belgenizin düzenini ve işlevselliğini geliştirmek için Aspose.Words.Tables.Table sınıfını keşfedin.
type: docs
weight: 7190
url: /tr/net/aspose.words.tables/table/
---
## Table class

Word belgesindeki bir tabloyu temsil eder.

Daha fazla bilgi edinmek için şu adresi ziyaret edin:[Tablolarla Çalışma](https://docs.aspose.com/words/net/working-with-tables/) belgeleme makalesi.

```csharp
public class Table : CompositeNode
```

## yapıcılar

| İsim | Tanım |
| --- | --- |
| [Table](table/)(*[DocumentBase](../../aspose.words/documentbase/)*) | Yeni bir örneğini başlatır`Table` sınıf. |

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [AbsoluteHorizontalDistance](../../aspose.words.tables/table/absolutehorizontaldistance/) { get; set; } | Tablo özellikleri tarafından belirtilen mutlak yatay yüzen tablo konumunu noktalar halinde alır veya ayarlar. Varsayılan değer 0'dır. |
| [AbsoluteVerticalDistance](../../aspose.words.tables/table/absoluteverticaldistance/) { get; set; } | Tablo özellikleri tarafından belirtilen mutlak dikey yüzen tablo konumunu noktalar halinde alır veya ayarlar. Varsayılan değer 0'dır. |
| [Alignment](../../aspose.words.tables/table/alignment/) { get; set; } | Satır içi tablonun belgede nasıl hizalanacağını belirtir. |
| [AllowAutoFit](../../aspose.words.tables/table/allowautofit/) { get; set; } | Microsoft Word ve Aspose.Words'ün bir tabloda hücrelerin boyutunu içeriğe uyacak şekilde otomatik olarak değiştirmesine olanak tanır. |
| [AllowCellSpacing](../../aspose.words.tables/table/allowcellspacing/) { get; set; } | "Hücreler arasında boşluk bırakılmasına izin ver" seçeneğini alır veya ayarlar. |
| [AllowOverlap](../../aspose.words.tables/table/allowoverlap/) { get; } | Bir yüzen tablonun, görüntülendiğinde belgedeki diğer yüzen nesnelerin kendi kapsamlarını kaplamasına izin verip vermeyeceğini alır. Varsayılan değer`doğru` . |
| [Bidi](../../aspose.words.tables/table/bidi/) { get; set; } | Bunun sağdan sola bir tablo olup olmadığını alır veya ayarlar. |
| [BottomPadding](../../aspose.words.tables/table/bottompadding/) { get; set; } | Hücrelerin içeriklerinin altına eklenecek boşluk miktarını (nokta cinsinden) alır veya ayarlar. |
| [CellSpacing](../../aspose.words.tables/table/cellspacing/) { get; set; } | Hücreler arasındaki boşluk miktarını (nokta cinsinden) alır veya ayarlar. |
| [Count](../../aspose.words/compositenode/count/) { get; } | Bu düğümün hemen alt düğümlerinin sayısını alır. |
| [CustomNodeId](../../aspose.words/node/customnodeid/) { get; set; } | Özel düğüm tanımlayıcısını belirtir. |
| [Description](../../aspose.words.tables/table/description/) { get; set; } | Bu tablonun açıklamasını alır veya ayarlar. Tabloda bulunan bilgilerin alternatif bir metin gösterimini sağlar. |
| [DistanceBottom](../../aspose.words.tables/table/distancebottom/) { get; set; } | Tablo altı ile çevresindeki metin arasındaki mesafeyi nokta cinsinden alır veya ayarlar. |
| [DistanceLeft](../../aspose.words.tables/table/distanceleft/) { get; set; } | Tablonun solu ile çevresindeki metin arasındaki mesafeyi noktalar halinde alır veya ayarlar. |
| [DistanceRight](../../aspose.words.tables/table/distanceright/) { get; set; } | Tablonun sağ tarafı ile çevresindeki metin arasındaki mesafeyi puan cinsinden alır veya ayarlar. |
| [DistanceTop](../../aspose.words.tables/table/distancetop/) { get; set; } | Tablo üstü ile çevresindeki metin arasındaki mesafeyi puan cinsinden alır veya ayarlar. |
| virtual [Document](../../aspose.words/node/document/) { get; } | Bu düğümün ait olduğu belgeyi alır. |
| [FirstChild](../../aspose.words/compositenode/firstchild/) { get; } | Düğümün ilk çocuğunu alır. |
| [FirstRow](../../aspose.words.tables/table/firstrow/) { get; } | İlkini döndürür[`Row`](../row/) tablodaki düğüm. |
| [HasChildNodes](../../aspose.words/compositenode/haschildnodes/) { get; } | Geri Döndürür`doğru` eğer bu düğümün herhangi bir alt düğümü varsa. |
| [HorizontalAnchor](../../aspose.words.tables/table/horizontalanchor/) { get; set; } | Yüzen tablonun yatay konumlandırmasının hesaplanacağı temel nesneyi alır. Varsayılan değerColumn . |
| override [IsComposite](../../aspose.words/compositenode/iscomposite/) { get; } | Geri Döndürür`doğru` çünkü bu düğümün alt düğümleri olabilir. |
| [LastChild](../../aspose.words/compositenode/lastchild/) { get; } | Düğümün son çocuğunu alır. |
| [LastRow](../../aspose.words.tables/table/lastrow/) { get; } | Sonuncuyu döndürür[`Row`](../row/) tablodaki düğüm. |
| [LeftIndent](../../aspose.words.tables/table/leftindent/) { get; set; } | Tablonun sol girintisini temsil eden değeri alır veya ayarlar. |
| [LeftPadding](../../aspose.words.tables/table/leftpadding/) { get; set; } | Hücrelerin içeriklerinin soluna eklenecek boşluk miktarını (nokta cinsinden) alır veya ayarlar. |
| [NextSibling](../../aspose.words/node/nextsibling/) { get; } | Bu düğümü hemen takip eden düğümü alır. |
| override [NodeType](../../aspose.words.tables/table/nodetype/) { get; } | Geri DöndürürTable . |
| [ParentNode](../../aspose.words/node/parentnode/) { get; } | Bu düğümün en yakın üst düğümünü alır. |
| [PreferredWidth](../../aspose.words.tables/table/preferredwidth/) { get; set; } | Tablonun tercih edilen genişliğini alır veya ayarlar. |
| [PreviousSibling](../../aspose.words/node/previoussibling/) { get; } | Bu düğümden hemen önceki düğümü alır. |
| [Range](../../aspose.words/node/range/) { get; } | Bir[`Range`](../../aspose.words/range/)bu düğümde bulunan bir belgenin bölümünü temsil eden nesne. |
| [RelativeHorizontalAlignment](../../aspose.words.tables/table/relativehorizontalalignment/) { get; set; } | Yüzen tablonun göreli yatay hizalamasını alır veya ayarlar. |
| [RelativeVerticalAlignment](../../aspose.words.tables/table/relativeverticalalignment/) { get; set; } | Yüzen tablonun göreli dikey hizalamasını alır veya ayarlar. |
| [RightPadding](../../aspose.words.tables/table/rightpadding/) { get; set; } | Hücrelerin içeriklerinin sağına eklenecek boşluk miktarını (nokta cinsinden) alır veya ayarlar. |
| [Rows](../../aspose.words.tables/table/rows/) { get; } | Tablonun satırlarına yazılmış erişim sağlar. |
| [Style](../../aspose.words.tables/table/style/) { get; set; } | Bu tabloya uygulanan tablo stilini alır veya ayarlar. |
| [StyleIdentifier](../../aspose.words.tables/table/styleidentifier/) { get; set; } | Bu tabloya uygulanan tablo stilinin yerel bağımsız stil tanımlayıcısını alır veya ayarlar. |
| [StyleName](../../aspose.words.tables/table/stylename/) { get; set; } | Bu tabloya uygulanan tablo stilinin adını alır veya ayarlar. |
| [StyleOptions](../../aspose.words.tables/table/styleoptions/) { get; set; } | Bu tabloya bir tablo stilinin nasıl uygulanacağını belirten bit bayraklarını alır veya ayarlar. |
| [TextWrapping](../../aspose.words.tables/table/textwrapping/) { get; set; } | Alır veya ayarlar[`TextWrapping`](./textwrapping/) tablo için. |
| [Title](../../aspose.words.tables/table/title/) { get; set; } | Bu tablonun başlığını alır veya ayarlar. Tabloda bulunan bilgilerin alternatif bir metin gösterimini sağlar. |
| [TopPadding](../../aspose.words.tables/table/toppadding/) { get; set; } | Hücrelerin içeriklerinin üstüne eklenecek boşluk miktarını (nokta cinsinden) alır veya ayarlar. |
| [VerticalAnchor](../../aspose.words.tables/table/verticalanchor/) { get; set; } | Yüzen tablonun dikey konumlandırmasının hesaplanacağı temel nesneyi alır. Varsayılan değerMargin . |

## yöntemler

| İsim | Tanım |
| --- | --- |
| override [Accept](../../aspose.words.tables/table/accept/)(*[DocumentVisitor](../../aspose.words/documentvisitor/)*) | Bir ziyaretçiyi kabul eder. |
| override [AcceptEnd](../../aspose.words.tables/table/acceptend/)(*[DocumentVisitor](../../aspose.words/documentvisitor/)*) | Tablonun sonunu ziyaret eden bir ziyaretçiyi kabul eder. |
| override [AcceptStart](../../aspose.words.tables/table/acceptstart/)(*[DocumentVisitor](../../aspose.words/documentvisitor/)*) | Tablonun başlangıcını ziyaret eden bir ziyaretçiyi kabul eder. |
| [AppendChild&lt;T&gt;](../../aspose.words/compositenode/appendchild/)(*T*) | Belirtilen düğümü bu düğüm için alt düğümler listesinin sonuna ekler. |
| [AutoFit](../../aspose.words.tables/table/autofit/)(*[AutoFitBehavior](../autofitbehavior/)*) | Tabloyu ve hücreleri belirtilen otomatik uyum davranışına göre yeniden boyutlandırır. |
| [ClearBorders](../../aspose.words.tables/table/clearborders/)() | Bu tablodaki tüm tablo ve hücre kenarlıklarını kaldırır. |
| [ClearShading](../../aspose.words.tables/table/clearshading/)() | Tablodaki tüm gölgelendirmeyi kaldırır. |
| [Clone](../../aspose.words/node/clone/)(*bool*) | Düğümün bir kopyasını oluşturur. |
| [ConvertToHorizontallyMergedCells](../../aspose.words.tables/table/converttohorizontallymergedcells/)() | Genişliğe göre yatay olarak birleştirilen hücreleri, genişliğe göre birleştirilen hücrelere dönüştürür.[`HorizontalMerge`](../cellformat/horizontalmerge/) . |
| [CreateNavigator](../../aspose.words/compositenode/createnavigator/)() | Düğümleri gezmek ve okumak için kullanılabilen gezgini oluşturur. |
| [EnsureMinimum](../../aspose.words.tables/table/ensureminimum/)() | Tabloda satır yoksa bir tane oluşturur ve ekler[`Row`](../row/) . |
| [GetAncestor](../../aspose.words/node/getancestor/)(*[NodeType](../../aspose.words/nodetype/)*) | Belirtilenin ilk atasını alır[`NodeType`](../../aspose.words/nodetype/) . |
| [GetAncestor](../../aspose.words/node/getancestor/)(*Type*) | Belirtilen nesne türünün ilk atasını alır. |
| [GetChild](../../aspose.words/compositenode/getchild/)(*[NodeType](../../aspose.words/nodetype/), int, bool*) | Belirtilen türle eşleşen N'inci alt düğümü döndürür. |
| [GetChildNodes](../../aspose.words/compositenode/getchildnodes/)(*[NodeType](../../aspose.words/nodetype/), bool*) | Belirtilen türle eşleşen alt düğümlerin canlı bir koleksiyonunu döndürür. |
| [GetEnumerator](../../aspose.words/compositenode/getenumerator/)() | Bu düğümün alt düğümleri üzerindeki her stil yinelemesi için destek sağlar. |
| override [GetText](../../aspose.words/compositenode/gettext/)() | Bu düğümün ve tüm alt düğümlerinin metnini alır. |
| [IndexOf](../../aspose.words/compositenode/indexof/)(*[Node](../../aspose.words/node/)*) | Alt düğüm dizisindeki belirtilen alt düğümün dizinini döndürür. |
| [InsertAfter&lt;T&gt;](../../aspose.words/compositenode/insertafter/)(*T, [Node](../../aspose.words/node/)*) | Belirtilen düğümü belirtilen referans düğümünden hemen sonra ekler. |
| [InsertBefore&lt;T&gt;](../../aspose.words/compositenode/insertbefore/)(*T, [Node](../../aspose.words/node/)*) | Belirtilen düğümü belirtilen referans düğümünden hemen önce ekler. |
| [NextPreOrder](../../aspose.words/node/nextpreorder/)(*[Node](../../aspose.words/node/)*) | Ön sipariş ağacı geçiş algoritmasına göre bir sonraki düğümü alır. |
| [PrependChild&lt;T&gt;](../../aspose.words/compositenode/prependchild/)(*T*) | Belirtilen düğümü bu düğüm için alt düğümler listesinin başına ekler. |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder/)(*[Node](../../aspose.words/node/)*) | Ön sipariş ağacı geçiş algoritmasına göre önceki düğümü alır. |
| [Remove](../../aspose.words/node/remove/)() | Kendini ana öğeden kaldırır. |
| [RemoveAllChildren](../../aspose.words/compositenode/removeallchildren/)() | Geçerli düğümün tüm alt düğümlerini kaldırır. |
| [RemoveChild&lt;T&gt;](../../aspose.words/compositenode/removechild/)(*T*) | Belirtilen alt düğümü kaldırır. |
| [RemoveSmartTags](../../aspose.words/compositenode/removesmarttags/)() | Tümünü kaldırır[`SmartTag`](../../aspose.words.markup/smarttag/) geçerli düğümün alt düğümleri. |
| [SelectNodes](../../aspose.words/compositenode/selectnodes/)(*string*) | XPath ifadesiyle eşleşen düğümlerin bir listesini seçer. |
| [SelectSingleNode](../../aspose.words/compositenode/selectsinglenode/)(*string*) | İlkini seçer[`Node`](../../aspose.words/node/) XPath ifadesiyle eşleşen. |
| [SetBorder](../../aspose.words.tables/table/setborder/)(*[BorderType](../../aspose.words/bordertype/), [LineStyle](../../aspose.words/linestyle/), double, Color, bool*) | Belirtilen tablo kenarlığını belirtilen çizgi stiline, genişliğe ve renge ayarlar. |
| [SetBorders](../../aspose.words.tables/table/setborders/)(*[LineStyle](../../aspose.words/linestyle/), double, Color*) | Tüm tablo kenarlıklarını belirtilen çizgi stiline, genişliğe ve renge ayarlar. |
| [SetShading](../../aspose.words.tables/table/setshading/)(*[TextureIndex](../../aspose.words/textureindex/), Color, Color*) | Tüm tabloda gölgelendirmeyi belirtilen değerlere ayarlar. |
| [ToString](../../aspose.words/node/tostring/)(*[SaveFormat](../../aspose.words/saveformat/)*) | Düğümün içeriğini belirtilen biçimde bir dizeye aktarır. |
| [ToString](../../aspose.words/node/tostring/)(*[SaveOptions](../../aspose.words.saving/saveoptions/)*) | Belirtilen kaydetme seçeneklerini kullanarak düğümün içeriğini bir dizeye aktarır. |

## Notlar

`Table` blok düzeyinde bir düğümdür ve türetilen sınıfların bir çocuğu olabilir[`Story`](../../aspose.words/story/) veya [`InlineStory`](../../aspose.words/inlinestory/).

`Table` bir veya daha fazlasını içerebilir[`Row`](../row/) düğümler.

Minimum geçerli bir tablonun en az bir tane olması gerekir[`Row`](../row/).

## Örnekler

Bir tablonun nasıl oluşturulacağını gösterir.

```csharp
Document doc = new Document();
Table table = new Table(doc);
doc.FirstSection.Body.AppendChild(table);

// Tablolar, hücreler içeren satırlar ve bu satırların içinde paragraflar olabilir
// tipik elemanlar olan koşular, şekiller ve hatta diğer tablolar ile.
// Bir tabloda "EnsureMinimum" metodunu çağırmak,
// tabloda en az bir satır, hücre ve paragraf var.
Row firstRow = new Row(doc);
table.AppendChild(firstRow);

Cell firstCell = new Cell(doc);
firstRow.AppendChild(firstCell);

Paragraph paragraph = new Paragraph(doc);
firstCell.AppendChild(paragraph);

// Tablonun ilk satırındaki ilk hücreye metin ekle.
Run run = new Run(doc, "Hello world!");
paragraph.AppendChild(run);

doc.Save(ArtifactsDir + "Table.CreateTable.docx");
```

Belgedeki tüm tablolarda nasıl gezinileceğini ve her hücrenin içeriğinin nasıl yazdırılacağını gösterir.

```csharp
Document doc = new Document(MyDir + "Tables.docx");
TableCollection tables = doc.FirstSection.Body.Tables;

Assert.AreEqual(2, tables.ToArray().Length);

for (int i = 0; i < tables.Count; i++)
{
    Console.WriteLine($"Start of Table {i}");

    RowCollection rows = tables[i].Rows;

    // Bir satır koleksiyonunu diziye kopyalamak için "ToArray" metodunu kullanabiliriz.
    Assert.AreEqual(rows, rows.ToArray());
    Assert.AreNotSame(rows, rows.ToArray());

    for (int j = 0; j < rows.Count; j++)
    {
        Console.WriteLine($"\tStart of Row {j}");

        CellCollection cells = rows[j].Cells;

        // Bir hücre koleksiyonunu diziye kopyalamak için "ToArray" metodunu kullanabiliriz.
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

Biçimlendirilmiş 2x2'lik bir tablonun nasıl oluşturulacağını gösterir.

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

// Tablo oluşturulurken, belge oluşturucu geçerli RowFormat/CellFormat özellik değerlerini uygulayacaktır
// imlecin bulunduğu geçerli satıra/hücreye ve bunları oluştururken oluşacak yeni satırlara/hücrelere.
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

// Daha önce eklenen satırlar ve hücreler, oluşturucunun biçimlendirmesinde yapılan değişikliklerden geriye dönük olarak etkilenmez.
Assert.AreEqual(0, table.Rows[0].RowFormat.Height);
Assert.AreEqual(HeightRule.Auto, table.Rows[0].RowFormat.HeightRule);
Assert.AreEqual(100, table.Rows[1].RowFormat.Height);
Assert.AreEqual(HeightRule.Exactly, table.Rows[1].RowFormat.HeightRule);
Assert.AreEqual(TextOrientation.Upward, table.Rows[1].Cells[0].CellFormat.Orientation);
Assert.AreEqual(TextOrientation.Downward, table.Rows[1].Cells[1].CellFormat.Orientation);

doc.Save(ArtifactsDir + "DocumentBuilder.BuildTable.docx");
```

Belge oluşturucu kullanmadan iç içe geçmiş tablonun nasıl oluşturulacağını gösterir.

```csharp
public void CreateNestedTable()
{
    Document doc = new Document();

    // Üç satır ve dört sütundan oluşan dış tabloyu oluştur ve ardından bunu belgeye ekle.
    Table outerTable = CreateTable(doc, 3, 4, "Outer Table");
    doc.FirstSection.Body.AppendChild(outerTable);

    // İki satır ve iki sütundan oluşan başka bir tablo oluştur ve bunu ilk tablonun ilk hücresine ekle.
    Table innerTable = CreateTable(doc, 2, 2, "Inner Table");
    outerTable.FirstRow.FirstCell.AppendChild(innerTable);

    doc.Save(ArtifactsDir + "Table.CreateNestedTable.docx");
}

/// <summary>
/// Belgede, her hücrede belirtilen boyutlar ve metinle yeni bir tablo oluşturur.
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

    // Tablonuza sırasıyla bir başlık ve açıklama eklemek için "Başlık" ve "Açıklama" özelliklerini kullanabilirsiniz.
    // Bu özellikleri kullanabilmemiz için tablonun en az bir satırının olması gerekir.
    // Bu özellikler ISO/IEC 29500 uyumlu .docx belgeleri için anlamlıdır (OoxmlCompliance sınıfına bakın).
    // Belgeyi ISO/IEC 29500 öncesi biçimlerde kaydedersek, Microsoft Word bu özellikleri yoksayar.
    table.Title = "Aspose table title";
    table.Description = "Aspose table description";

    return table;
}
```

### Ayrıca bakınız

* class [CompositeNode](../../aspose.words/compositenode/)
* ad alanı [Aspose.Words.Tables](../../aspose.words.tables/)
* toplantı [Aspose.Words](../../)
