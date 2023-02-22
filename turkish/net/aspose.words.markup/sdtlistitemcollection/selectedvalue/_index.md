---
title: SdtListItemCollection.SelectedValue
second_title: Aspose.Words for .NET API Referansı
description: SdtListItemCollection mülk. Bu listede şu anda seçili değeri belirtir. Boş değere izin verilir bu şu anda seçili olan hiçbir girişin bu liste öğesi koleksiyonuyla ilişkilendirilmediği anlamına gelir.
type: docs
weight: 30
url: /tr/net/aspose.words.markup/sdtlistitemcollection/selectedvalue/
---
## SdtListItemCollection.SelectedValue property

Bu listede şu anda seçili değeri belirtir. Boş değere izin verilir, bu, şu anda seçili olan hiçbir girişin bu liste öğesi koleksiyonuyla ilişkilendirilmediği anlamına gelir.

```csharp
public SdtListItem SelectedValue { get; set; }
```

### Örnekler

Açılır liste yapılandırılmış belge etiketleriyle nasıl çalışılacağını gösterir.

```csharp
Document doc = new Document();
StructuredDocumentTag tag = new StructuredDocumentTag(doc, SdtType.DropDownList, MarkupLevel.Block);
doc.FirstSection.Body.AppendChild(tag);

// Açılır liste yapılandırılmış belge etiketi, kullanıcının
// sol tıklayarak ve formu Microsoft Word'de açarak listeden bir seçenek seçin.
// "ListItems" özelliği tüm liste öğelerini içerir ve her liste öğesi bir "SdtListItem"dir.
SdtListItemCollection listItems = tag.ListItems;
listItems.Add(new SdtListItem("Value 1"));

Assert.AreEqual(listItems[0].DisplayText, listItems[0].Value);

// 3 liste öğesi daha ekleyin. İlk öğeden farklı bir kurucu kullanarak bu öğeleri başlat
// değerlerinden farklı dizeleri görüntülemek için.
listItems.Add(new SdtListItem("Item 2", "Value 2"));
listItems.Add(new SdtListItem("Item 3", "Value 3"));
listItems.Add(new SdtListItem("Item 4", "Value 4"));

Assert.AreEqual(4, listItems.Count);

// Açılır liste ilk öğeyi gösteriyor. Görüntülemek için "SelectedValue" öğesine farklı bir liste öğesi atayın.
listItems.SelectedValue = listItems[3];

Assert.AreEqual("Value 4", listItems.SelectedValue.Value);

// Koleksiyon üzerinde numaralandırın ve her bir elemanı yazdırın.
using (IEnumerator<SdtListItem> enumerator = listItems.GetEnumerator())
{
    while (enumerator.MoveNext())
        if (enumerator.Current != null)
            Console.WriteLine($"List item: {enumerator.Current.DisplayText}, value: {enumerator.Current.Value}");
}

 // Son liste öğesini kaldırın.
listItems.RemoveAt(3);

Assert.AreEqual(3, listItems.Count);

// Açılır kontrolümüz varsayılan olarak kaldırılan öğeyi gösterecek şekilde ayarlandığından, ona var olan bir öğeyi göster.
listItems.SelectedValue = listItems[1];

doc.Save(ArtifactsDir + "StructuredDocumentTag.ListItemCollection.docx");

// Açılan öğe koleksiyonunun tamamını bir kerede boşaltmak için "Temizle" yöntemini kullanın.
listItems.Clear();

Assert.AreEqual(0, listItems.Count);
```

### Ayrıca bakınız

* class [SdtListItem](../../sdtlistitem/)
* class [SdtListItemCollection](../)
* ad alanı [Aspose.Words.Markup](../../sdtlistitemcollection/)
* toplantı [Aspose.Words](../../../)


