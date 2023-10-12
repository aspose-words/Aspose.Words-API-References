---
title: Enum LineNumberRestartMode
second_title: Aspose.Words for .NET API Referansı
description: Aspose.Words.LineNumberRestartMode Sıralama. Otomatik satır numaralandırmanın ne zaman yeniden başlayacağını belirler.
type: docs
weight: 3430
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
| RestartPage | `0` | Satır numaralandırma her sayfanın başında yeniden başlar. |
| RestartSection | `1` | Satır numaralandırma bölüm başlangıcında yeniden başlar. |
| Continuous | `2` | Önceki bölümden devam eden satır numaralandırma. |

### Örnekler

Bir bölüm için satır numaralandırmanın nasıl etkinleştirileceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Bölümün metin satırlarının solundaki sayıları görüntülemek için bölümün PageSetup nesnesini kullanabiliriz.
// Bu, List nesnesiyle aynı davranıştır,
// ancak bölümün tamamını kapsar ve metni hiçbir şekilde değiştirmez.
// Bölümümüz her yeni sayfada numaralandırmayı 1'den başlatacak ve numarayı gösterecektir,
// 3'ün katı ise satırın solunda 50 punto.
PageSetup pageSetup = builder.PageSetup;
pageSetup.LineStartingNumber = 1;
pageSetup.LineNumberCountBy = 3;
pageSetup.LineNumberRestartMode = LineNumberRestartMode.RestartPage;
pageSetup.LineNumberDistanceFromText = 50.0d;

for (int i = 1; i <= 25; i++)
    builder.Writeln($"Line {i}.");

// Satır sayacı, "SuppressLineNumbers" bayrağı "true" olarak ayarlanmış olan herhangi bir paragrafı atlayacaktır.
// Bu paragraf 3'ün katı olan 15. satırdadır ve bu nedenle normalde bir satır numarası görüntüler.
// Bölümün satır sayacı da bu satırı göz ardı edecek, sonraki satırı 15'inci satır olarak değerlendirecek,
// ve bu noktadan itibaren saymaya devam edin.
doc.FirstSection.Body.Paragraphs[14].ParagraphFormat.SuppressLineNumbers = true;

doc.Save(ArtifactsDir + "PageSetup.LineNumbers.docx");
```

### Ayrıca bakınız

* class [PageSetup](../pagesetup/)
* property [LineNumberRestartMode](../pagesetup/linenumberrestartmode/)
* ad alanı [Aspose.Words](../../aspose.words/)
* toplantı [Aspose.Words](../../)


