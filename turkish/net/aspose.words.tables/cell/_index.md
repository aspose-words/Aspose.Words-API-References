---
title: Cell
second_title: Aspose.Words for .NET API Referansı
description: Bir tablo hücresini temsil eder.
type: docs
weight: 5940
url: /tr/net/aspose.words.tables/cell/
---
## Cell class

Bir tablo hücresini temsil eder.

```csharp
public class Cell : CompositeNode
```

## yapıcılar

| İsim | Tanım |
| --- | --- |
| [Cell](cell)(DocumentBase) | Yeni bir örneğini başlatır **Hücre** sınıf. |

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [CellFormat](../../aspose.words.tables/cell/cellformat) { get; } | Hücrenin biçimlendirme özelliklerine erişim sağlar. |
| [ChildNodes](../../aspose.words/compositenode/childnodes) { get; } | Bu düğümün tüm acil alt düğümlerini alır. |
| [Count](../../aspose.words/compositenode/count) { get; } | Bu düğümün acil alt öğelerinin sayısını alır. |
| [CustomNodeId](../../aspose.words/node/customnodeid) { get; set; } | Özel düğüm tanımlayıcısını belirtir. |
| virtual [Document](../../aspose.words/node/document) { get; } | Bu düğümün ait olduğu belgeyi alır. |
| [FirstChild](../../aspose.words/compositenode/firstchild) { get; } | Düğümün ilk alt öğesini alır. |
| [FirstParagraph](../../aspose.words.tables/cell/firstparagraph) { get; } | En yakın alt öğeler arasında ilk paragrafı alır. |
| [HasChildNodes](../../aspose.words/compositenode/haschildnodes) { get; } | Bu düğümün herhangi bir alt düğümü varsa doğru döndürür. |
| override [IsComposite](../../aspose.words/compositenode/iscomposite) { get; } | Bu düğümün alt düğümleri olabileceğinden true değerini döndürür. |
| [IsFirstCell](../../aspose.words.tables/cell/isfirstcell) { get; } | Bu, bir satırdaki ilk hücreyse doğrudur; aksi halde yanlış. |
| [IsLastCell](../../aspose.words.tables/cell/islastcell) { get; } | Bu, bir satırdaki son hücreyse doğrudur; aksi halde yanlış. |
| [LastChild](../../aspose.words/compositenode/lastchild) { get; } | Düğümün son alt öğesini alır. |
| [LastParagraph](../../aspose.words.tables/cell/lastparagraph) { get; } | En yakın alt öğeler arasında son paragrafı alır. |
| [NextSibling](../../aspose.words/node/nextsibling) { get; } | Bu düğümden hemen sonraki düğümü alır. |
| override [NodeType](../../aspose.words.tables/cell/nodetype) { get; } | İade **DüğümTürü.Hücre** . |
| [Paragraphs](../../aspose.words.tables/cell/paragraphs) { get; } | Hücrenin doğrudan alt öğeleri olan bir paragraf koleksiyonu alır. |
| [ParentNode](../../aspose.words/node/parentnode) { get; } | Bu düğümün hemen üst öğesini alır. |
| [ParentRow](../../aspose.words.tables/cell/parentrow) { get; } | Hücrenin üst satırını döndürür. |
| [PreviousSibling](../../aspose.words/node/previoussibling) { get; } | Bu düğümden hemen önceki düğümü alır. |
| [Range](../../aspose.words/node/range) { get; } | Bir döndürür **Menzil** belgenin bu düğümde bulunan bölümünü temsil eden nesne. |
| [Tables](../../aspose.words.tables/cell/tables) { get; } | Hücrenin hemen alt öğeleri olan tabloların bir koleksiyonunu alır. |

## yöntemler

