---
title: Document.UpdateListLabels
linktitle: UpdateListLabels
articleTitle: UpdateListLabels
second_title: Aspose.Words for .NET
description: Document UpdateListLabels yöntem. Belgedeki tüm liste öğeleri için liste etiketlerini günceller C#'da.
type: docs
weight: 760
url: /tr/net/aspose.words/document/updatelistlabels/
---
## Document.UpdateListLabels method

Belgedeki tüm liste öğeleri için liste etiketlerini günceller.

```csharp
public void UpdateListLabels()
```

## Notlar

Bu yöntem, aşağıdakiler gibi liste etiketi özelliklerini günceller:[`LabelValue`](../../../aspose.words.lists/listlabel/labelvalue/) ve [`LabelString`](../../../aspose.words.lists/listlabel/labelstring/) her biri için[`ListLabel`](../../paragraph/listlabel/)belgedeki nesne.

Ayrıca bu yöntem bazen belgedeki alanlar güncellenirken dolaylı olarak çağrılır. Bu, gerekli 'dir çünkü liste numaralarına referans verebilecek bazı alanların (TOC veya REF gibi) güncel olması gerekir.

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

* class [Document](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
