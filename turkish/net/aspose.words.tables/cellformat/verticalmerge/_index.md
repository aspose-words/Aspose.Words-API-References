---
title: CellFormat.VerticalMerge
linktitle: VerticalMerge
articleTitle: VerticalMerge
second_title: .NET için Aspose.Words
description: Elektronik tablolarda kesintisiz dikey hücre birleştirme için CellFormat VerticalMerge özelliğini keşfedin. Veri organizasyonunu ve sunumunu zahmetsizce geliştirin!
type: docs
weight: 130
url: /tr/net/aspose.words.tables/cellformat/verticalmerge/
---
## CellFormat.VerticalMerge property

Hücrenin diğer hücrelerle dikey olarak nasıl birleştirileceğini belirtir.

```csharp
public CellMerge VerticalMerge { get; set; }
```

## Notlar

Hücreler yalnızca sol ve sağ sınırları aynıysa dikey olarak birleştirilebilir.

Hücreler dikey olarak birleştirildiğinde, birleştirilen hücrelerin görüntüleme alanları birleştirilir. Birleştirilen alan, ilk dikey olarak birleştirilen hücrenin içeriğini görüntülemek için kullanılır ve diğer tüm dikey olarak birleştirilen hücreler boş olmalıdır.

## Örnekler

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

* enum [CellMerge](../../cellmerge/)
* class [CellFormat](../)
* ad alanı [Aspose.Words.Tables](../../../aspose.words.tables/)
* toplantı [Aspose.Words](../../../)
