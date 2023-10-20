---
title: ListLabel.LabelValue
linktitle: LabelValue
articleTitle: LabelValue
second_title: Aspose.Words for .NET
description: ListLabel LabelValue mülk. Bu etiket için sayısal bir değer alır C#'da.
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

Kullan[`UpdateListLabels`](../../../aspose.words/document/updatelistlabels/) bu özelliğin değerini güncelleme yöntemi.

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

* class [ListLabel](../)
* ad alanı [Aspose.Words.Lists](../../../aspose.words.lists/)
* toplantı [Aspose.Words](../../../)
