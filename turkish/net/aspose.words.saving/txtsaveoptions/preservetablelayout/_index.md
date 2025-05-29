---
title: TxtSaveOptions.PreserveTableLayout
linktitle: PreserveTableLayout
articleTitle: PreserveTableLayout
second_title: .NET için Aspose.Words
description: TxtSaveOptions'ın PreserveTableLayout özelliğini keşfedin, tablolarınızın düz metin olarak kaydedildiğinde düzenlerini korumasını sağlayın. Belgenizin okunabilirliğini artırın!
type: docs
weight: 50
url: /tr/net/aspose.words.saving/txtsaveoptions/preservetablelayout/
---
## TxtSaveOptions.PreserveTableLayout property

Programın düz metin biçiminde kaydederken tabloların düzenini korumaya çalışıp çalışmayacağını belirtir. Varsayılan değer`YANLIŞ` .

```csharp
public bool PreserveTableLayout { get; set; }
```

## Örnekler

Düz metne dönüştürülürken tabloların düzeninin nasıl korunacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.StartTable();
builder.InsertCell();
builder.Write("Row 1, cell 1");
builder.InsertCell();
builder.Write("Row 1, cell 2");
builder.EndRow();
builder.InsertCell();
builder.Write("Row 2, cell 1");
builder.InsertCell();
builder.Write("Row 2, cell 2");
builder.EndTable();

// Belgenin "Kaydet" metoduna geçirebileceğimiz bir "TxtSaveOptions" nesnesi oluşturun
// Belgeyi düz metne nasıl kaydedeceğimizi değiştirmek için.
TxtSaveOptions txtSaveOptions = new TxtSaveOptions();

// İçeriğe boşluk dolgusu uygulamak için "PreserveTableLayout" özelliğini "true" olarak ayarlayın
// Tablonun düzenini mümkün olduğunca korumak için çıktı düz metin belgesinin.
// Tüm tabloların içeriklerini kaydetmek için "PreserveTableLayout" özelliğini "false" olarak ayarlayın
// her satır için yeni bir satır olacak şekilde, sürekli bir metin gövdesi olarak.
txtSaveOptions.PreserveTableLayout = preserveTableLayout;

doc.Save(ArtifactsDir + "TxtSaveOptions.PreserveTableLayout.txt", txtSaveOptions);

string docText = File.ReadAllText(ArtifactsDir + "TxtSaveOptions.PreserveTableLayout.txt");

if (preserveTableLayout)
    Assert.AreEqual("Row 1, cell 1                                            Row 1, cell 2\r\n" +
                    "Row 2, cell 1                                            Row 2, cell 2\r\n\r\n", docText);
else
    Assert.AreEqual("Row 1, cell 1\r" +
                    "Row 1, cell 2\r" +
                    "Row 2, cell 1\r" +
                    "Row 2, cell 2\r\r\n", docText);
```

### Ayrıca bakınız

* class [TxtSaveOptions](../)
* ad alanı [Aspose.Words.Saving](../../../aspose.words.saving/)
* toplantı [Aspose.Words](../../../)
