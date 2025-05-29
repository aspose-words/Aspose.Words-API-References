---
title: ParagraphFormat.SuppressLineNumbers
linktitle: SuppressLineNumbers
articleTitle: SuppressLineNumbers
second_title: .NET için Aspose.Words
description: ParagraphFormat SuppressLineNumbers özelliğinin paragraflar için satır numaralandırmayı nasıl özelleştirebileceğinizi, belge netliğini ve organizasyonunu nasıl geliştirebileceğinizi keşfedin.
type: docs
weight: 390
url: /tr/net/aspose.words/paragraphformat/suppresslinenumbers/
---
## ParagraphFormat.SuppressLineNumbers property

Geçerli paragrafın satırlarının, üst bölümde uygulanan satır numaralandırmasından muaf tutulup tutulmayacağını belirtir.

```csharp
public bool SuppressLineNumbers { get; set; }
```

## Örnekler

Bir bölüm için satır numaralandırmanın nasıl etkinleştirileceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Bölümün PageSetup nesnesini kullanarak bölümün metin satırlarının solunda sayıları görüntüleyebiliriz.
// Bu, bir Liste nesnesiyle aynı davranıştır,
// ancak bölümün tamamını kapsıyor ve metni hiçbir şekilde değiştirmiyor.
// Bölümümüz her yeni sayfada numaralandırmayı 1'den yeniden başlatacak ve numarayı görüntüleyecektir,
// 3'ün katı ise satırın solunda 50pt.
PageSetup pageSetup = builder.PageSetup;
pageSetup.LineStartingNumber = 1;
pageSetup.LineNumberCountBy = 3;
pageSetup.LineNumberRestartMode = LineNumberRestartMode.RestartPage;
pageSetup.LineNumberDistanceFromText = 50.0d;

for (int i = 1; i <= 25; i++)
    builder.Writeln($"Line {i}.");

// Satır sayacı, "SuppressLineNumbers" bayrağı "true" olarak ayarlandığında herhangi bir paragrafı atlayacaktır.
// Bu paragraf 15. satırdadır, yani 3'ün katıdır ve bu nedenle normalde satır numarası gösterilmelidir.
// Bölümün satır sayacı da bu satırı yoksayacak, bir sonraki satırı 15. satır olarak değerlendirecek,
// ve saymaya o noktadan itibaren devam edilir.
doc.FirstSection.Body.Paragraphs[14].ParagraphFormat.SuppressLineNumbers = true;

doc.Save(ArtifactsDir + "PageSetup.LineNumbers.docx");
```

### Ayrıca bakınız

* class [ParagraphFormat](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
