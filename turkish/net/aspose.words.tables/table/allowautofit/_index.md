---
title: Table.AllowAutoFit
linktitle: AllowAutoFit
articleTitle: AllowAutoFit
second_title: .NET için Aspose.Words
description: Microsoft Word ve Aspose.Words tablo hücrelerinin boyutunu zahmetsizce değiştirmek için Table AllowAutoFit özelliğini keşfedin, böylece belgenizin okunabilirliğini ve sunumunu geliştirin.
type: docs
weight: 50
url: /tr/net/aspose.words.tables/table/allowautofit/
---
## Table.AllowAutoFit property

Microsoft Word ve Aspose.Words'ün bir tabloda hücrelerin boyutunu içeriğe uyacak şekilde otomatik olarak değiştirmesine olanak tanır.

```csharp
public bool AllowAutoFit { get; set; }
```

## Notlar

Varsayılan değer:`doğru`.

## Örnekler

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

// Tablonun boyutlarını koruması için "AllowAutoFit" özelliğini "false" olarak ayarlayın
// tüm satır ve hücrelerinin içeriğini, eğer içerik sığmayacak kadar büyük olursa keser.
// Tablonun hücrelerinin genişliğini ve yüksekliğini değiştirmesine izin vermek için "AllowAutoFit" özelliğini "true" olarak ayarlayın
// içeriklerini barındırmak için.
table.AllowAutoFit = allowAutoFit;

doc.Save(ArtifactsDir + "Table.AllowAutoFitOnTable.html");
```

### Ayrıca bakınız

* class [Table](../)
* ad alanı [Aspose.Words.Tables](../../../aspose.words.tables/)
* toplantı [Aspose.Words](../../../)
