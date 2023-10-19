---
title: CustomDocumentProperties.Add
linktitle: Add
articleTitle: Add
second_title: Aspose.Words for .NET
description: CustomDocumentProperties Add yöntem. Yeni bir özel belge özelliği oluşturur.String veri türü C#'da.
type: docs
weight: 10
url: /tr/net/aspose.words.properties/customdocumentproperties/add/
---
## Add(*string, string*) {#add_4}

Yeni bir özel belge özelliği oluşturur.String veri türü.

```csharp
public DocumentProperty Add(string name, string value)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| name | String | Mülkün adı. |
| value | String | Mülkün değeri. |

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

* class [DocumentProperty](../../documentproperty/)
* class [CustomDocumentProperties](../)
* ad alanı [Aspose.Words.Properties](../../../aspose.words.properties/)
* toplantı [Aspose.Words](../../../)

---

## Add(*string, int*) {#add_2}

Yeni bir özel belge özelliği oluşturur.Number veri türü.

```csharp
public DocumentProperty Add(string name, int value)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| name | String | Mülkün adı. |
| value | Int32 | Mülkün değeri. |

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

* class [DocumentProperty](../../documentproperty/)
* class [CustomDocumentProperties](../)
* ad alanı [Aspose.Words.Properties](../../../aspose.words.properties/)
* toplantı [Aspose.Words](../../../)

---

## Add(*string, DateTime*) {#add_3}

Yeni bir özel belge özelliği oluşturur.DateTime veri türü.

```csharp
public DocumentProperty Add(string name, DateTime value)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| name | String | Mülkün adı. |
| value | DateTime | Mülkün değeri. |

### Geri dönüş değeri

Yeni oluşturulan özellik nesnesi.

## Örnekler

Tarih ve saat içeren özel bir belge özelliğinin nasıl oluşturulacağını gösterir.

```csharp
Document doc = new Document();

doc.CustomDocumentProperties.Add("AuthorizationDate", DateTime.Now);

Console.WriteLine($"Document authorized on {doc.CustomDocumentProperties["AuthorizationDate"].ToDateTime()}");
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

* class [DocumentProperty](../../documentproperty/)
* class [CustomDocumentProperties](../)
* ad alanı [Aspose.Words.Properties](../../../aspose.words.properties/)
* toplantı [Aspose.Words](../../../)

---

## Add(*string, bool*) {#add}

Yeni bir özel belge özelliği oluşturur.Boolean veri türü.

```csharp
public DocumentProperty Add(string name, bool value)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| name | String | Mülkün adı. |
| value | Boolean | Mülkün değeri. |

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

* class [DocumentProperty](../../documentproperty/)
* class [CustomDocumentProperties](../)
* ad alanı [Aspose.Words.Properties](../../../aspose.words.properties/)
* toplantı [Aspose.Words](../../../)

---

## Add(*string, double*) {#add_1}

Yeni bir özel belge özelliği oluşturur.Double veri türü.

```csharp
public DocumentProperty Add(string name, double value)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| name | String | Mülkün adı. |
| value | Double | Mülkün değeri. |

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

* class [DocumentProperty](../../documentproperty/)
* class [CustomDocumentProperties](../)
* ad alanı [Aspose.Words.Properties](../../../aspose.words.properties/)
* toplantı [Aspose.Words](../../../)
