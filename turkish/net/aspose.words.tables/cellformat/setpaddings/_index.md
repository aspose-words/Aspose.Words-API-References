---
title: CellFormat.SetPaddings
linktitle: SetPaddings
articleTitle: SetPaddings
second_title: .NET için Aspose.Words
description: Hücre aralıklarını noktalar halinde özelleştirmek, okunabilirliği ve tasarımı geliştirmek için CellFormat SetPaddings yöntemini keşfedin.
type: docs
weight: 170
url: /tr/net/aspose.words.tables/cellformat/setpaddings/
---
## CellFormat.SetPaddings method

Hücrenin içeriğinin soluna/üstüne/sağına/altına eklenecek boşluk miktarını (nokta cinsinden) ayarlar.

```csharp
public void SetPaddings(double leftPadding, double topPadding, double rightPadding, 
    double bottomPadding)
```

## Örnekler

Bir hücrenin içeriğinin boşluklarla nasıl doldurulacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Sınır ile metin içeriği arasında bir dolgu mesafesi (nokta cinsinden) ayarlayın
 // Belge oluşturucu ile oluşturduğumuz her tablo hücresinin.
builder.CellFormat.SetPaddings(5, 10, 40, 50);

// İçeriği boşluklarla doldurulacak tek hücreli bir tablo oluşturun.
builder.StartTable();
builder.InsertCell();
builder.Write("Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. " +
              "Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.");

doc.Save(ArtifactsDir + "CellFormat.Padding.docx");
```

### Ayrıca bakınız

* class [CellFormat](../)
* ad alanı [Aspose.Words.Tables](../../../aspose.words.tables/)
* toplantı [Aspose.Words](../../../)
