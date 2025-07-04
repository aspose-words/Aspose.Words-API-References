---
title: CustomDocumentProperties.Add
linktitle: Add
articleTitle: Add
second_title: Aspose.Words for .NET
description: Create unique custom document properties effortlessly with the Add method. Enhance your documents with tailored String data types for optimal performance.
type: docs
weight: 10
url: /net/aspose.words.properties/customdocumentproperties/add/
---
## Add(*string, string*) {#add_4}

Creates a new custom document property of the String data type.

```csharp
public DocumentProperty Add(string name, string value)
```

| Parameter | Type | Description |
| --- | --- | --- |
| name | String | The name of the property. |
| value | String | The value of the property. |

### Return Value

The newly created property object.

## Examples

Shows how to work with a document's custom properties.

```csharp
Document doc = new Document();
CustomDocumentProperties properties = doc.CustomDocumentProperties;

Assert.That(properties.Count, Is.EqualTo(0));

// Custom document properties are key-value pairs that we can add to the document.
properties.Add("Authorized", true);
properties.Add("Authorized By", "John Doe");
properties.Add("Authorized Date", DateTime.Today);
properties.Add("Authorized Revision", doc.BuiltInDocumentProperties.RevisionNumber);
properties.Add("Authorized Amount", 123.45);

// The collection sorts the custom properties in alphabetic order.
Assert.That(properties.IndexOf("Authorized Amount"), Is.EqualTo(1));
Assert.That(properties.Count, Is.EqualTo(5));

// Print every custom property in the document.
using (IEnumerator<DocumentProperty> enumerator = properties.GetEnumerator())
{
    while (enumerator.MoveNext())
        Console.WriteLine($"Name: \"{enumerator.Current.Name}\"\n\tType: \"{enumerator.Current.Type}\"\n\tValue: \"{enumerator.Current.Value}\"");
}

// Display the value of a custom property using a DOCPROPERTY field.
DocumentBuilder builder = new DocumentBuilder(doc);
FieldDocProperty field = (FieldDocProperty)builder.InsertField(" DOCPROPERTY \"Authorized By\"");
field.Update();

Assert.That(field.Result, Is.EqualTo("John Doe"));

// We can find these custom properties in Microsoft Word via "File" -> "Properties" > "Advanced Properties" > "Custom".
doc.Save(ArtifactsDir + "DocumentProperties.DocumentPropertyCollection.docx");

// Below are three ways or removing custom properties from a document.
// 1 -  Remove by index:
properties.RemoveAt(1);

Assert.That(properties.Contains("Authorized Amount"), Is.False);
Assert.That(properties.Count, Is.EqualTo(4));

// 2 -  Remove by name:
properties.Remove("Authorized Revision");

Assert.That(properties.Contains("Authorized Revision"), Is.False);
Assert.That(properties.Count, Is.EqualTo(3));

// 3 -  Empty the entire collection at once:
properties.Clear();

Assert.That(properties.Count, Is.EqualTo(0));
```

### See Also

* class [DocumentProperty](../../documentproperty/)
* class [CustomDocumentProperties](../)
* namespace [Aspose.Words.Properties](../../../aspose.words.properties/)
* assembly [Aspose.Words](../../../)

---

## Add(*string, int*) {#add_2}

Creates a new custom document property of the Number data type.

```csharp
public DocumentProperty Add(string name, int value)
```

| Parameter | Type | Description |
| --- | --- | --- |
| name | String | The name of the property. |
| value | Int32 | The value of the property. |

### Return Value

The newly created property object.

## Examples

Shows how to work with a document's custom properties.

```csharp
Document doc = new Document();
CustomDocumentProperties properties = doc.CustomDocumentProperties;

Assert.That(properties.Count, Is.EqualTo(0));

// Custom document properties are key-value pairs that we can add to the document.
properties.Add("Authorized", true);
properties.Add("Authorized By", "John Doe");
properties.Add("Authorized Date", DateTime.Today);
properties.Add("Authorized Revision", doc.BuiltInDocumentProperties.RevisionNumber);
properties.Add("Authorized Amount", 123.45);

// The collection sorts the custom properties in alphabetic order.
Assert.That(properties.IndexOf("Authorized Amount"), Is.EqualTo(1));
Assert.That(properties.Count, Is.EqualTo(5));

// Print every custom property in the document.
using (IEnumerator<DocumentProperty> enumerator = properties.GetEnumerator())
{
    while (enumerator.MoveNext())
        Console.WriteLine($"Name: \"{enumerator.Current.Name}\"\n\tType: \"{enumerator.Current.Type}\"\n\tValue: \"{enumerator.Current.Value}\"");
}

// Display the value of a custom property using a DOCPROPERTY field.
DocumentBuilder builder = new DocumentBuilder(doc);
FieldDocProperty field = (FieldDocProperty)builder.InsertField(" DOCPROPERTY \"Authorized By\"");
field.Update();

Assert.That(field.Result, Is.EqualTo("John Doe"));

// We can find these custom properties in Microsoft Word via "File" -> "Properties" > "Advanced Properties" > "Custom".
doc.Save(ArtifactsDir + "DocumentProperties.DocumentPropertyCollection.docx");

// Below are three ways or removing custom properties from a document.
// 1 -  Remove by index:
properties.RemoveAt(1);

Assert.That(properties.Contains("Authorized Amount"), Is.False);
Assert.That(properties.Count, Is.EqualTo(4));

// 2 -  Remove by name:
properties.Remove("Authorized Revision");

Assert.That(properties.Contains("Authorized Revision"), Is.False);
Assert.That(properties.Count, Is.EqualTo(3));

// 3 -  Empty the entire collection at once:
properties.Clear();

Assert.That(properties.Count, Is.EqualTo(0));
```

