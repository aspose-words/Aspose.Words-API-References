---
title: CustomDocumentProperties.Add
linktitle: Add
articleTitle: Add
second_title: .NET için Aspose.Words
description: Add yöntemi ile benzersiz özel belge özelliklerini zahmetsizce oluşturun. En iyi performans için belgelerinizi özelleştirilmiş Dize veri türleriyle geliştirin.
type: docs
weight: 10
url: /tr/net/aspose.words.properties/customdocumentproperties/add/
---
## Add(*string, string*) {#add_4}

Yeni bir özel belge özelliği oluştururString veri türü.

```csharp
public DocumentProperty Add(string name, string value)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| name | String | Mülkün adı. |
| value | String | Emlakın değeri. |

### Geri dönüş değeri

Yeni oluşturulan özellik nesnesi.

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

// Belgedeki her özel özelliği yazdır.
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

// Bu özel özellikleri Microsoft Word'de "Dosya" -> "Özellikler" > "Gelişmiş Özellikler" > "Özel" yoluyla bulabiliriz.
doc.Save(ArtifactsDir + "DocumentProperties.DocumentPropertyCollection.docx");

// Aşağıda bir belgeden özel özellikleri kaldırmanın üç yolu bulunmaktadır.
// 1 - Dizinle kaldır:
properties.RemoveAt(1);

Assert.False(properties.Contains("Authorized Amount"));
Assert.AreEqual(4, properties.Count);

// 2 - İsme göre kaldır:
properties.Remove("Authorized Revision");

Assert.False(properties.Contains("Authorized Revision"));
Assert.AreEqual(3, properties.Count);

// 3 - Tüm koleksiyonu bir defada boşalt:
properties.Clear();

Assert.AreEqual(0, properties.Count);
```

### Ayrıca bakınız

* class [DocumentProperty](../../documentproperty/)
* class [CustomDocumentProperties](../)
* ad alanı [Aspose.Words.Properties](../../../aspose.words.properties/)
* toplantı [Aspose.Words](../../../)

---

## Add(*string, int*) {#add_2}

Yeni bir özel belge özelliği oluştururNumber veri türü.

```csharp
public DocumentProperty Add(string name, int value)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| name | String | Mülkün adı. |
| value | Int32 | Emlakın değeri. |

### Geri dönüş değeri

Yeni oluşturulan özellik nesnesi.

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

// Belgedeki her özel özelliği yazdır.
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

// Bu özel özellikleri Microsoft Word'de "Dosya" -> "Özellikler" > "Gelişmiş Özellikler" > "Özel" yoluyla bulabiliriz.
doc.Save(ArtifactsDir + "DocumentProperties.DocumentPropertyCollection.docx");

// Aşağıda bir belgeden özel özellikleri kaldırmanın üç yolu bulunmaktadır.
// 1 - Dizinle kaldır:
properties.RemoveAt(1);

Assert.False(properties.Contains("Authorized Amount"));
Assert.AreEqual(4, properties.Count);

// 2 - İsme göre kaldır:
properties.Remove("Authorized Revision");

Assert.False(properties.Contains("Authorized Revision"));
Assert.AreEqual(3, properties.Count);

// 3 - Tüm koleksiyonu bir defada boşalt:
properties.Clear();

Assert.AreEqual(0, properties.Count);
```

### Ayrıca bakınız

* class [DocumentProperty](../../documentproperty/)
* class [CustomDocumentProperties](../)
* ad alanı [Aspose.Words.Properties](../../../aspose.words.properties/)
* toplantı [Aspose.Words](../../../)

---

## Add(*string, DateTime*) {#add_3}

Yeni bir özel belge özelliği oluştururDateTime veri türü.

```csharp
public DocumentProperty Add(string name, DateTime value)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| name | String | Mülkün adı. |
| value | DateTime | Emlakın değeri. |

### Geri dönüş değeri

Yeni oluşturulan özellik nesnesi.

## Örnekler

Tarih ve saat içeren özel bir belge özelliğinin nasıl oluşturulacağını gösterir.

```csharp
Document doc = new Document();

doc.CustomDocumentProperties.Add("AuthorizationDate", DateTime.Now);
DateTime authorizationDate = doc.CustomDocumentProperties["AuthorizationDate"].ToDateTime();
Console.WriteLine($"Document authorized on {authorizationDate}");
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

