---
title: Document.UpdateListLabels
linktitle: UpdateListLabels
articleTitle: UpdateListLabels
second_title: .NET için Aspose.Words
description: Belgenizdeki tüm liste öğesi etiketlerini UpdateListLabels yöntemi ile zahmetsizce güncelleyin, böylece içeriğinizde tutarlılık ve netlik sağlayın.
type: docs
weight: 820
url: /tr/net/aspose.words/document/updatelistlabels/
---
## Document.UpdateListLabels method

Belgedeki tüm liste öğelerinin liste etiketlerini günceller.

```csharp
public void UpdateListLabels()
```

## Notlar

Bu yöntem, aşağıdaki gibi liste etiketi özelliklerini günceller:[`LabelValue`](../../../aspose.words.lists/listlabel/labelvalue/) ve [`LabelString`](../../../aspose.words.lists/listlabel/labelstring/) her biri için[`ListLabel`](../../paragraph/listlabel/) Belgedeki nesne.

Ayrıca, bu yöntem bazen belgedeki alanlar güncellenirken örtük olarak çağrılır. Bu, liste numaralarına (örneğin TOC veya REF) başvurabilen bazı alanların güncel olmaları gerektiğinden required 'dir.

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

* class [Document](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