### See Also

* class [DocumentProperty](../../documentproperty/)
* class [CustomDocumentProperties](../)
* namespace [Aspose.Words.Properties](../../../aspose.words.properties/)
* assembly [Aspose.Words](../../../)

---

## Add(*string, DateTime*) {#add_3}

Creates a new custom document property of the DateTime data type.

```csharp
public DocumentProperty Add(string name, DateTime value)
```

| Parameter | Type | Description |
| --- | --- | --- |
| name | String | The name of the property. |
| value | DateTime | The value of the property. |

### Return Value

The newly created property object.

## Examples

Shows how to create a custom document property which contains a date and time.

```csharp
Document doc = new Document();

doc.CustomDocumentProperties.Add("AuthorizationDate", DateTime.Now);
DateTime authorizationDate = doc.CustomDocumentProperties["AuthorizationDate"].ToDateTime();
Console.WriteLine($"Document authorized on {authorizationDate}");
```

Shows how to work with a document's custom properties.

```csharp
Document doc = new Document();
CustomDocumentProperties properties = doc.CustomDocumentProperties;

Assert.That(properties.Count, Is.EqualTo(0));

// Custom document properties are key-value pairs that we can add to the document.
properties.Add("Authorized", true);
properties.Add("Authorized By", "John Doe");
properties.Add("Authorized Date", DateTime.Today);
properties.Add("Authorized Revision", doc.BuiltInDocumentProperties.RevisionNumber);
properties.Add("Authorized Amount", 123.45);

// The collection sorts the custom properties in alphabetic order.
Assert.That(properties.IndexOf("Authorized Amount"), Is.EqualTo(1));
Assert.That(properties.Count, Is.EqualTo(5));

// Print every custom property in the document.
using (IEnumerator<DocumentProperty> enumerator = properties.GetEnumerator())
{
    while (enumerator.MoveNext())
        Console.WriteLine($"Name: \"{enumerator.Current.Name}\"\n\tType: \"{enumerator.Current.Type}\"\n\tValue: \"{enumerator.Current.Value}\"");
}

// Display the value of a custom property using a DOCPROPERTY field.
DocumentBuilder builder = new DocumentBuilder(doc);
FieldDocProperty field = (FieldDocProperty)builder.InsertField(" DOCPROPERTY \"Authorized By\"");
field.Update();

Assert.That(field.Result, Is.EqualTo("John Doe"));

// We can find these custom properties in Microsoft Word via "File" -> "Properties" > "Advanced Properties" > "Custom".
doc.Save(ArtifactsDir + "DocumentProperties.DocumentPropertyCollection.docx");

// Below are three ways or removing custom properties from a document.
// 1 -  Remove by index:
properties.RemoveAt(1);

Assert.That(properties.Contains("Authorized Amount"), Is.False);
Assert.That(properties.Count, Is.EqualTo(4));

// 2 -  Remove by name:
properties.Remove("Authorized Revision");

Assert.That(properties.Contains("Authorized Revision"), Is.False);
Assert.That(properties.Count, Is.EqualTo(3));

// 3 -  Empty the entire collection at once:
properties.Clear();

Assert.That(properties.Count, Is.EqualTo(0));
```

### See Also

* class [DocumentProperty](../../documentproperty/)
* class [CustomDocumentProperties](../)
* namespace [Aspose.Words.Properties](../../../aspose.words.properties/)
* assembly [Aspose.Words](../../../)

---

## Add(*string, bool*) {#add}

Creates a new custom document property of the Boolean data type.

```csharp
public DocumentProperty Add(string name, bool value)
```

| Parameter | Type | Description |
| --- | --- | --- |
| name | String | The name of the property. |
| value | Boolean | The value of the property. |

### Return Value

The newly created property object.

## Examples

Shows how to work with a document's custom properties.

