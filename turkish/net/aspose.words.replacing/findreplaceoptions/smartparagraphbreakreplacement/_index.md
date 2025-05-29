---
title: FindReplaceOptions.SmartParagraphBreakReplacement
linktitle: SmartParagraphBreakReplacement
articleTitle: SmartParagraphBreakReplacement
second_title: .NET için Aspose.Words
description: FindReplaceOptions'daki SmartParagraphBreakReplacement özelliğini keşfedin. Sorunsuz metin biçimlendirmesi için paragraf sonlarını zahmetsizce kontrol edin.
type: docs
weight: 170
url: /tr/net/aspose.words.replacing/findreplaceoptions/smartparagraphbreakreplacement/
---
## FindReplaceOptions.SmartParagraphBreakReplacement property

Sonraki kardeş paragraf olmadığında paragraf break 'nin değiştirilmesine izin verilip verilmediğini belirten bir Boole değeri alır veya ayarlar.

Varsayılan değer:`YANLIŞ`.

```csharp
public bool SmartParagraphBreakReplacement { get; set; }
```

## Notlar

Bu seçenek, tüm child düğümlerinin taşınabileceği bir sonraki kardeş paragraf olmadığında, değiştirilen paragraftan sonraki herhangi bir (mutlaka kardeş olması gerekmeyen) sonraki paragrafı bularak paragraf sonunu değiştirmeye olanak tanır.

## Örnekler

İç içe geçmiş bir tabloda tablo hücresinden paragrafın nasıl kaldırılacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// İlk hücrede paragraf ve iç tablo içeren tabloyu oluştur.
builder.StartTable();
builder.InsertCell();
builder.Write("TEXT1");
builder.StartTable();
builder.InsertCell();
builder.EndTable();
builder.EndTable();
builder.Writeln();

FindReplaceOptions options = new FindReplaceOptions();
// Aşağıdaki seçenek 'true' olarak ayarlandığında, Aspose.Words paragrafın metnini kaldıracaktır
// paragraf işaretiyle tamamen. Aksi takdirde, Aspose.Words Word'ü taklit edecek ve kaldıracaktır
// sadece paragrafın metni ve paragraf işaretini olduğu gibi bırakır (metnin ardından tablo geldiğinde).
options.SmartParagraphBreakReplacement = isSmartParagraphBreakReplacement;
doc.Range.Replace(new Regex(@"TEXT1&p"), "", options);

doc.Save(ArtifactsDir + "Table.RemoveParagraphTextAndMark.docx");
```

### Ayrıca bakınız

* class [FindReplaceOptions](../)
* ad alanı [Aspose.Words.Replacing](../../../aspose.words.replacing/)
* toplantı [Aspose.Words](../../../)
