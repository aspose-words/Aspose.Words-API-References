---
title: CellFormat.Width
second_title: Aspose.Words for .NET API Referansı
description: CellFormat mülk. Hücrenin genişliğini nokta olarak alır.
type: docs
weight: 140
url: /tr/net/aspose.words.tables/cellformat/width/
---
## CellFormat.Width property

Hücrenin genişliğini nokta olarak alır.

```csharp
public double Width { get; set; }
```

### Notlar

Genişlik, Aspose.Words tarafından belge yükleme ve kaydetme sırasında hesaplanır. Şu anda tablo, hücre ve belge özelliklerinin her kombinasyonu desteklenmemektedir. Döndürülen değer bazı belgeler için doğru olmayabilir. Belge MS Word'de açıldığında MS Word tarafından hesaplanan hücre genişliği.

Bu özelliğin ayarlanması önerilmez. Hücrenin gerçekte ayarlanan genişliğe sahip olacağına dair bir garanti yoktur. Genişlik, hücre içeriklerini otomatik sığdırma tablosu düzeninde barındıracak şekilde ayarlanabilir. Diğer satırlardaki hücreler çakışan genişliğe sahip olabilir settings. Tablo, kaba sığacak veya tablo genişliği ayarlarını karşılayacak şekilde yeniden boyutlandırılabilir. Kullanmayı düşünün[`PreferredWidth`](../preferredwidth/) hücre genişliğini ayarlamak için. Bu özellik setlerini ayarlama[`PreferredWidth`](../preferredwidth/)15.8. sürümünden beri örtülü olarak

### Örnekler

Belge oluşturucuyla hücrelerin nasıl biçimlendirileceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Table table = builder.StartTable();
builder.InsertCell();
builder.Write("Row 1, cell 1.");

// İkinci bir hücre ekleyin ve ardından hücre metni dolgu seçeneklerini yapılandırın.
// Oluşturucu bu ayarları mevcut hücresine uygulayacak ve daha sonra oluşturulacak yeni hücrelere uygulayacaktır.
builder.InsertCell();

CellFormat cellFormat = builder.CellFormat;
cellFormat.Width = 250;
cellFormat.LeftPadding = 30;
cellFormat.RightPadding = 30;
cellFormat.TopPadding = 30;
cellFormat.BottomPadding = 30;

builder.Write("Row 1, cell 2.");
builder.EndRow();
builder.EndTable();

// İlk hücre dolgunun yeniden yapılandırılmasından etkilenmedi ve hala varsayılan değerleri koruyor.
Assert.AreEqual(0.0d, table.FirstRow.Cells[0].CellFormat.Width);
Assert.AreEqual(5.4d, table.FirstRow.Cells[0].CellFormat.LeftPadding);
Assert.AreEqual(5.4d, table.FirstRow.Cells[0].CellFormat.RightPadding);
Assert.AreEqual(0.0d, table.FirstRow.Cells[0].CellFormat.TopPadding);
Assert.AreEqual(0.0d, table.FirstRow.Cells[0].CellFormat.BottomPadding);

Assert.AreEqual(250.0d, table.FirstRow.Cells[1].CellFormat.Width);
Assert.AreEqual(30.0d, table.FirstRow.Cells[1].CellFormat.LeftPadding);
Assert.AreEqual(30.0d, table.FirstRow.Cells[1].CellFormat.RightPadding);
Assert.AreEqual(30.0d, table.FirstRow.Cells[1].CellFormat.TopPadding);
Assert.AreEqual(30.0d, table.FirstRow.Cells[1].CellFormat.BottomPadding);

// İlk hücre, çıktı belgesinde komşu hücrenin boyutuna uyacak şekilde büyümeye devam edecek.
doc.Save(ArtifactsDir + "DocumentBuilder.SetCellFormatting.docx");
```

Özel kenarlıklara sahip bir tablonun nasıl oluşturulacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.StartTable();

// Belge oluşturucu için tablo biçimlendirme seçeneklerini ayarlama
// bunları eklediğimiz her satıra ve hücreye uygulayacaktır.
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

// Biçimlendirmeyi değiştirmek onu geçerli hücreye uygulayacaktır,
// ve daha sonra oluşturucuyla oluşturduğumuz yeni hücreler.
// Bu daha önce eklediğimiz hücreleri etkilemeyecektir.
builder.CellFormat.Shading.ClearFormatting();

builder.InsertCell();
builder.Write("Row 2, Col 1");

builder.InsertCell();
builder.Write("Row 2, Col 2");

builder.EndRow();

// Dikey metne sığacak şekilde satır yüksekliğini artırın.
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

* class [CellFormat](../)
* ad alanı [Aspose.Words.Tables](../../cellformat/)
* toplantı [Aspose.Words](../../../)


