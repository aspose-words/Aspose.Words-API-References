---
title: ListLabel Class
linktitle: ListLabel
articleTitle: ListLabel
second_title: .NET için Aspose.Words
description: Daha iyi kontrol ve sunum için özelleştirilebilir liste etiketi özellikleriyle belge biçimlendirmenizi geliştirmek üzere Aspose.Words.Lists.ListLabel sınıfını keşfedin.
type: docs
weight: 3940
url: /tr/net/aspose.words.lists/listlabel/
---
## ListLabel class

Bir liste etiketine özgü özellikleri tanımlar.

Daha fazla bilgi edinmek için şu adresi ziyaret edin:[Listelerle Çalışma](https://docs.aspose.com/words/net/working-with-lists/) belgeleme makalesi.

```csharp
public class ListLabel
```

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [Font](../../aspose.words.lists/listlabel/font/) { get; } | Liste etiketi yazı tipini alır. |
| [LabelString](../../aspose.words.lists/listlabel/labelstring/) { get; } | Liste etiketinin dize gösterimini alır. |
| [LabelValue](../../aspose.words.lists/listlabel/labelvalue/) { get; } | Bu etiket için sayısal bir değer alır. |

## Örnekler

Liste öğeleri olan tüm paragrafların liste etiketlerinin nasıl çıkarılacağını gösterir.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");
doc.UpdateListLabels();

NodeCollection paras = doc.GetChildNodes(NodeType.Paragraph, true);

// Paragraf listesine sahip olup olmadığımızı bul. Belgemizde, listemiz düz Arap rakamlarını kullanır,
// üçte başlayıp altıda biten.
foreach (Paragraph paragraph in paras.OfType<Paragraph>().Where(p => p.ListFormat.IsListItem).ToList())
{
    Console.WriteLine($"List item paragraph #{paras.IndexOf(paragraph)}");

    // Bu düğümü metin formatına dönüştürdüğümüzde elde edeceğimiz metin budur.
     // Bu metin çıktısı liste etiketlerini atlayacaktır. Paragraf biçimlendirme karakterlerini kırpın.
    string paragraphText = paragraph.ToString(SaveFormat.Text).Trim();
    Console.WriteLine($"\tExported Text: {paragraphText}");

    ListLabel label = paragraph.ListLabel;

    // Bu, listenin geçerli seviyesindeki paragrafın pozisyonunu alır. Birden fazla seviyeye sahip bir listemiz varsa,
    // bu bize o seviyedeki pozisyonunun ne olduğunu söyleyecektir.
    Console.WriteLine($"\tNumerical Id: {label.LabelValue}");

    // Çıktıdaki metinle birlikte liste etiketini eklemek için bunları birleştirin.
    Console.WriteLine($"\tList label combined with text: {label.LabelString} {paragraphText}");
}
```

### Ayrıca bakınız

* ad alanı [Aspose.Words.Lists](../../aspose.words.lists/)
* toplantı [Aspose.Words](../../)
