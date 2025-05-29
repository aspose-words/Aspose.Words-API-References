---
title: VariableCollection.Item
linktitle: Item
articleTitle: Item
second_title: .NET için Aspose.Words
description: VariableCollection Item ile belge değişkenlerini zahmetsizce yönetin. Büyük/küçük harfe duyarlı olmayan adları kolayca ayarlayın veya alın; boş değerlere izin verilmez, böylece veri bütünlüğü sağlanır.
type: docs
weight: 20
url: /tr/net/aspose.words/variablecollection/item/
---
## VariableCollection indexer (1 of 2)

Büyük/küçük harfe duyarlı olmayan bir adla bir belge değişkenini alır veya ayarlar. `hükümsüz`değerler atama işleminin sağ tarafında yer alamaz ve boş bir dize ile değiştirilir.

```csharp
public string this[string name] { get; set; }
```

## Örnekler

Bir belgenin değişken koleksiyonuyla nasıl çalışılacağını gösterir.

```csharp
Document doc = new Document();
VariableCollection variables = doc.Variables;

// Her belgenin, öğeler ekleyebileceğimiz bir anahtar/değer çifti değişkenleri koleksiyonu vardır.
variables.Add("Home address", "123 Main St.");
variables.Add("City", "London");
variables.Add("Bedrooms", "3");

Assert.AreEqual(3, variables.Count);

// DOCVARIABLE alanlarını kullanarak değişkenlerin değerlerini belge gövdesinde görüntüleyebiliriz.
DocumentBuilder builder = new DocumentBuilder(doc);
FieldDocVariable field = (FieldDocVariable)builder.InsertField(FieldType.FieldDocVariable, true);
field.VariableName = "Home address";
field.Update();

Assert.AreEqual("123 Main St.", field.Result);

// Mevcut anahtarlara değer atamak onları güncelleyecektir.
variables.Add("Home address", "456 Queen St.");

// Daha sonra güncel bir değer görüntülediğinden emin olmak için DOCVARIABLE alanlarını güncellememiz gerekecek.
Assert.AreEqual("123 Main St.", field.Result);

field.Update();

Assert.AreEqual("456 Queen St.", field.Result);

// Belirli bir ad veya değere sahip belge değişkenlerinin var olduğunu doğrulayın.
Assert.True(variables.Contains("City"));
Assert.True(variables.Any(v => v.Value == "London"));

// Değişken koleksiyonu değişkenleri otomatik olarak adlarına göre alfabetik olarak sıralar.
Assert.AreEqual(0, variables.IndexOfKey("Bedrooms"));
Assert.AreEqual(1, variables.IndexOfKey("City"));
Assert.AreEqual(2, variables.IndexOfKey("Home address"));

Assert.AreEqual("3", variables[0]);
Assert.AreEqual("London", variables["City"]);

// Değişken koleksiyonu üzerinde numaralandırma.
using (IEnumerator<KeyValuePair<string, string>> enumerator = doc.Variables.GetEnumerator())
    while (enumerator.MoveNext())
        Console.WriteLine($"Name: {enumerator.Current.Key}, Value: {enumerator.Current.Value}");

// Aşağıda bir koleksiyondan belge değişkenlerini kaldırmanın üç yolu bulunmaktadır.
// 1 - İsme göre:
variables.Remove("City");

Assert.False(variables.Contains("City"));

// 2 - Dizin olarak:
variables.RemoveAt(1);

Assert.False(variables.Contains("Home address"));

// 3 - Tüm koleksiyonu bir defada temizle:
variables.Clear();

Assert.AreEqual(0, variables.Count);
```

### Ayrıca bakınız

* class [VariableCollection](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)

---

## VariableCollection indexer (2 of 2)

Belirtilen dizinde bir belge değişkenini alır veya ayarlar. `hükümsüz`değerler atama işleminin sağ tarafında yer alamaz ve boş bir dize ile değiştirilir.

```csharp
public string this[int index] { get; set; }
```

| Parametre | Tanım |
| --- | --- |
| index | Belge değişkeninin sıfırdan başlayan indeksi. |

## Örnekler

Bir belgenin değişken koleksiyonuyla nasıl çalışılacağını gösterir.

```csharp
Document doc = new Document();
VariableCollection variables = doc.Variables;

// Her belgenin, öğeler ekleyebileceğimiz bir anahtar/değer çifti değişkenleri koleksiyonu vardır.
variables.Add("Home address", "123 Main St.");
variables.Add("City", "London");
variables.Add("Bedrooms", "3");

Assert.AreEqual(3, variables.Count);

// DOCVARIABLE alanlarını kullanarak değişkenlerin değerlerini belge gövdesinde görüntüleyebiliriz.
DocumentBuilder builder = new DocumentBuilder(doc);
FieldDocVariable field = (FieldDocVariable)builder.InsertField(FieldType.FieldDocVariable, true);
field.VariableName = "Home address";
field.Update();

Assert.AreEqual("123 Main St.", field.Result);

// Mevcut anahtarlara değer atamak onları güncelleyecektir.
variables.Add("Home address", "456 Queen St.");

// Daha sonra güncel bir değer görüntülediğinden emin olmak için DOCVARIABLE alanlarını güncellememiz gerekecek.
Assert.AreEqual("123 Main St.", field.Result);

field.Update();

Assert.AreEqual("456 Queen St.", field.Result);

// Belirli bir ad veya değere sahip belge değişkenlerinin var olduğunu doğrulayın.
Assert.True(variables.Contains("City"));
Assert.True(variables.Any(v => v.Value == "London"));

// Değişken koleksiyonu değişkenleri otomatik olarak adlarına göre alfabetik olarak sıralar.
Assert.AreEqual(0, variables.IndexOfKey("Bedrooms"));
Assert.AreEqual(1, variables.IndexOfKey("City"));
Assert.AreEqual(2, variables.IndexOfKey("Home address"));

Assert.AreEqual("3", variables[0]);
Assert.AreEqual("London", variables["City"]);

// Değişken koleksiyonu üzerinde numaralandırma.
using (IEnumerator<KeyValuePair<string, string>> enumerator = doc.Variables.GetEnumerator())
    while (enumerator.MoveNext())
        Console.WriteLine($"Name: {enumerator.Current.Key}, Value: {enumerator.Current.Value}");

// Aşağıda bir koleksiyondan belge değişkenlerini kaldırmanın üç yolu bulunmaktadır.
// 1 - İsme göre:
variables.Remove("City");

Assert.False(variables.Contains("City"));

// 2 - Dizin olarak:
variables.RemoveAt(1);

Assert.False(variables.Contains("Home address"));

// 3 - Tüm koleksiyonu bir defada temizle:
variables.Clear();

Assert.AreEqual(0, variables.Count);
```

### Ayrıca bakınız

* class [VariableCollection](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
