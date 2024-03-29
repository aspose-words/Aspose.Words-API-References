---
title: PropertyType Enum
linktitle: PropertyType
articleTitle: PropertyType
second_title: Aspose.Words for .NET
description: Aspose.Words.Properties.PropertyType Sıralama. Bir belge özelliğinin veri türünü belirtir C#'da.
type: docs
weight: 4500
url: /tr/net/aspose.words.properties/propertytype/
---
## PropertyType enumeration

Bir belge özelliğinin veri türünü belirtir.

```csharp
public enum PropertyType
```

### değerler

| İsim | Değer | Tanım |
| --- | --- | --- |
| Boolean | `0` | Özellik bir boole değeridir. |
| DateTime | `1` | Özellik bir tarih saat değeridir. |
| Double | `2` | Özellik kayan bir sayıdır. |
| Number | `3` | Özellik bir tam sayıdır. |
| String | `4` | Özellik bir dize değeridir. |
| StringArray | `5` | Özellik bir dize dizisidir. |
| ObjectArray | `6` | Özellik bir nesne dizisidir. |
| ByteArray | `7` | Özellik bir bayt dizisidir. |
| Other | `8` | Özellik başka bir türdedir. |

## Örnekler

Bir belgenin özel özellikleriyle nasıl çalışılacağını gösterir.

```csharp
Document doc = new Document();
CustomDocumentProperties properties = doc.CustomDocumentProperties;

Assert.AreEqual(0, properties.Count);

// Özel belge özellikleri, belgeye ekleyebileceğimiz anahtar-değer çiftleridir.
properties.Add("Authorized", true);
properties.Add("Authorized By", "John Doe");
properties.Add("Authorized Date", DateTime.Today);
properties.Add("Authorized Revision", doc.BuiltInDocumentProperties.RevisionNumber);
properties.Add("Authorized Amount", 123.45);

// Koleksiyon, özel özellikleri alfabetik sıraya göre sıralar.
Assert.AreEqual(1, properties.IndexOf("Authorized Amount"));
Assert.AreEqual(5, properties.Count);

// Belgedeki her özel özelliği yazdırın.
using (IEnumerator<DocumentProperty> enumerator = properties.GetEnumerator())
{
    while (enumerator.MoveNext())
        Console.WriteLine($"Name: \"{enumerator.Current.Name}\"\n\tType: \"{enumerator.Current.Type}\"\n\tValue: \"{enumerator.Current.Value}\"");
}

// DOCPROPERTY alanını kullanarak özel bir özelliğin değerini görüntüleyin.
DocumentBuilder builder = new DocumentBuilder(doc);
FieldDocProperty field = (FieldDocProperty)builder.InsertField(" DOCPROPERTY \"Authorized By\"");
field.Update();

Assert.AreEqual("John Doe", field.Result);

// Bu özel özellikleri Microsoft Word'de "Dosya" -> aracılığıyla bulabiliriz. "Özellikler" > "Gelişmiş Özellikler" > "Gelenek".
doc.Save(ArtifactsDir + "DocumentProperties.DocumentPropertyCollection.docx");

// Aşağıda bir belgeden özel özellikleri kaldırmanın üç yolu bulunmaktadır.
// 1 - Dizine göre kaldır:
properties.RemoveAt(1);

Assert.False(properties.Contains("Authorized Amount"));
Assert.AreEqual(4, properties.Count);

// 2 - İsme göre kaldır:
properties.Remove("Authorized Revision");

Assert.False(properties.Contains("Authorized Revision"));
Assert.AreEqual(3, properties.Count);

// 3 - Koleksiyonun tamamını bir kerede boşaltın:
properties.Clear();

Assert.AreEqual(0, properties.Count);
```

### Ayrıca bakınız

* class [DocumentProperty](../documentproperty/)
* property [Type](../documentproperty/type/)
* ad alanı [Aspose.Words.Properties](../../aspose.words.properties/)
* toplantı [Aspose.Words](../../)
