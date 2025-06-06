---
title: DropDownItemCollection Class
linktitle: DropDownItemCollection
articleTitle: DropDownItemCollection
second_title: .NET için Aspose.Words
description: Aspose.Words.Fields.DropDownItemCollection sınıfını keşfedin; form alanlarındaki açılır öğeleri zahmetsizce yönetmek için başvuracağınız çözüm!
type: docs
weight: 1910
url: /tr/net/aspose.words.fields/dropdownitemcollection/
---
## DropDownItemCollection class

Bir açılır form alanındaki tüm öğeleri temsil eden dizelerin bir koleksiyonu.

Daha fazla bilgi edinmek için şu adresi ziyaret edin:[Alanlarla Çalışma](https://docs.aspose.com/words/net/working-with-fields/) belgeleme makalesi.

```csharp
public class DropDownItemCollection : IEnumerable<string>
```

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [Count](../../aspose.words.fields/dropdownitemcollection/count/) { get; } | Koleksiyonda bulunan öğelerin sayısını alır. |
| [Item](../../aspose.words.fields/dropdownitemcollection/item/) { get; set; } | Belirtilen dizindeki öğeyi alır veya ayarlar. |

## yöntemler

| İsim | Tanım |
| --- | --- |
| [Add](../../aspose.words.fields/dropdownitemcollection/add/)(*string*) | Koleksiyonun sonuna bir dize ekler. |
| [Clear](../../aspose.words.fields/dropdownitemcollection/clear/)() | Koleksiyondaki tüm öğeleri kaldırır. |
| [Contains](../../aspose.words.fields/dropdownitemcollection/contains/)(*string*) | Koleksiyonun belirtilen değeri içerip içermediğini belirler. |
| [GetEnumerator](../../aspose.words.fields/dropdownitemcollection/getenumerator/)() | Koleksiyondaki tüm öğeler üzerinde yineleme yapmak için kullanılabilen bir numaratör nesnesi döndürür. |
| [IndexOf](../../aspose.words.fields/dropdownitemcollection/indexof/)(*string*) | Koleksiyondaki belirtilen değerin sıfır tabanlı dizinini döndürür. |
| [Insert](../../aspose.words.fields/dropdownitemcollection/insert/)(*int, string*) | Belirtilen dizindeki koleksiyona bir dize ekler. |
| [Remove](../../aspose.words.fields/dropdownitemcollection/remove/)(*string*) | Belirtilen değeri koleksiyondan kaldırır. |
| [RemoveAt](../../aspose.words.fields/dropdownitemcollection/removeat/)(*int*) | Belirtilen dizindeki bir değeri kaldırır. |

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

* class [FormField](../formfield/)
* property [DropDownItems](../formfield/dropdownitems/)
* ad alanı [Aspose.Words.Fields](../../aspose.words.fields/)
* toplantı [Aspose.Words](../../)
