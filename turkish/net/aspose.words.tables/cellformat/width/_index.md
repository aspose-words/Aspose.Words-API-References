---
title: CellFormat.Width
linktitle: Width
articleTitle: Width
second_title: .NET için Aspose.Words
description: Hücre genişliğini noktalarla kolayca ölçmek, elektronik tablonuzun düzenini ve okunabilirliğini artırmak için CellFormat Width özelliğini keşfedin.
type: docs
weight: 140
url: /tr/net/aspose.words.tables/cellformat/width/
---
## CellFormat.Width property

Hücrenin genişliğini noktalar halinde alır.

```csharp
public double Width { get; set; }
```

## Notlar

Genişlik, Aspose.Words tarafından belge yüklenirken ve kaydedilirken hesaplanır. Şu anda, tablo, hücre ve belge özelliklerinin her kombinasyonu desteklenmemektedir. Döndürülen değer bazı belgeler için doğru olmayabilir. Belge MS Word'de açıldığında, MS Word tarafından hesaplanan hücre genişliğiyle tam olarak eşleşmeyebilir.

Bu özelliğin ayarlanması önerilmez. Hücrenin gerçekten ayarlanan genişliğe sahip olacağının garantisi yoktur. Genişlik, otomatik sığdırılan bir tablo düzeninde hücre içeriklerine uyacak şekilde ayarlanabilir. Diğer satırlardaki hücrelerin çakışan genişlik ayarları olabilir. Tablo, kapsayıcıya sığacak veya tablo genişliği ayarlarını karşılayacak şekilde yeniden boyutlandırılabilir. Şunu kullanmayı düşünün:[`PreferredWidth`](../preferredwidth/)hücre genişliğini ayarlamak için. Bu özelliği ayarlamak[`PreferredWidth`](../preferredwidth/) dolaylı olarak 15.8. sürümünden beri

## Örnekler

Belge oluşturucuyla hücrelerin nasıl biçimlendirileceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Table table = builder.StartTable();
builder.InsertCell();
builder.Write("Row 1, cell 1.");

// İkinci bir hücre ekleyin ve ardından hücre metin dolgusu seçeneklerini yapılandırın.
// Oluşturucu bu ayarları mevcut hücreye uygulayacak ve daha sonra oluşturulan tüm yeni hücrelere uygulayacaktır.
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

// İlk hücre, dolgu yeniden yapılandırmasından etkilenmedi ve hala varsayılan değerleri koruyor.
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

// İlk hücre, komşu hücresinin boyutuna uyacak şekilde çıktı belgesinde büyümeye devam edecektir.
doc.Save(ArtifactsDir + "DocumentBuilder.SetCellFormatting.docx");
```

Özel kenarlıkları olan bir tablonun nasıl oluşturulacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.StartTable();

// Bir belge oluşturucu için tablo biçimlendirme seçeneklerini ayarlama
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

// Biçimlendirmeyi değiştirmek, bunu geçerli hücreye uygulayacaktır.
// ve sonrasında builder ile oluşturduğumuz yeni hücreler.
// Bu daha önce eklediğimiz hücreleri etkilemeyecektir.
builder.CellFormat.Shading.ClearFormatting();

builder.InsertCell();
builder.Write("Row 2, Col 1");

builder.InsertCell();
builder.Write("Row 2, Col 2");

builder.EndRow();

// Dikey metne uyacak şekilde satır yüksekliğini artırın.
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
* ad alanı [Aspose.Words.Tables](../../../aspose.words.tables/)
* toplantı [Aspose.Words](../../../)
