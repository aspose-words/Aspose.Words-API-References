---
title: SdtListItemCollection.Add
linktitle: Add
articleTitle: Add
second_title: .NET için Aspose.Words
description: SdtListItemCollection Add yöntemiyle koleksiyonunuzu nasıl geliştireceğinizi keşfedin. Bugün zahmetsizce öğeler ekleyin ve veri yönetiminizi kolaylaştırın!
type: docs
weight: 40
url: /tr/net/aspose.words.markup/sdtlistitemcollection/add/
---
## SdtListItemCollection.Add method

Bu koleksiyona bir öğe ekler.

```csharp
public void Add(SdtListItem item)
```

## Örnekler

Açılır liste yapılandırılmış belge etiketleriyle nasıl çalışılacağını gösterir.

```csharp
Document doc = new Document();
StructuredDocumentTag tag = new StructuredDocumentTag(doc, SdtType.DropDownList, MarkupLevel.Block);
doc.FirstSection.Body.AppendChild(tag);

// Açılır liste yapılandırılmış belge etiketi, kullanıcının
// sol tıklayarak listeden bir seçenek seçin ve formu Microsoft Word'de açın.
// "ListItems" özelliği tüm liste öğelerini içerir ve her liste öğesi bir "SdtListItem"dır.
SdtListItemCollection listItems = tag.ListItems;
listItems.Add(new SdtListItem("Value 1"));

Assert.AreEqual(listItems[0].DisplayText, listItems[0].Value);

// 3 tane daha liste öğesi ekle. Bu öğeleri ilk öğeye göre farklı bir oluşturucu kullanarak başlat
// değerlerinden farklı olan dizeleri görüntülemek için.
listItems.Add(new SdtListItem("Item 2", "Value 2"));
listItems.Add(new SdtListItem("Item 3", "Value 3"));
listItems.Add(new SdtListItem("Item 4", "Value 4"));

Assert.AreEqual(4, listItems.Count);

// Açılır liste ilk öğeyi görüntülüyor. "SelectedValue" öğesini görüntülemek için ona farklı bir liste öğesi atayın.
listItems.SelectedValue = listItems[3];

Assert.AreEqual("Value 4", listItems.SelectedValue.Value);

// Koleksiyon üzerinde numaralandırma yap ve her bir elemanı yazdır.
using (IEnumerator<SdtListItem> enumerator = listItems.GetEnumerator())
{
    while (enumerator.MoveNext())
        if (enumerator.Current != null)
            Console.WriteLine($"List item: {enumerator.Current.DisplayText}, value: {enumerator.Current.Value}");
}

 // Son liste öğesini kaldır.
listItems.RemoveAt(3);

Assert.AreEqual(3, listItems.Count);

// Açılır kontrolümüz varsayılan olarak kaldırılan öğeyi görüntüleyecek şekilde ayarlandığından, mevcut bir öğeyi görüntüleyecek şekilde ayarlayın.
listItems.SelectedValue = listItems[1];

doc.Save(ArtifactsDir + "StructuredDocumentTag.ListItemCollection.docx");

// Tüm açılır öğe koleksiyonunu bir kerede boşaltmak için "Temizle" yöntemini kullanın.
listItems.Clear();

Assert.AreEqual(0, listItems.Count);
```

### Ayrıca bakınız

* class [SdtListItem](../../sdtlistitem/)
* class [SdtListItemCollection](../)
* ad alanı [Aspose.Words.Markup](../../../aspose.words.markup/)
* toplantı [Aspose.Words](../../../)
