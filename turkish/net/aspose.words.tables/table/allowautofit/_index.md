---
title: Table.AllowAutoFit
second_title: Aspose.Words for .NET API Referansı
description: Table mülk. Microsoft Word ve Aspose.Wordsün tablodaki hücreleri içeriklerine uyacak şekilde otomatik olarak yeniden boyutlandırmasına olanak tanır.
type: docs
weight: 50
url: /tr/net/aspose.words.tables/table/allowautofit/
---
## Table.AllowAutoFit property

Microsoft Word ve Aspose.Words'ün tablodaki hücreleri içeriklerine uyacak şekilde otomatik olarak yeniden boyutlandırmasına olanak tanır.

```csharp
public bool AllowAutoFit { get; set; }
```

### Notlar

Varsayılan değer:`doğru`.

### Örnekler

Otomatik tablo hücresi yeniden boyutlandırmanın nasıl etkinleştirileceğini/devre dışı bırakılacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Table table = builder.StartTable();
builder.InsertCell();
builder.CellFormat.PreferredWidth = PreferredWidth.FromPoints(100);
builder.Write("Lorem ipsum dolor sit amet, consectetur adipiscing elit, " +
              "sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

builder.InsertCell();
builder.CellFormat.PreferredWidth = PreferredWidth.Auto;
builder.Write("Lorem ipsum dolor sit amet, consectetur adipiscing elit, " +
              "sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");
builder.EndRow();
builder.EndTable();

// Tablonun boyutları korumasını sağlamak için "AllowAutoFit" özelliğini "false" olarak ayarlayın
// tüm satır ve hücrelerini ayır ve sığamayacak kadar büyürlerse içerikleri kes.
// Tablonun hücrelerinin genişliğini ve yüksekliğini değiştirmesine izin vermek için "AllowAutoFit" özelliğini "true" olarak ayarlayın
// içeriklerini barındırmak için.
table.AllowAutoFit = allowAutoFit;

doc.Save(ArtifactsDir + "Table.AllowAutoFitOnTable.html");
```

### Ayrıca bakınız

* class [Table](../)
* ad alanı [Aspose.Words.Tables](../../table/)
* toplantı [Aspose.Words](../../../)


