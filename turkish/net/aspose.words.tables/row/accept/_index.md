---
title: Row.Accept
linktitle: Accept
articleTitle: Accept
second_title: .NET için Aspose.Words
description: Web sitenizin başarısı için ziyaretçi katılımını artırmak ve kullanıcı etkileşimlerini kolaylaştırmak üzere tasarlanmış Satır Kabul yöntemini keşfedin.
type: docs
weight: 120
url: /tr/net/aspose.words.tables/row/accept/
---
## Row.Accept method

Bir ziyaretçiyi kabul eder.

```csharp
public override bool Accept(DocumentVisitor visitor)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| visitor | DocumentVisitor | Düğümleri ziyaret edecek ziyaretçi. |

### Geri dönüş değeri

Tüm düğümler ziyaret edildiyse doğru; eğer ziyaret edilmediyse yanlış[`DocumentVisitor`](../../../aspose.words/documentvisitor/) tüm düğümleri ziyaret etmeden önce işlemi durdurdu.

## Notlar

Bu düğüm ve tüm alt düğümleri üzerinde numaralandırma yapar. Her düğüm, ilgili bir yöntemi çağırır[`DocumentVisitor`](../../../aspose.words/documentvisitor/).

Daha fazla bilgi için Ziyaretçi tasarım desenine bakın.

Çağrılar[`VisitRowStart`](../../../aspose.words/documentvisitor/visitrowstart/) , sonra arar[`Accept`](../../../aspose.words/node/accept/) section ve çağrıların tüm alt düğümleri için[`VisitRowEnd`](../../../aspose.words/documentvisitor/visitrowend/) sonunda.

## Örnekler

Bir belgedeki her tablonun düğüm yapısının nasıl yazdırılacağını gösterir.

```csharp
public void TableToText()
{
    Document doc = new Document(MyDir + "DocumentVisitor-compatible features.docx");
    TableStructurePrinter visitor = new TableStructurePrinter();

    // Bir belge ziyaretçisini kabul etmek için bir bileşik düğüm aldığımızda, ziyaretçi kabul eden düğümü ziyaret eder,
    // ve sonra düğümün tüm çocuklarını derinlemesine bir şekilde dolaşır.
    // Ziyaretçi ziyaret edilen her düğümü okuyabilir ve değiştirebilir.
    doc.Accept(visitor);

    Console.WriteLine(visitor.GetText());
}

/// <summary>
/// Bir düğümün alt düğümlerinin ikili olmayan ağacını dolaşır.
/// Karşılaşılan tüm Tablo düğümlerini ve bunların alt öğelerini içeren bir dize biçiminde bir harita oluşturur.
/// </summary>
public class TableStructurePrinter : DocumentVisitor
{
    public TableStructurePrinter()
    {
        mVisitedTables = new StringBuilder();
        mVisitorIsInsideTable = false;
    }

    public string GetText()
    {
        return mVisitedTables.ToString();
    }

    /// <summary>
    /// Belgede bir Çalıştırma düğümüyle karşılaşıldığında çağrılır.
    /// Tabloların içinde olmayan çalıştırmalar kaydedilmez.
    /// </summary>
    public override VisitorAction VisitRun(Run run)
    {
        if (mVisitorIsInsideTable) IndentAndAppendLine("[Run] \"" + run.GetText() + "\"");

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Belgede bir Tablo ile karşılaşıldığında çağrılır.
    /// </summary>
    public override VisitorAction VisitTableStart(Table table)
    {
        int rows = 0;
        int columns = 0;

        if (table.Rows.Count > 0)
        {
            rows = table.Rows.Count;
            columns = table.FirstRow.Count;
        }

        IndentAndAppendLine("[Table start] Size: " + rows + "x" + columns);
        mDocTraversalDepth++;
        mVisitorIsInsideTable = true;

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Bir Tablo düğümünün tüm alt düğümleri ziyaret edildikten sonra çağrılır.
    /// </summary>
    public override VisitorAction VisitTableEnd(Table table)
    {
        mDocTraversalDepth--;
        IndentAndAppendLine("[Table end]");
        mVisitorIsInsideTable = false;

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Belgede bir Satır düğümüyle karşılaşıldığında çağrılır.
    /// </summary>
    public override VisitorAction VisitRowStart(Row row)
    {
        string rowContents = row.GetText().TrimEnd(new []{ '\u0007', ' ' }).Replace("\u0007", ", ");
        int rowWidth = row.IndexOf(row.LastCell) + 1;
        int rowIndex = row.ParentTable.IndexOf(row);
        string rowStatusInTable = row.IsFirstRow && row.IsLastRow ? "only" : row.IsFirstRow ? "first" : row.IsLastRow ? "last" : "";
        if (rowStatusInTable != "")
        {
            rowStatusInTable = $", the {rowStatusInTable} row in this table,";
        }

        IndentAndAppendLine($"[Row start] Row #{++rowIndex}{rowStatusInTable} width {rowWidth}, \"{rowContents}\"");
        mDocTraversalDepth++;

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Bir Satır düğümünün tüm alt düğümleri ziyaret edildikten sonra çağrılır.
    /// </summary>
    public override VisitorAction VisitRowEnd(Row row)
    {
        mDocTraversalDepth--;
        IndentAndAppendLine("[Row end]");

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Belgede bir Hücre düğümüyle karşılaşıldığında çağrılır.
    /// </summary>
    public override VisitorAction VisitCellStart(Cell cell)
    {
        Row row = cell.ParentRow;
        Table table = row.ParentTable;
        string cellStatusInRow = cell.IsFirstCell && cell.IsLastCell ? "only" : cell.IsFirstCell ? "first" : cell.IsLastCell ? "last" : "";
        if (cellStatusInRow != "")
        {
            cellStatusInRow = $", the {cellStatusInRow} cell in this row";
        }

        IndentAndAppendLine($"[Cell start] Row {table.IndexOf(row) + 1}, Col {row.IndexOf(cell) + 1}{cellStatusInRow}");
        mDocTraversalDepth++;

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Bir Hücre düğümünün tüm alt düğümleri ziyaret edildikten sonra çağrılır.
    /// </summary>
    public override VisitorAction VisitCellEnd(Cell cell)
    {
        mDocTraversalDepth--;
        IndentAndAppendLine("[Cell end]");
        return VisitorAction.Continue;
    }

    /// <summary>
    /// StringBuilder'a bir satır ekleyin ve ziyaretçinin derinliğine bağlı olarak girintisini ayarlayın
    /// Mevcut tablonun alt düğüm ağacına.
    /// </summary>
    /// <param adı="metin"></param>
    private void IndentAndAppendLine(string text)
    {
        for (int i = 0; i < mDocTraversalDepth; i++)
        {
            mVisitedTables.Append("|  ");
        }

        mVisitedTables.AppendLine(text);
    }

    private bool mVisitorIsInsideTable;
    private int mDocTraversalDepth;
    private readonly StringBuilder mVisitedTables;
}
```

### Ayrıca bakınız

* class [DocumentVisitor](../../../aspose.words/documentvisitor/)
* class [Row](../)
* ad alanı [Aspose.Words.Tables](../../../aspose.words.tables/)
* toplantı [Aspose.Words](../../../)
