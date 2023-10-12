---
title: DocumentProperty.Type
second_title: Aspose.Words for .NET API Referansı
description: DocumentProperty mülk. Özelliğin veri türünü alır.
type: docs
weight: 40
url: /tr/net/aspose.words.properties/documentproperty/type/
---
## DocumentProperty.Type property

Özelliğin veri türünü alır.

```csharp
public PropertyType Type { get; }
```

### Örnekler

Yerleşik belge özellikleriyle nasıl çalışılacağını gösterir.

```csharp
Document doc = new Document(MyDir + "Properties.docx");

// "Belge" nesnesi, meta verilerinin bir kısmını üyelerinde içerir.
Console.WriteLine($"Document filename:\n\t \"{doc.OriginalFileName}\"");

// Belge aynı zamanda meta verileri yerleşik özelliklerinde de saklar.
// Her yerleşik özellik, belgenin "BuiltInDocumentProperties" nesnesinin bir üyesidir.
Console.WriteLine("Built-in Properties:");
foreach (DocumentProperty docProperty in doc.BuiltInDocumentProperties)
{
    Console.WriteLine(docProperty.Name);
    Console.WriteLine($"\tType:\t{docProperty.Type}");

    // Bazı özellikler birden fazla değer saklayabilir.
    if (docProperty.Value is ICollection<object>)
    {
        foreach (object value in docProperty.Value as ICollection<object>)
            Console.WriteLine($"\tValue:\t\"{value}\"");
    }
    else
    {
        Console.WriteLine($"\tValue:\t\"{docProperty.Value}\"");
    }
}
```

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

* enum [PropertyType](../../propertytype/)
* class [DocumentProperty](../)
* ad alanı [Aspose.Words.Properties](../../documentproperty/)
* toplantı [Aspose.Words](../../../)


