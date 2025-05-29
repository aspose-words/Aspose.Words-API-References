---
title: SdtListItem.Value
linktitle: Value
articleTitle: Value
second_title: .NET için Aspose.Words
description: Uygulamalarınızda gelişmiş veri işleme için liste öğesi değerlerine kolayca erişmek ve bunları yönetmek amacıyla SdtListItem Değer özelliğini keşfedin.
type: docs
weight: 30
url: /tr/net/aspose.words.markup/sdtlistitem/value/
---
## SdtListItem.Value property

Bu liste öğesinin değerini alır.

```csharp
public string Value { get; }
```

## Notlar

Olamaz`hükümsüz` ve boş bir dize olamaz.

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

* class [SdtListItem](../)
* ad alanı [Aspose.Words.Markup](../../../aspose.words.markup/)
* toplantı [Aspose.Words](../../../)
