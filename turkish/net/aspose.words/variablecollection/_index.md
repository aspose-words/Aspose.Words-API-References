---
title: VariableCollection Class
linktitle: VariableCollection
articleTitle: VariableCollection
second_title: .NET için Aspose.Words
description: Aspose.Words.VariableCollection'ı keşfedin, gelişmiş belge otomasyonu ve esnekliği için belge değişkenlerini etkin bir şekilde yönetin ve özelleştirin.
type: docs
weight: 7380
url: /tr/net/aspose.words/variablecollection/
---
## VariableCollection class

Belge değişkenlerinin bir koleksiyonu.

Daha fazla bilgi edinmek için şu adresi ziyaret edin:[Belge Özellikleriyle Çalışma](https://docs.aspose.com/words/net/work-with-document-properties/) belgeleme makalesi.

```csharp
public class VariableCollection : IEnumerable<KeyValuePair<string, string>>
```

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [Count](../../aspose.words/variablecollection/count/) { get; } | Koleksiyonda bulunan öğelerin sayısını alır. |
| [Item](../../aspose.words/variablecollection/item/) { get; set; } | Büyük/küçük harfe duyarlı olmayan bir adla bir belge değişkenini alır veya ayarlar. `hükümsüz`değerler atama işleminin sağ tarafında yer alamaz ve boş bir dize ile değiştirilir. (2 indexers) |

## yöntemler

| İsim | Tanım |
| --- | --- |
| [Add](../../aspose.words/variablecollection/add/)(*string, string*) | Koleksiyona bir belge değişkeni ekler. |
| [Clear](../../aspose.words/variablecollection/clear/)() | Koleksiyondaki tüm öğeleri kaldırır. |
| [Contains](../../aspose.words/variablecollection/contains/)(*string*) | Koleksiyonun verilen ada sahip bir belge değişkeni içerip içermediğini belirler. |
| [GetEnumerator](../../aspose.words/variablecollection/getenumerator/)() | Koleksiyondaki tüm değişkenler üzerinde yineleme yapmak için kullanılabilen bir numaralandırıcı nesnesi döndürür. |
| [IndexOfKey](../../aspose.words/variablecollection/indexofkey/)(*string*) | Koleksiyondaki belirtilen belge değişkeninin sıfır tabanlı dizinini döndürür. |
| [Remove](../../aspose.words/variablecollection/remove/)(*string*) | Belirtilen ada sahip bir belge değişkenini koleksiyondan kaldırır. |
| [RemoveAt](../../aspose.words/variablecollection/removeat/)(*int*) | Belirtilen dizindeki bir belge değişkenini kaldırır. |

## Notlar

Değişken adları ve değerleri dizelerdir.

Değişken adları büyük/küçük harfe duyarlı değildir.

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

* ad alanı [Aspose.Words](../../aspose.words/)
* toplantı [Aspose.Words](../../)