```csharp
Document doc = new Document();
CustomDocumentProperties properties = doc.CustomDocumentProperties;

Assert.That(properties.Count, Is.EqualTo(0));

// Custom document properties are key-value pairs that we can add to the document.
properties.Add("Authorized", true);
properties.Add("Authorized By", "John Doe");
properties.Add("Authorized Date", DateTime.Today);
properties.Add("Authorized Revision", doc.BuiltInDocumentProperties.RevisionNumber);
properties.Add("Authorized Amount", 123.45);

// The collection sorts the custom properties in alphabetic order.
Assert.That(properties.IndexOf("Authorized Amount"), Is.EqualTo(1));
Assert.That(properties.Count, Is.EqualTo(5));

// Print every custom property in the document.
using (IEnumerator<DocumentProperty> enumerator = properties.GetEnumerator())
{
    while (enumerator.MoveNext())
        Console.WriteLine($"Name: \"{enumerator.Current.Name}\"\n\tType: \"{enumerator.Current.Type}\"\n\tValue: \"{enumerator.Current.Value}\"");
}

// Display the value of a custom property using a DOCPROPERTY field.
DocumentBuilder builder = new DocumentBuilder(doc);
FieldDocProperty field = (FieldDocProperty)builder.InsertField(" DOCPROPERTY \"Authorized By\"");
field.Update();

Assert.That(field.Result, Is.EqualTo("John Doe"));

// We can find these custom properties in Microsoft Word via "File" -> "Properties" > "Advanced Properties" > "Custom".
doc.Save(ArtifactsDir + "DocumentProperties.DocumentPropertyCollection.docx");

// Below are three ways or removing custom properties from a document.
// 1 -  Remove by index:
properties.RemoveAt(1);

Assert.That(properties.Contains("Authorized Amount"), Is.False);
Assert.That(properties.Count, Is.EqualTo(4));

// 2 -  Remove by name:
properties.Remove("Authorized Revision");

Assert.That(properties.Contains("Authorized Revision"), Is.False);
Assert.That(properties.Count, Is.EqualTo(3));

// 3 -  Empty the entire collection at once:
properties.Clear();

Assert.That(properties.Count, Is.EqualTo(0));
```

### See Also

* class [DocumentProperty](../../documentproperty/)
* class [CustomDocumentProperties](../)
* namespace [Aspose.Words.Properties](../../../aspose.words.properties/)
* assembly [Aspose.Words](../../../)

---

## Add(*string, double*) {#add_1}

Creates a new custom document property of the Double data type.

```csharp
public DocumentProperty Add(string name, double value)
```

| Parameter | Type | Description |
| --- | --- | --- |
| name | String | The name of the property. |
| value | Double | The value of the property. |

### Return Value

The newly created property object.

## Examples

Shows how to work with a document's custom properties.

```csharp
Document doc = new Document();
CustomDocumentProperties properties = doc.CustomDocumentProperties;

Assert.That(properties.Count, Is.EqualTo(0));

// Custom document properties are key-value pairs that we can add to the document.
properties.Add("Authorized", true);
properties.Add("Authorized By", "John Doe");
properties.Add("Authorized Date", DateTime.Today);
properties.Add("Authorized Revision", doc.BuiltInDocumentProperties.RevisionNumber);
properties.Add("Authorized Amount", 123.45);

// The collection sorts the custom properties in alphabetic order.
Assert.That(properties.IndexOf("Authorized Amount"), Is.EqualTo(1));
Assert.That(properties.Count, Is.EqualTo(5));

// Print every custom property in the document.
using (IEnumerator<DocumentProperty> enumerator = properties.GetEnumerator())
{
    while (enumerator.MoveNext())
        Console.WriteLine($"Name: \"{enumerator.Current.Name}\"\n\tType: \"{enumerator.Current.Type}\"\n\tValue: \"{enumerator.Current.Value}\"");
}

// Display the value of a custom property using a DOCPROPERTY field.
DocumentBuilder builder = new DocumentBuilder(doc);
FieldDocProperty field = (FieldDocProperty)builder.InsertField(" DOCPROPERTY \"Authorized By\"");
field.Update();

Assert.That(field.Result, Is.EqualTo("John Doe"));

// We can find these custom properties in Microsoft Word via "File" -> "Properties" > "Advanced Properties" > "Custom".
doc.Save(ArtifactsDir + "DocumentProperties.DocumentPropertyCollection.docx");

// Below are three ways or removing custom properties from a document.
// 1 -  Remove by index:
properties.RemoveAt(1);

Assert.That(properties.Contains("Authorized Amount"), Is.False);
Assert.That(properties.Count, Is.EqualTo(4));

// 2 -  Remove by name:
properties.Remove("Authorized Revision");

Assert.That(properties.Contains("Authorized Revision"), Is.False);
Assert.That(properties.Count, Is.EqualTo(3));

// 3 -  Empty the entire collection at once:
properties.Clear();

Assert.That(properties.Count, Is.EqualTo(0));
```

### See Also

* class [DocumentProperty](../../documentproperty/)
* class [CustomDocumentProperties](../)
* namespace [Aspose.Words.Properties](../../../aspose.words.properties/)
* assembly [Aspose.Words](../../../)
