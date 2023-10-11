---
title: Class VariableCollection
second_title: Aspose.Words for .NET API Referansı
description: Aspose.Words.VariableCollection sınıf. Belge değişkenlerinden oluşan bir koleksiyon.
type: docs
weight: 6530
url: /tr/net/aspose.words/variablecollection/
---
## VariableCollection class

Belge değişkenlerinden oluşan bir koleksiyon.

Daha fazlasını öğrenmek için şu adresi ziyaret edin:[Belge Özellikleriyle Çalışma](https://docs.aspose.com/words/net/work-with-document-properties/) dokümantasyon makalesi.

```csharp
public class VariableCollection : IEnumerable<KeyValuePair<string, string>>
```

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [Count](../../aspose.words/variablecollection/count/) { get; } | Koleksiyonda yer alan öğelerin sayısını alır. |
| [Item](../../aspose.words/variablecollection/item/) { get; set; } | Büyük/küçük harfe duyarlı olmayan ada göre bir belge değişkenini alır veya ayarlar. `hükümsüz` atamanın sağ tarafında değerlere izin verilmez ve bunlar boş dizeyle değiştirilecektir. (2 indexers) |

## yöntemler

| İsim | Tanım |
| --- | --- |
| [Add](../../aspose.words/variablecollection/add/)(string, string) | Koleksiyona bir belge değişkeni ekler. |
| [Clear](../../aspose.words/variablecollection/clear/)() | Koleksiyondaki tüm öğeleri kaldırır. |
| [Contains](../../aspose.words/variablecollection/contains/)(string) | Koleksiyonun verilen adda bir belge değişkeni içerip içermediğini belirler. |
| [GetEnumerator](../../aspose.words/variablecollection/getenumerator/)() | Koleksiyondaki tüm değişkenleri yinelemek için kullanılabilecek bir numaralandırıcı nesnesini döndürür. |
| [IndexOfKey](../../aspose.words/variablecollection/indexofkey/)(string) | Koleksiyonda belirtilen belge değişkeninin sıfır tabanlı dizinini döndürür. |
| [Remove](../../aspose.words/variablecollection/remove/)(string) | Koleksiyondan belirtilen ada sahip bir belge değişkenini kaldırır. |
| [RemoveAt](../../aspose.words/variablecollection/removeat/)(int) | Belirtilen dizindeki bir belge değişkenini kaldırır. |

### Notlar

Değişken adları ve değerleri dizelerdir.

Değişken adları büyük/küçük harfe duyarlı değildir.

### Örnekler

Bir belgenin değişken koleksiyonuyla nasıl çalışılacağını gösterir.

```csharp
Document doc = new Document();
VariableCollection variables = doc.Variables;

// Her belgede, öğeler ekleyebileceğimiz bir anahtar/değer çifti değişkenleri koleksiyonu bulunur.
variables.Add("Home address", "123 Main St.");
variables.Add("City", "London");
variables.Add("Bedrooms", "3");

Assert.AreEqual(3, variables.Count);

// DOCVARIABLE alanlarını kullanarak belge gövdesindeki değişkenlerin değerlerini görüntüleyebiliriz.
DocumentBuilder builder = new DocumentBuilder(doc);
FieldDocVariable field = (FieldDocVariable)builder.InsertField(FieldType.FieldDocVariable, true);
field.VariableName = "Home address";
field.Update();

Assert.AreEqual("123 Main St.", field.Result);

// Mevcut anahtarlara değer atamak onları güncelleyecektir.
variables.Add("Home address", "456 Queen St.");

// Daha sonra DOCVARIABLE alanlarını güncel bir değer görüntülediklerinden emin olmak için güncellememiz gerekecek.
Assert.AreEqual("123 Main St.", field.Result);

field.Update();

Assert.AreEqual("456 Queen St.", field.Result);

//Belirli bir ada veya değere sahip belge değişkenlerinin mevcut olduğunu doğrulayın.
Assert.True(variables.Contains("City"));
Assert.True(variables.Any(v => v.Value == "London"));

// Değişkenlerin toplanması, değişkenleri otomatik olarak ada göre alfabetik olarak sıralar.
Assert.AreEqual(0, variables.IndexOfKey("Bedrooms"));
Assert.AreEqual(1, variables.IndexOfKey("City"));
Assert.AreEqual(2, variables.IndexOfKey("Home address"));

// Değişkenlerin koleksiyonunu numaralandırın.
using (IEnumerator<KeyValuePair<string, string>> enumerator = doc.Variables.GetEnumerator())
    while (enumerator.MoveNext())
        Console.WriteLine($"Name: {enumerator.Current.Key}, Value: {enumerator.Current.Value}");

// Aşağıda belge değişkenlerini bir koleksiyondan kaldırmanın üç yolu verilmiştir.
// 1 - Ada göre:
variables.Remove("City");

Assert.False(variables.Contains("City"));

// 2 - Dizine göre:
variables.RemoveAt(1);

Assert.False(variables.Contains("Home address"));

// 3 - Tüm koleksiyonu bir kerede temizleyin:
variables.Clear();

Assert.That(variables, Is.Empty);
```

### Ayrıca bakınız

* ad alanı [Aspose.Words](../../aspose.words/)
* toplantı [Aspose.Words](../../)


