---
title: ListLabel Class
linktitle: ListLabel
articleTitle: ListLabel
second_title: Aspose.Words for .NET
description: Aspose.Words.Lists.ListLabel sınıf. Liste etiketine özgü özellikleri tanımlar C#'da.
type: docs
weight: 3490
url: /tr/net/aspose.words.lists/listlabel/
---
## ListLabel class

Liste etiketine özgü özellikleri tanımlar.

Daha fazlasını öğrenmek için şu adresi ziyaret edin:[Listelerle Çalışmak](https://docs.aspose.com/words/net/working-with-lists/) dokümantasyon makalesi.

```csharp
public class ListLabel
```

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [Font](../../aspose.words.lists/listlabel/font/) { get; } | Liste etiketi yazı tipini alır. |
| [LabelString](../../aspose.words.lists/listlabel/labelstring/) { get; } | Liste etiketinin dize temsilini alır. |
| [LabelValue](../../aspose.words.lists/listlabel/labelvalue/) { get; } | Bu etiket için sayısal bir değer alır. |

## Örnekler

Liste öğesi olan tüm paragrafların liste etiketlerinin nasıl çıkarılacağını gösterir.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");
doc.UpdateListLabels();

NodeCollection paras = doc.GetChildNodes(NodeType.Paragraph, true);

//Paragraf listemizin olup olmadığını bulun. Belgemizde listemizde sade Arapça rakamlar kullanılıyor,
// üçte başlayıp altıda biten.
foreach (Paragraph paragraph in paras.OfType<Paragraph>().Where(p => p.ListFormat.IsListItem))
{
    Console.WriteLine($"List item paragraph #{paras.IndexOf(paragraph)}");

    // Bu düğümün çıktısını metin formatına aldığımızda elde ettiğimiz metin budur.
     // Bu metin çıktısı liste etiketlerini atlayacaktır. Paragraf biçimlendirme karakterlerini kırpın.
    string paragraphText = paragraph.ToString(SaveFormat.Text).Trim();
    Console.WriteLine($"\tExported Text: {paragraphText}");

    ListLabel label = paragraph.ListLabel;

    // Bu, paragrafın listenin geçerli düzeyindeki konumunu alır. Birden fazla düzeyden oluşan bir listemiz varsa,
    // bu bize o seviyede hangi konumda olduğunu söyleyecektir.
    Console.WriteLine($"\tNumerical Id: {label.LabelValue}");

    // Liste etiketini çıktıdaki metinle birlikte eklemek için bunları birleştirin.
    Console.WriteLine($"\tList label combined with text: {label.LabelString} {paragraphText}");
}
```

### Ayrıca bakınız

* ad alanı [Aspose.Words.Lists](../../aspose.words.lists/)
* toplantı [Aspose.Words](../../)
