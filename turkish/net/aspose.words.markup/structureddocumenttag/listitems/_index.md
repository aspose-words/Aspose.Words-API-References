---
title: StructuredDocumentTag.ListItems
linktitle: ListItems
articleTitle: ListItems
second_title: Aspose.Words for .NET
description: StructuredDocumentTag ListItems mülk. AlırSdtListItemCollection bununla ilişkiliSDT  C#'da.
type: docs
weight: 180
url: /tr/net/aspose.words.markup/structureddocumenttag/listitems/
---
## StructuredDocumentTag.ListItems property

Alır[`SdtListItemCollection`](../../sdtlistitemcollection/) bununla ilişkili**SDT** .

```csharp
public SdtListItemCollection ListItems { get; }
```

## Notlar

Bu özelliğe erişim yalnızca şunun için işe yarayacaktır:ComboBox veyaDropDownList SDT türleri.

Diğer tüm SDT türleri için istisna meydana gelecektir.

## Örnekler

Açılır liste yapılandırılmış belge etiketleriyle nasıl çalışılacağını gösterir.

```csharp
Document doc = new Document();
StructuredDocumentTag tag = new StructuredDocumentTag(doc, SdtType.DropDownList, MarkupLevel.Block);
doc.FirstSection.Body.AppendChild(tag);

// Açılır liste yapılandırılmış belge etiketi, kullanıcının şunları yapmasına olanak tanıyan bir formdur
// sol tıklayıp formu Microsoft Word'de açarak listeden bir seçenek seçin.
// "ListItems" özelliği tüm liste öğelerini içerir ve her liste öğesi bir "SdtListItem"dir.
SdtListItemCollection listItems = tag.ListItems;
listItems.Add(new SdtListItem("Value 1"));

Assert.AreEqual(listItems[0].DisplayText, listItems[0].Value);

// 3 liste öğesi daha ekleyin. Bu öğeleri ilk öğeden farklı bir kurucu kullanarak başlat
// değerlerinden farklı olan dizeleri görüntülemek için.
listItems.Add(new SdtListItem("Item 2", "Value 2"));
listItems.Add(new SdtListItem("Item 3", "Value 3"));
listItems.Add(new SdtListItem("Item 4", "Value 4"));

Assert.AreEqual(4, listItems.Count);

// Açılır liste ilk öğeyi gösteriyor. Görüntülemek için "SeçiliDeğer"e farklı bir liste öğesi atayın.
listItems.SelectedValue = listItems[3];

Assert.AreEqual("Value 4", listItems.SelectedValue.Value);

// Koleksiyonun üzerinde numaralandırın ve her öğeyi yazdırın.
using (IEnumerator<SdtListItem> enumerator = listItems.GetEnumerator())
{
    while (enumerator.MoveNext())
        if (enumerator.Current != null)
            Console.WriteLine($"List item: {enumerator.Current.DisplayText}, value: {enumerator.Current.Value}");
}

 // Listedeki son öğeyi kaldır.
listItems.RemoveAt(3);

Assert.AreEqual(3, listItems.Count);

// Açılır kontrolümüz varsayılan olarak kaldırılan öğeyi görüntüleyecek şekilde ayarlandığından, ona mevcut olanı görüntüleyecek bir öğe verin.
listItems.SelectedValue = listItems[1];

doc.Save(ArtifactsDir + "StructuredDocumentTag.ListItemCollection.docx");

// Açılan öğe koleksiyonunun tamamını bir kerede boşaltmak için "Temizle" yöntemini kullanın.
listItems.Clear();

Assert.AreEqual(0, listItems.Count);
```

### Ayrıca bakınız

* class [SdtListItemCollection](../../sdtlistitemcollection/)
* class [StructuredDocumentTag](../)
* ad alanı [Aspose.Words.Markup](../../../aspose.words.markup/)
* toplantı [Aspose.Words](../../../)
