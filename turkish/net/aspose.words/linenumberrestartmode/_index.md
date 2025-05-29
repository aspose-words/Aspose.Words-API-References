---
title: LineNumberRestartMode Enum
linktitle: LineNumberRestartMode
articleTitle: LineNumberRestartMode
second_title: .NET için Aspose.Words
description: Gelişmiş belge biçimlendirmesi ve netliği için otomatik satır numaralandırma sıfırlamalarını kontrol etmek üzere Aspose.Words.LineNumberRestartMode enum'unu keşfedin.
type: docs
weight: 3880
url: /tr/net/aspose.words/linenumberrestartmode/
---
## LineNumberRestartMode enumeration

Otomatik satır numaralandırmanın ne zaman yeniden başlayacağını belirler.

```csharp
public enum LineNumberRestartMode
```

### değerler

| İsim | Değer | Tanım |
| --- | --- | --- |
| RestartPage | `0` | Satır numaralandırması her sayfanın başında yeniden başlar. |
| RestartSection | `1` | Satır numaralandırması bölüm başlangıcında yeniden başlar. |
| Continuous | `2` | Satır numaralandırması önceki bölümden devam ediyor. |

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

* class [PageSetup](../pagesetup/)
* property [LineNumberRestartMode](../pagesetup/linenumberrestartmode/)
* ad alanı [Aspose.Words](../../aspose.words/)
* toplantı [Aspose.Words](../../)
