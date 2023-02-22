---
title: DocumentBuilder.InsertCell
second_title: Aspose.Words for .NET API Referansı
description: DocumentBuilder yöntem. Belgeye bir tablo hücresi ekler.
type: docs
weight: 250
url: /tr/net/aspose.words/documentbuilder/insertcell/
---
## DocumentBuilder.InsertCell method

Belgeye bir tablo hücresi ekler.

```csharp
public Cell InsertCell()
```

### Geri dönüş değeri

Yeni eklenen hücre düğümü.

### Notlar

Bir masa başlatmak için aramanız yeterli **EkleHücre** . Bundan sonra, diğer yöntemlerini kullanarak eklediğiniz herhangi bir içerik[`DocumentBuilder`](../) sınıfı geçerli hücreye eklenecektir.

Aynı satırda yeni bir hücre başlatmak için arayın **EkleHücre** Yeniden.

Bir tablo satırı çağrısını sonlandırmak için[`EndRow`](../endrow/).

Kullan[`CellFormat`](../cellformat/)hücre biçimlendirmesini belirtmek için özellik.

### Örnekler

Tablo oluşturmak için belge oluşturucunun nasıl kullanılacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Tabloyu başlatın, ardından ilk satırı iki hücreyle doldurun.
builder.StartTable();
builder.InsertCell();
builder.Write("Row 1, Cell 1.");
builder.InsertCell();
builder.Write("Row 1, Cell 2.");

// Yeni bir satır başlatmak için oluşturucunun "EndRow" yöntemini çağırın.
builder.EndRow();
builder.InsertCell();
builder.Write("Row 2, Cell 1.");
builder.InsertCell();
builder.Write("Row 2, Cell 2.");
builder.EndTable();

doc.Save(ArtifactsDir + "DocumentBuilder.CreateTable.docx");
```

Özel kenarlıklı bir tablonun nasıl oluşturulacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.StartTable();

// Bir belge oluşturucu için tablo biçimlendirme seçeneklerini ayarlama
// onları eklediğimiz her satıra ve hücreye uygulayacak.
builder.ParagraphFormat.Alignment = ParagraphAlignment.Center;

builder.CellFormat.ClearFormatting();
builder.CellFormat.Width = 150;
builder.CellFormat.VerticalAlignment = CellVerticalAlignment.Center;
builder.CellFormat.Shading.BackgroundPatternColor = Color.GreenYellow;
builder.CellFormat.WrapText = false;
builder.CellFormat.FitText = true;

builder.RowFormat.ClearFormatting();
builder.RowFormat.HeightRule = HeightRule.Exactly;
builder.RowFormat.Height = 50;
builder.RowFormat.Borders.LineStyle = LineStyle.Engrave3D;
builder.RowFormat.Borders.Color = Color.Orange;

builder.InsertCell();
builder.Write("Row 1, Col 1");

builder.InsertCell();
builder.Write("Row 1, Col 2");
builder.EndRow();

// Biçimlendirmeyi değiştirmek, onu geçerli hücreye uygular,
// ve daha sonra oluşturucu ile oluşturduğumuz yeni hücreler.
// Bu daha önce eklediğimiz hücreleri etkilemeyecektir.
builder.CellFormat.Shading.ClearFormatting();

builder.InsertCell();
builder.Write("Row 2, Col 1");

builder.InsertCell();
builder.Write("Row 2, Col 2");

builder.EndRow();

// Dikey metne sığdırmak için satır yüksekliğini artırın.
builder.InsertCell();
builder.RowFormat.Height = 150;
builder.CellFormat.Orientation = TextOrientation.Upward;
builder.Write("Row 3, Col 1");

builder.InsertCell();
builder.CellFormat.Orientation = TextOrientation.Downward;
builder.Write("Row 3, Col 2");

builder.EndRow();
builder.EndTable();

doc.Save(ArtifactsDir + "DocumentBuilder.InsertTable.docx");
```

### Ayrıca bakınız

* class [Cell](../../../aspose.words.tables/cell/)
* class [DocumentBuilder](../)
* ad alanı [Aspose.Words](../../documentbuilder/)
* toplantı [Aspose.Words](../../../)


