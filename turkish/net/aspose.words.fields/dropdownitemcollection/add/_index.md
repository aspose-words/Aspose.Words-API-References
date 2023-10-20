---
title: DropDownItemCollection.Add
linktitle: Add
articleTitle: Add
second_title: Aspose.Words for .NET
description: DropDownItemCollection Add yöntem. Koleksiyonun sonuna bir dize ekler C#'da.
type: docs
weight: 30
url: /tr/net/aspose.words.fields/dropdownitemcollection/add/
---
## DropDownItemCollection.Add method

Koleksiyonun sonuna bir dize ekler.

```csharp
public int Add(string value)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| value | String | Koleksiyonun sonuna eklenecek dize. |

### Geri dönüş değeri

Yeni öğenin eklendiği sıfır tabanlı dizin.

## Örnekler

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

* class [DropDownItemCollection](../)
* ad alanı [Aspose.Words.Fields](../../../aspose.words.fields/)
* toplantı [Aspose.Words](../../../)
