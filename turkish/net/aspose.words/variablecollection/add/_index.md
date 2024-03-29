---
title: VariableCollection.Add
linktitle: Add
articleTitle: Add
second_title: Aspose.Words for .NET
description: VariableCollection Add yöntem. Koleksiyona bir belge değişkeni ekler C#'da.
type: docs
weight: 30
url: /tr/net/aspose.words/variablecollection/add/
---
## VariableCollection.Add method

Koleksiyona bir belge değişkeni ekler.

```csharp
public void Add(string name, string value)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| name | String | Eklenecek değişkenin büyük/küçük harfe duyarlı olmayan adı. |
| value | String | Değişkenin değeri. Değer olamaz`hükümsüz`, eğer değer null ise bunun yerine boş dize kullanılacaktır. |

## Örnekler

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

* class [VariableCollection](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
