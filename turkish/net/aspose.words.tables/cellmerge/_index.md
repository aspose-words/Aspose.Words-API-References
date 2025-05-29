---
title: CellMerge Enum
linktitle: CellMerge
articleTitle: CellMerge
second_title: .NET için Aspose.Words
description: Verimli tablo hücre birleştirme için Aspose.Words.Tables.CellMerge enum'unu keşfedin. Belge düzenlerinizi kusursuz entegrasyon ve esneklikle geliştirin.
type: docs
weight: 7120
url: /tr/net/aspose.words.tables/cellmerge/
---
## CellMerge enumeration

Bir tabloda bulunan bir hücrenin diğer hücrelerle nasıl birleştirileceğini belirtir.

```csharp
public enum CellMerge
```

### değerler

| İsim | Değer | Tanım |
| --- | --- | --- |
| None | `0` | Hücre birleştirilmedi. |
| First | `1` | Hücre, birleştirilmiş hücreler aralığındaki ilk hücredir. |
| Previous | `2` | Hücre, bir önceki hücreye yatay veya dikey olarak birleştirilir. |

## Örnekler

Tablo hücrelerinin yatay olarak nasıl birleştirileceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// İlk satırın ilk sütununa bir hücre ekle.
// Bu hücre yatay olarak birleştirilmiş hücrelerden oluşan bir aralığın ilki olacaktır.
builder.InsertCell();
builder.CellFormat.HorizontalMerge = CellMerge.First;
builder.Write("Text in merged cells.");

// İlk satırın ikinci sütununa bir hücre ekleyin. Metin içerikleri eklemek yerine,
// bu hücreyi doğrudan sola eklediğimiz ilk hücreyle birleştireceğiz.
builder.InsertCell();
builder.CellFormat.HorizontalMerge = CellMerge.Previous;
builder.EndRow();

// İkinci satıra iki tane birleştirilmemiş hücre daha ekle.
builder.CellFormat.HorizontalMerge = CellMerge.None;
builder.InsertCell();
builder.Write("Text in unmerged cell.");
builder.InsertCell();
builder.Write("Text in unmerged cell.");
builder.EndRow();
builder.EndTable();

doc.Save(ArtifactsDir + "CellFormat.HorizontalMerge.docx");
```

Hücrenin yatay ve dikey birleştirme türünü yazdırır.

```csharp
public void CheckCellsMerged()
{
    Document doc = new Document(MyDir + "Table with merged cells.docx");
    Table table = doc.FirstSection.Body.Tables[0];

    foreach (Row row in table.Rows)
        foreach (Cell cell in row.Cells)
            Console.WriteLine(PrintCellMergeType(cell));
}

public string PrintCellMergeType(Cell cell)
{
    bool isHorizontallyMerged = cell.CellFormat.HorizontalMerge != CellMerge.None;
    bool isVerticallyMerged = cell.CellFormat.VerticalMerge != CellMerge.None;
    string cellLocation =
        $"R{cell.ParentRow.ParentTable.IndexOf(cell.ParentRow) + 1}, C{cell.ParentRow.IndexOf(cell) + 1}";

    if (isHorizontallyMerged && isVerticallyMerged)
        return $"The cell at {cellLocation} is both horizontally and vertically merged";
    if (isHorizontallyMerged)
        return $"The cell at {cellLocation} is horizontally merged.";

    return isVerticallyMerged ? $"The cell at {cellLocation} is vertically merged" : $"The cell at {cellLocation} is not merged";
}
```

Tablo hücrelerinin dikey olarak nasıl birleştirileceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// İlk satırın ilk sütununa bir hücre ekle.
// Bu hücre, dikey olarak birleştirilmiş hücrelerden oluşan bir aralığın ilki olacaktır.
builder.InsertCell();
builder.CellFormat.VerticalMerge = CellMerge.First;
builder.Write("Text in merged cells.");

// İlk satırın ikinci sütununa bir hücre ekle, ardından satırı sonlandır.
// Ayrıca, oluşturulan hücrelerde dikey birleştirmeyi devre dışı bırakmak için oluşturucuyu yapılandırın.
builder.InsertCell();
builder.CellFormat.VerticalMerge = CellMerge.None;
builder.Write("Text in unmerged cell.");
builder.EndRow();

 // İkinci satırın ilk sütununa bir hücre ekle.
// Metin içeriği eklemek yerine, bu hücreyi doğrudan üstüne eklediğimiz ilk hücreyle birleştireceğiz.
builder.InsertCell();
builder.CellFormat.VerticalMerge = CellMerge.Previous;

// İkinci satırın ikinci sütununa başka bir bağımsız hücre ekle.
builder.InsertCell();
builder.CellFormat.VerticalMerge = CellMerge.None;
builder.Write("Text in unmerged cell.");
builder.EndRow();
builder.EndTable();

doc.Save(ArtifactsDir + "CellFormat.VerticalMerge.docx");
```

### Ayrıca bakınız

* ad alanı [Aspose.Words.Tables](../../aspose.words.tables/)
* toplantı [Aspose.Words](../../)