| İsim | Tanım |
| --- | --- |
| override [Accept](../../aspose.words.tables/cell/accept)(DocumentVisitor) | Bir ziyaretçiyi kabul eder. |
| [AppendChild](../../aspose.words/compositenode/appendchild)(Node) | Belirtilen düğümü, bu düğüm için alt düğümler listesinin sonuna ekler. |
| [Clone](../../aspose.words/node/clone)(bool) | Düğümün bir kopyasını oluşturur. |
| [CreateNavigator](../../aspose.words/compositenode/createnavigator)() | Sistem kullanımı için ayrılmıştır. IXPathNavigable. |
| [EnsureMinimum](../../aspose.words.tables/cell/ensureminimum)() | Son alt öğe bir paragraf değilse, boş bir paragraf oluşturur ve ekler. |
| [GetAncestor](../../aspose.words/node/getancestor)(NodeType) | Belirtilenin ilk atasını alır[`NodeType`](../../aspose.words/nodetype) . |
| [GetAncestor](../../aspose.words/node/getancestor)(Type) | Belirtilen nesne türünün ilk üst öğesini alır. |
| [GetChild](../../aspose.words/compositenode/getchild)(NodeType, int, bool) | Belirtilen türle eşleşen N. alt düğümü döndürür. |
| [GetChildNodes](../../aspose.words/compositenode/getchildnodes)(NodeType, bool) | Belirtilen türle eşleşen canlı bir alt düğüm koleksiyonu döndürür. |
| [GetEnumerator](../../aspose.words/compositenode/getenumerator)() | Bu düğümün alt düğümleri üzerinde her stil yinelemesi için destek sağlar. |
| override [GetText](../../aspose.words/compositenode/gettext)() | Bu düğümün ve tüm alt öğelerinin metnini alır. |
| [IndexOf](../../aspose.words/compositenode/indexof)(Node) | Alt düğüm dizisindeki belirtilen alt düğümün dizinini döndürür. |
| [InsertAfter](../../aspose.words/compositenode/insertafter)(Node, Node) | Belirtilen referans düğümünden hemen sonra belirtilen düğümü ekler. |
| [InsertBefore](../../aspose.words/compositenode/insertbefore)(Node, Node) | Belirtilen düğümü, belirtilen referans düğümünden hemen önce ekler. |
| [NextPreOrder](../../aspose.words/node/nextpreorder)(Node) | Ön sipariş ağaç geçiş algoritmasına göre sonraki düğümü alır. |
| [PrependChild](../../aspose.words/compositenode/prependchild)(Node) | Belirtilen düğümü, bu düğüm için alt düğümler listesinin başına ekler. |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder)(Node) | Ön sipariş ağacı geçiş algoritmasına göre önceki düğümü alır. |
| [Remove](../../aspose.words/node/remove)() | Kendini üst öğeden kaldırır. |
| [RemoveAllChildren](../../aspose.words/compositenode/removeallchildren)() | Geçerli düğümün tüm alt düğümlerini kaldırır. |
| [RemoveChild](../../aspose.words/compositenode/removechild)(Node) | Belirtilen alt düğümü kaldırır. |
| [RemoveSmartTags](../../aspose.words/compositenode/removesmarttags)() | Tümünü kaldırır[`SmartTag`](../../aspose.words.markup/smarttag) geçerli düğümün alt düğümleri. |
| [SelectNodes](../../aspose.words/compositenode/selectnodes)(string) | XPath ifadesiyle eşleşen düğümlerin listesini seçer. |
| [SelectSingleNode](../../aspose.words/compositenode/selectsinglenode)(string) | XPath ifadesiyle eşleşen ilk Düğümü seçer. |
| [ToString](../../aspose.words/node/tostring)(SaveFormat) | Düğümün içeriğini belirtilen biçimde bir dizeye aktarır. |
| [ToString](../../aspose.words/node/tostring)(SaveOptions) | Belirtilen kaydetme seçeneklerini kullanarak düğümün içeriğini bir dizeye aktarır. |

### Notlar

**Hücre** sadece bir çocuğun çocuğu olabilir **Sıra**.

**Hücre** blok düzeyinde düğümler içerebilir **Paragraf** ve **Masa**.

Minimum geçerli bir hücrenin en az bir tane olması gerekir **Paragraf**.

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

* class [CompositeNode](../../aspose.words/compositenode)
* ad alanı [Aspose.Words.Tables](../../aspose.words.tables)
* toplantı [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
