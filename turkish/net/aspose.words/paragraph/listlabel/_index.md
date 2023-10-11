---
title: Paragraph.ListLabel
second_title: Aspose.Words for .NET API Referansı
description: Paragraph mülk. Bir alırListLabelbu paragraf için liste numaralandırma değerine ve formatlama ye erişim sağlayan nesne.
type: docs
weight: 160
url: /tr/net/aspose.words/paragraph/listlabel/
---
## Paragraph.ListLabel property

Bir alır`ListLabel`bu paragraf için liste numaralandırma değerine ve formatlama 'ye erişim sağlayan nesne.

```csharp
public ListLabel ListLabel { get; }
```

### Örnekler

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

* class [ListLabel](../../../aspose.words.lists/listlabel/)
* class [Paragraph](../)
* ad alanı [Aspose.Words](../../paragraph/)
* toplantı [Aspose.Words](../../../)


