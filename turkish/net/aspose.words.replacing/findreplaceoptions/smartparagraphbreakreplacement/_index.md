---
title: FindReplaceOptions.SmartParagraphBreakReplacement
linktitle: SmartParagraphBreakReplacement
articleTitle: SmartParagraphBreakReplacement
second_title: Aspose.Words for .NET
description: FindReplaceOptions SmartParagraphBreakReplacement mülk. Sonraki eş paragraf olmadığında break paragrafının değiştirilmesine izin verildiğini belirten bir boole değeri alır veya ayarlar C#'da.
type: docs
weight: 160
url: /tr/net/aspose.words.replacing/findreplaceoptions/smartparagraphbreakreplacement/
---
## FindReplaceOptions.SmartParagraphBreakReplacement property

Sonraki eş paragraf olmadığında break paragrafının değiştirilmesine izin verildiğini belirten bir boole değeri alır veya ayarlar.

Varsayılan değer:`YANLIŞ`.

```csharp
public bool SmartParagraphBreakReplacement { get; set; }
```

## Notlar

Bu seçenek, tüm alt düğümlerinin taşınabileceği bir sonraki kardeş paragraf olmadığında, paragraf değiştirildikten sonra herhangi bir sonraki paragrafı (kardeş olması gerekmez) bularak paragraf sonunun değiştirilmesine olanak tanır.

## Örnekler

İç içe tablo içeren bir tablo hücresinden paragrafın nasıl kaldırılacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// İlk hücrede paragraf ve iç tablo içeren tablo oluşturun.
builder.StartTable();
builder.InsertCell();
builder.Write("TEXT1");
builder.StartTable();
builder.InsertCell();
builder.EndTable();
builder.EndTable();
builder.Writeln();

FindReplaceOptions options = new FindReplaceOptions();
// Aşağıdaki seçenek 'true' olarak ayarlandığında Aspose.Words paragraf metnini kaldıracaktır
// paragraf işaretiyle tamamen. Aksi takdirde Aspose.Words, Word'ü taklit edecek ve kaldıracaktır.
// yalnızca paragrafın metni ve paragraf işaretini olduğu gibi bırakır (bir tablo metni takip ettiğinde).
options.SmartParagraphBreakReplacement = isSmartParagraphBreakReplacement;
doc.Range.Replace(new Regex(@"TEXT1&p"), "", options);

doc.Save(ArtifactsDir + "Table.RemoveParagraphTextAndMark.docx");
```

### Ayrıca bakınız

* class [FindReplaceOptions](../)
* ad alanı [Aspose.Words.Replacing](../../../aspose.words.replacing/)
* toplantı [Aspose.Words](../../../)
