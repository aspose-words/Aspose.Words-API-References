---
title: TxtSaveOptions.PreserveTableLayout
second_title: Aspose.Words for .NET API Referansı
description: TxtSaveOptions mülk. Programın düz metin biçiminde kaydederken tabloların düzenini korumaya çalışıp çalışmayacağını belirtir. Varsayılan değer yanlış .
type: docs
weight: 50
url: /tr/net/aspose.words.saving/txtsaveoptions/preservetablelayout/
---
## TxtSaveOptions.PreserveTableLayout property

Programın düz metin biçiminde kaydederken tabloların düzenini korumaya çalışıp çalışmayacağını belirtir. Varsayılan değer **yanlış** .

```csharp
public bool PreserveTableLayout { get; set; }
```

### Örnekler

Düz metne dönüştürürken tablo düzeninin nasıl korunacağını gösterir.

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

// Belgenin "Kaydet" yöntemine aktarabileceğimiz bir "TxtSaveOptions" nesnesi oluşturun
// belgeyi düz metne kaydetme şeklimizi değiştirmek için.
TxtSaveOptions txtSaveOptions = new TxtSaveOptions();

// İçeriğe boşluk dolgusu uygulamak için "PreserveTableLayout" özelliğini "true" olarak ayarlayın
// tablo düzeninin mümkün olduğunca çoğunu korumak için çıktı düz metin belgesinin.
// Tüm tabloların içeriğini kaydetmek için "PreserveTableLayout" özelliğini "false" olarak ayarlayın
// her satır için yalnızca yeni bir satırla, sürekli bir metin gövdesi olarak.
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
* ad alanı [Aspose.Words.Saving](../../txtsaveoptions/)
* toplantı [Aspose.Words](../../../)