// Belgedeki her özel özelliği yazdır.
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

// Bu özel özellikleri Microsoft Word'de "Dosya" -> "Özellikler" > "Gelişmiş Özellikler" > "Özel" yoluyla bulabiliriz.
doc.Save(ArtifactsDir + "DocumentProperties.DocumentPropertyCollection.docx");

// Aşağıda bir belgeden özel özellikleri kaldırmanın üç yolu bulunmaktadır.
// 1 - Dizinle kaldır:
properties.RemoveAt(1);

Assert.False(properties.Contains("Authorized Amount"));
Assert.AreEqual(4, properties.Count);

// 2 - İsme göre kaldır:
properties.Remove("Authorized Revision");

Assert.False(properties.Contains("Authorized Revision"));
Assert.AreEqual(3, properties.Count);

// 3 - Tüm koleksiyonu bir defada boşalt:
properties.Clear();

Assert.AreEqual(0, properties.Count);
```

### Ayrıca bakınız

* class [DocumentProperty](../../documentproperty/)
* class [CustomDocumentProperties](../)
* ad alanı [Aspose.Words.Properties](../../../aspose.words.properties/)
* toplantı [Aspose.Words](../../../)

---

## Add(*string, bool*) {#add}

Yeni bir özel belge özelliği oluştururBoolean veri türü.

```csharp
public DocumentProperty Add(string name, bool value)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| name | String | Mülkün adı. |
| value | Boolean | Emlakın değeri. |

### Geri dönüş değeri

Yeni oluşturulan özellik nesnesi.

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

// Belgedeki her özel özelliği yazdır.
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

// Bu özel özellikleri Microsoft Word'de "Dosya" -> "Özellikler" > "Gelişmiş Özellikler" > "Özel" yoluyla bulabiliriz.
doc.Save(ArtifactsDir + "DocumentProperties.DocumentPropertyCollection.docx");

// Aşağıda bir belgeden özel özellikleri kaldırmanın üç yolu bulunmaktadır.
// 1 - Dizinle kaldır:
properties.RemoveAt(1);

Assert.False(properties.Contains("Authorized Amount"));
Assert.AreEqual(4, properties.Count);

// 2 - İsme göre kaldır:
properties.Remove("Authorized Revision");

Assert.False(properties.Contains("Authorized Revision"));
Assert.AreEqual(3, properties.Count);

// 3 - Tüm koleksiyonu bir defada boşalt:
properties.Clear();

Assert.AreEqual(0, properties.Count);
```

### Ayrıca bakınız

* class [DocumentProperty](../../documentproperty/)
* class [CustomDocumentProperties](../)
* ad alanı [Aspose.Words.Properties](../../../aspose.words.properties/)
* toplantı [Aspose.Words](../../../)

---

## Add(*string, double*) {#add_1}

Yeni bir özel belge özelliği oluştururDouble veri türü.

```csharp
public DocumentProperty Add(string name, double value)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| name | String | Mülkün adı. |
| value | Double | Emlakın değeri. |

### Geri dönüş değeri

Yeni oluşturulan özellik nesnesi.

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

// Belgedeki her özel özelliği yazdır.
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

// Bu özel özellikleri Microsoft Word'de "Dosya" -> "Özellikler" > "Gelişmiş Özellikler" > "Özel" yoluyla bulabiliriz.
doc.Save(ArtifactsDir + "DocumentProperties.DocumentPropertyCollection.docx");

// Aşağıda bir belgeden özel özellikleri kaldırmanın üç yolu bulunmaktadır.
// 1 - Dizinle kaldır:
properties.RemoveAt(1);

Assert.False(properties.Contains("Authorized Amount"));
Assert.AreEqual(4, properties.Count);

// 2 - İsme göre kaldır:
properties.Remove("Authorized Revision");

Assert.False(properties.Contains("Authorized Revision"));
Assert.AreEqual(3, properties.Count);

// 3 - Tüm koleksiyonu bir defada boşalt:
properties.Clear();

Assert.AreEqual(0, properties.Count);
```

### Ayrıca bakınız

* class [DocumentProperty](../../documentproperty/)
* class [CustomDocumentProperties](../)
* ad alanı [Aspose.Words.Properties](../../../aspose.words.properties/)
* toplantı [Aspose.Words](../../../)
