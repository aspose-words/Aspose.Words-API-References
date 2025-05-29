---
title: SdtListItemCollection Class
linktitle: SdtListItemCollection
articleTitle: SdtListItemCollection
second_title: .NET için Aspose.Words
description: Sorunsuz SdtListItem öğelerine erişim için Aspose.Words.Markup.SdtListItemCollection sınıfını keşfedin ve yapılandırılmış belge yönetimini zahmetsizce geliştirin.
type: docs
weight: 4720
url: /tr/net/aspose.words.markup/sdtlistitemcollection/
---
## SdtListItemCollection class

Şuna erişim sağlar:[`SdtListItem`](../sdtlistitem/) yapılandırılmış bir belge etiketinin öğeleri.

Daha fazla bilgi edinmek için şu adresi ziyaret edin:[Yapılandırılmış Belge Etiketleri veya İçerik Denetimi](https://docs.aspose.com/words/net/working-with-content-control-sdt/) belgeleme makalesi.

```csharp
public class SdtListItemCollection : IEnumerable<SdtListItem>
```

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [Count](../../aspose.words.markup/sdtlistitemcollection/count/) { get; } | Koleksiyondaki öğelerin sayısını alır. |
| [Item](../../aspose.words.markup/sdtlistitemcollection/item/) { get; } | Bir[`SdtListItem`](../sdtlistitem/) koleksiyondaki sıfır tabanlı indeksi verilen nesne. |
| [SelectedValue](../../aspose.words.markup/sdtlistitemcollection/selectedvalue/) { get; set; } | Bu listede şu anda seçili değeri belirtir. Boş değere izin verilir, yani şu anda seçili bir girdi bu liste öğesi koleksiyonuyla ilişkilendirilmemiştir. |

## yöntemler

| İsim | Tanım |
| --- | --- |
| [Add](../../aspose.words.markup/sdtlistitemcollection/add/)(*[SdtListItem](../sdtlistitem/)*) | Bu koleksiyona bir öğe ekler. |
| [Clear](../../aspose.words.markup/sdtlistitemcollection/clear/)() | Bu koleksiyondaki tüm öğeleri temizler. |
| [GetEnumerator](../../aspose.words.markup/sdtlistitemcollection/getenumerator/)() | Koleksiyondaki tüm öğeler üzerinde yineleme yapmak için kullanılabilen bir numaratör nesnesi döndürür. |
| [RemoveAt](../../aspose.words.markup/sdtlistitemcollection/removeat/)(*int*) | Belirtilen dizindeki bir liste öğesini kaldırır. |

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

* class [SdtListItem](../sdtlistitem/)
* ad alanı [Aspose.Words.Markup](../../aspose.words.markup/)
* toplantı [Aspose.Words](../../)
