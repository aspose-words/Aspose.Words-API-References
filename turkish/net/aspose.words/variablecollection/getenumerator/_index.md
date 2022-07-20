---
title: GetEnumerator
second_title: Aspose.Words for .NET API Referansı
description: Koleksiyondaki tüm değişkenler üzerinde yineleme yapmak için kullanılabilecek bir numaralandırıcı nesnesi döndürür.
type: docs
weight: 60
url: /tr/net/aspose.words/variablecollection/getenumerator/
---
## VariableCollection.GetEnumerator method

Koleksiyondaki tüm değişkenler üzerinde yineleme yapmak için kullanılabilecek bir numaralandırıcı nesnesi döndürür.

```csharp
public IEnumerator<KeyValuePair<string, string>> GetEnumerator()
```

### Örnekler

Bir belgenin değişken koleksiyonuyla nasıl çalışılacağını gösterir.

```csharp
Document doc = new Document();
VariableCollection variables = doc.Variables;

// Her belge, öğeler ekleyebileceğimiz bir anahtar/değer çifti değişkenleri koleksiyonuna sahiptir.
variables.Add("Home address", "123 Main St.");
variables.Add("City", "London");
variables.Add("Bedrooms", "3");

Assert.AreEqual(3, variables.Count);

// Belge gövdesindeki değişkenlerin değerlerini DOCVARIABLE alanlarını kullanarak görüntüleyebiliriz.
DocumentBuilder builder = new DocumentBuilder(doc);
FieldDocVariable field = (FieldDocVariable)builder.InsertField(FieldType.FieldDocVariable, true);
field.VariableName = "Home address";
field.Update();

Assert.AreEqual("123 Main St.", field.Result);

// Mevcut anahtarlara değer atamak onları güncelleyecektir.
variables.Add("Home address", "456 Queen St.");

// Daha sonra, güncel bir değer göstermelerini sağlamak için DOCVARIABLE alanlarını güncellememiz gerekecek.
Assert.AreEqual("123 Main St.", field.Result);

field.Update();

Assert.AreEqual("456 Queen St.", field.Result);

// Belirli bir ad veya değere sahip belge değişkenlerinin var olduğunu doğrulayın.
Assert.True(variables.Contains("City"));
Assert.True(variables.Any(v => v.Value == "London"));

// Değişken koleksiyonu, değişkenleri ada göre alfabetik olarak otomatik olarak sıralar.
Assert.AreEqual(0, variables.IndexOfKey("Bedrooms"));
Assert.AreEqual(1, variables.IndexOfKey("City"));
Assert.AreEqual(2, variables.IndexOfKey("Home address"));

// Değişken koleksiyonu üzerinde numaralandır.
using (IEnumerator<KeyValuePair<string, string>> enumerator = doc.Variables.GetEnumerator())
    while (enumerator.MoveNext())
        Console.WriteLine($"Name: {enumerator.Current.Key}, Value: {enumerator.Current.Value}");

// Aşağıda, bir koleksiyondan belge değişkenlerini kaldırmanın üç yolu bulunmaktadır.
// 1 - Ada göre:
variables.Remove("City");

Assert.False(variables.Contains("City"));

// 2 - Dizine göre:
variables.RemoveAt(1);

Assert.False(variables.Contains("Home address"));

// 3 - Tüm koleksiyonu bir kerede temizle:
variables.Clear();

Assert.That(variables, Is.Empty);
```

### Ayrıca bakınız

* class [VariableCollection](../../variablecollection)
* ad alanı [Aspose.Words](../../variablecollection)
* toplantı [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->