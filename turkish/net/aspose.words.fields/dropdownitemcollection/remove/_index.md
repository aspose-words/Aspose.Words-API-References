---
title: DropDownItemCollection.Remove
linktitle: Remove
articleTitle: Remove
second_title: .NET için Aspose.Words
description: Sezgisel Remove metodumuzla DropDownItemCollection'ınızdan belirli değerleri zahmetsizce kaldırın. Veri yönetiminizi bugün kolaylaştırın!
type: docs
weight: 90
url: /tr/net/aspose.words.fields/dropdownitemcollection/remove/
---
## DropDownItemCollection.Remove method

Belirtilen değeri koleksiyondan kaldırır.

```csharp
public void Remove(string name)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| name | String | Kaldırılacak büyük/küçük harfe duyarlı değer. |

## Örnekler

Bir birleşik kutu alanının nasıl ekleneceğini ve öğe koleksiyonundaki öğelerin nasıl düzenleneceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Bir birleşik kutu ekleyin ve ardından açılır öğelerin koleksiyonunu doğrulayın.
// Microsoft Word'de kullanıcı birleşik kutuyu tıklayacaktır,
// ve ardından koleksiyondaki metin öğelerinden birini görüntülemek için seçin.
string[] items = { "One", "Two", "Three" };
FormField comboBoxField = builder.InsertComboBox("DropDown", items, 0);
DropDownItemCollection dropDownItems = comboBoxField.DropDownItems;

Assert.AreEqual(3, dropDownItems.Count);
Assert.AreEqual("One", dropDownItems[0]);
Assert.AreEqual(1, dropDownItems.IndexOf("Two"));
Assert.IsTrue(dropDownItems.Contains("Three"));

// Mevcut açılır kutu öğeleri koleksiyonuna yeni bir öğe eklemenin iki yolu vardır.
// 1 - Koleksiyonun sonuna bir öğe ekle:
dropDownItems.Add("Four");

// 2 - Belirtilen dizinde başka bir öğeden önce bir öğe ekle:
dropDownItems.Insert(3, "Three and a half");

Assert.AreEqual(5, dropDownItems.Count);

// Koleksiyon üzerinde yineleme yap ve her elemanı yazdır.
using (IEnumerator<string> dropDownCollectionEnumerator = dropDownItems.GetEnumerator())
    while (dropDownCollectionEnumerator.MoveNext())
        Console.WriteLine(dropDownCollectionEnumerator.Current);

// Açılır liste öğelerinden oluşan bir koleksiyondan öğeleri kaldırmanın iki yolu vardır.
// 1 - İçeriği geçirilen dizgeye eşit olan bir öğeyi kaldır:
dropDownItems.Remove("Four");

// 2 - Bir dizindeki bir öğeyi kaldır:
dropDownItems.RemoveAt(3);

Assert.AreEqual(3, dropDownItems.Count);
Assert.IsFalse(dropDownItems.Contains("Three and a half"));
Assert.IsFalse(dropDownItems.Contains("Four"));

doc.Save(ArtifactsDir + "FormFields.DropDownItemCollection.html");

// Açılır öğelerin tüm koleksiyonunu boşalt.
dropDownItems.Clear();
```

### Ayrıca bakınız

* class [DropDownItemCollection](../)
* ad alanı [Aspose.Words.Fields](../../../aspose.words.fields/)
* toplantı [Aspose.Words](../../../)
