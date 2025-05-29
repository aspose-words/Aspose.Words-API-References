---
title: Paragraph.ListLabel
linktitle: ListLabel
articleTitle: ListLabel
second_title: .NET için Aspose.Words
description: Paragraf ListLabel özelliğiyle liste numaralandırmasına erişin ve biçimlendirin. Belgenizin organizasyonunu ve netliğini zahmetsizce geliştirin!
type: docs
weight: 160
url: /tr/net/aspose.words/paragraph/listlabel/
---
## Paragraph.ListLabel property

Bir tane alır`ListLabel`Bu paragraf için liste numaralandırma değerine ve biçimlendirmeye erişim sağlayan nesne

```csharp
public ListLabel ListLabel { get; }
```

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

* class [ListLabel](../../../aspose.words.lists/listlabel/)
* class [Paragraph](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
