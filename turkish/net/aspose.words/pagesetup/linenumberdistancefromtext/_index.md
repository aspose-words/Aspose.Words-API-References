---
title: PageSetup.LineNumberDistanceFromText
linktitle: LineNumberDistanceFromText
articleTitle: LineNumberDistanceFromText
second_title: .NET için Aspose.Words
description: Satır numaraları ile belgenizin metni arasındaki boşluğu kolayca ayarlayarak okunabilirliği artırmak için PageSetup LineNumberDistanceFromText özelliğini keşfedin.
type: docs
weight: 220
url: /tr/net/aspose.words/pagesetup/linenumberdistancefromtext/
---
## PageSetup.LineNumberDistanceFromText property

Satır numaralarının sağ kenarı ile belgenin sol kenarı arasındaki mesafeyi alır veya ayarlar.

```csharp
public double LineNumberDistanceFromText { get; set; }
```

## Notlar

Belgenin satır numaraları ile metni arasındaki mesafeyi otomatik olarak sıfırlamak için bu özelliği sıfıra ayarlayın.

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

* class [PageSetup](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
