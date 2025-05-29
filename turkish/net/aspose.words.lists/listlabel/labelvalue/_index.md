---
title: ListLabel.LabelValue
linktitle: LabelValue
articleTitle: LabelValue
second_title: .NET için Aspose.Words
description: Etiketler için sayısal değerleri kolayca almak, veri yönetiminizi ve raporlama verimliliğinizi artırmak için ListLabel LabelValue özelliğini keşfedin.
type: docs
weight: 30
url: /tr/net/aspose.words.lists/listlabel/labelvalue/
---
## ListLabel.LabelValue property

Bu etiket için sayısal bir değer alır.

```csharp
public int LabelValue { get; }
```

## Notlar

Şunu kullanın:[`UpdateListLabels`](../../../aspose.words/document/updatelistlabels/) bu özelliğin değerini güncelleme yöntemi.

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

* class [ListLabel](../)
* ad alanı [Aspose.Words.Lists](../../../aspose.words.lists/)
* toplantı [Aspose.Words](../../../)
