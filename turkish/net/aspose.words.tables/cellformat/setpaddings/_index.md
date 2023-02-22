---
title: CellFormat.SetPaddings
second_title: Aspose.Words for .NET API Referansı
description: CellFormat yöntem. Hücre içeriğinin soluna/üstüne/sağına/altına eklenecek boşluk miktarını puan olarak ayarlar.
type: docs
weight: 160
url: /tr/net/aspose.words.tables/cellformat/setpaddings/
---
## CellFormat.SetPaddings method

Hücre içeriğinin soluna/üstüne/sağına/altına eklenecek boşluk miktarını (puan olarak) ayarlar.

```csharp
public void SetPaddings(double leftPadding, double topPadding, double rightPadding, 
    double bottomPadding)
```

### Örnekler

Bir hücrenin içeriğinin boşlukla nasıl doldurulacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Kenarlık ve metin içeriği arasında bir dolgu mesafesi (nokta olarak) ayarlayın
// belge oluşturucu ile oluşturduğumuz her tablo hücresinin. 
builder.CellFormat.SetPaddings(5, 10, 40, 50);

// İçeriğinde boşluk dolgusu olacak bir hücreli bir tablo oluşturun.
builder.StartTable();
builder.InsertCell();
builder.Write("Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. " +
              "Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.");

doc.Save(ArtifactsDir + "CellFormat.Padding.docx");
```

### Ayrıca bakınız

* class [CellFormat](../)
* ad alanı [Aspose.Words.Tables](../../cellformat/)
* toplantı [Aspose.Words](../../../)


