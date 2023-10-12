---
title: Class DropDownItemCollection
second_title: Aspose.Words for .NET API Referansı
description: Aspose.Words.Fields.DropDownItemCollection sınıf. Açılan form alanındaki tüm öğeleri temsil eden dizelerden oluşan bir koleksiyon.
type: docs
weight: 1500
url: /tr/net/aspose.words.fields/dropdownitemcollection/
---
## DropDownItemCollection class

Açılan form alanındaki tüm öğeleri temsil eden dizelerden oluşan bir koleksiyon.

Daha fazlasını öğrenmek için şu adresi ziyaret edin:[Alanlarla Çalışmak](https://docs.aspose.com/words/net/working-with-fields/) dokümantasyon makalesi.

```csharp
public class DropDownItemCollection : IEnumerable<string>
```

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [Count](../../aspose.words.fields/dropdownitemcollection/count/) { get; } | Koleksiyonda yer alan öğelerin sayısını alır. |
| [Item](../../aspose.words.fields/dropdownitemcollection/item/) { get; set; } | Belirtilen dizindeki öğeyi alır veya ayarlar. |

## yöntemler

| İsim | Tanım |
| --- | --- |
| [Add](../../aspose.words.fields/dropdownitemcollection/add/)(string) | Koleksiyonun sonuna bir dize ekler. |
| [Clear](../../aspose.words.fields/dropdownitemcollection/clear/)() | Koleksiyondaki tüm öğeleri kaldırır. |
| [Contains](../../aspose.words.fields/dropdownitemcollection/contains/)(string) | Koleksiyonun belirtilen değeri içerip içermediğini belirler. |
| [GetEnumerator](../../aspose.words.fields/dropdownitemcollection/getenumerator/)() | Koleksiyondaki tüm öğeler üzerinde yineleme yapmak için kullanılabilecek bir numaralandırıcı nesnesini döndürür. |
| [IndexOf](../../aspose.words.fields/dropdownitemcollection/indexof/)(string) | Koleksiyonda belirtilen değerin sıfır tabanlı dizinini döndürür. |
| [Insert](../../aspose.words.fields/dropdownitemcollection/insert/)(int, string) | Belirtilen dizindeki koleksiyona bir dize ekler. |
| [Remove](../../aspose.words.fields/dropdownitemcollection/remove/)(string) | Belirtilen değeri koleksiyondan kaldırır. |
| [RemoveAt](../../aspose.words.fields/dropdownitemcollection/removeat/)(int) | Belirtilen dizindeki bir değeri kaldırır. |

### Örnekler

Açılan kutu alanının nasıl ekleneceğini ve öğe koleksiyonundaki öğelerin nasıl düzenleneceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Bir açılan kutu ekleyin ve ardından açılır öğeler koleksiyonunu doğrulayın.
// Microsoft Word'de kullanıcı açılan kutuya tıklayacak,
// ve ardından koleksiyondaki görüntülenecek metin öğelerinden birini seçin.
string[] items = { "One", "Two", "Three" };
FormField comboBoxField = builder.InsertComboBox("DropDown", items, 0);
DropDownItemCollection dropDownItems = comboBoxField.DropDownItems;

Assert.AreEqual(3, dropDownItems.Count);
Assert.AreEqual("One", dropDownItems[0]);
Assert.AreEqual(1, dropDownItems.IndexOf("Two"));
Assert.IsTrue(dropDownItems.Contains("Three"));

// Mevcut açılır kutu öğeleri koleksiyonuna yeni bir öğe eklemenin iki yolu vardır.
// 1 - Koleksiyonun sonuna bir öğe ekleyin:
dropDownItems.Add("Four");

// 2 - Belirtilen dizindeki başka bir öğenin önüne bir öğe ekleyin:
dropDownItems.Insert(3, "Three and a half");

Assert.AreEqual(5, dropDownItems.Count);

// Koleksiyon üzerinde yineleme yapın ve her öğeyi yazdırın.
using (IEnumerator<string> dropDownCollectionEnumerator = dropDownItems.GetEnumerator())
    while (dropDownCollectionEnumerator.MoveNext())
        Console.WriteLine(dropDownCollectionEnumerator.Current);

// Açılan öğeler koleksiyonundan öğeleri kaldırmanın iki yolu vardır.
// 1 - İçeriği iletilen dizeye eşit olan bir öğeyi kaldırın:
dropDownItems.Remove("Four");

// 2 - Dizindeki bir öğeyi kaldırın:
dropDownItems.RemoveAt(3);

Assert.AreEqual(3, dropDownItems.Count);
Assert.IsFalse(dropDownItems.Contains("Three and a half"));
Assert.IsFalse(dropDownItems.Contains("Four"));

doc.Save(ArtifactsDir + "FormFields.DropDownItemCollection.html");

// Açılan öğeler koleksiyonunun tamamını boşaltın.
dropDownItems.Clear();
```

### Ayrıca bakınız

* class [FormField](../formfield/)
* property [DropDownItems](../formfield/dropdownitems/)
* ad alanı [Aspose.Words.Fields](../../aspose.words.fields/)
* toplantı [Aspose.Words](../../)


