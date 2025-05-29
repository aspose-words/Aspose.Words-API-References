---
title: CustomDocumentProperties.Add
linktitle: Add
articleTitle: Add
second_title: Aspose.Words för .NET
description: Skapa unika anpassade dokumentegenskaper utan problem med Add-metoden. Förbättra dina dokument med skräddarsydda String-datatyper för optimal prestanda.
type: docs
weight: 10
url: /sv/net/aspose.words.properties/customdocumentproperties/add/
---
## Add(*string, string*) {#add_4}

Skapar en ny anpassad dokumentegenskap förString datatyp.

```csharp
public DocumentProperty Add(string name, string value)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| name | String | Fastighetens namn. |
| value | String | Fastighetens värde. |

### Returvärde

Det nyskapade egenskapsobjektet.

## Exempel

Visar hur man arbetar med ett dokuments anpassade egenskaper.

```csharp
Document doc = new Document();
CustomDocumentProperties properties = doc.CustomDocumentProperties;

Assert.AreEqual(0, properties.Count);

// Anpassade dokumentegenskaper är nyckel-värde-par som vi kan lägga till i dokumentet.
properties.Add("Authorized", true);
properties.Add("Authorized By", "John Doe");
properties.Add("Authorized Date", DateTime.Today);
properties.Add("Authorized Revision", doc.BuiltInDocumentProperties.RevisionNumber);
properties.Add("Authorized Amount", 123.45);

// Samlingen sorterar de anpassade egenskaperna i alfabetisk ordning.
Assert.AreEqual(1, properties.IndexOf("Authorized Amount"));
Assert.AreEqual(5, properties.Count);

// Skriv ut alla anpassade egenskaper i dokumentet.
using (IEnumerator<DocumentProperty> enumerator = properties.GetEnumerator())
{
    while (enumerator.MoveNext())
        Console.WriteLine($"Name: \"{enumerator.Current.Name}\"\n\tType: \"{enumerator.Current.Type}\"\n\tValue: \"{enumerator.Current.Value}\"");
}

// Visa värdet för en anpassad egenskap med hjälp av ett DOCPROPERTY-fält.
DocumentBuilder builder = new DocumentBuilder(doc);
FieldDocProperty field = (FieldDocProperty)builder.InsertField(" DOCPROPERTY \"Authorized By\"");
field.Update();

Assert.AreEqual("John Doe", field.Result);

// Vi hittar dessa anpassade egenskaper i Microsoft Word via "Arkiv" -> "Egenskaper" > "Avancerade egenskaper" > "Anpassad".
doc.Save(ArtifactsDir + "DocumentProperties.DocumentPropertyCollection.docx");

// Nedan följer tre sätt att ta bort anpassade egenskaper från ett dokument.
// 1 - Ta bort via index:
properties.RemoveAt(1);

Assert.False(properties.Contains("Authorized Amount"));
Assert.AreEqual(4, properties.Count);

// 2 - Ta bort efter namn:
properties.Remove("Authorized Revision");

Assert.False(properties.Contains("Authorized Revision"));
Assert.AreEqual(3, properties.Count);

// 3 - Töm hela samlingen på en gång:
properties.Clear();

Assert.AreEqual(0, properties.Count);
```

### Se även

* class [DocumentProperty](../../documentproperty/)
* class [CustomDocumentProperties](../)
* namnutrymme [Aspose.Words.Properties](../../../aspose.words.properties/)
* hopsättning [Aspose.Words](../../../)

---

## Add(*string, int*) {#add_2}

Skapar en ny anpassad dokumentegenskap förNumber datatyp.

```csharp
public DocumentProperty Add(string name, int value)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| name | String | Fastighetens namn. |
| value | Int32 | Fastighetens värde. |

### Returvärde

Det nyskapade egenskapsobjektet.

## Exempel

Visar hur man arbetar med ett dokuments anpassade egenskaper.

```csharp
Document doc = new Document();
CustomDocumentProperties properties = doc.CustomDocumentProperties;

Assert.AreEqual(0, properties.Count);

// Anpassade dokumentegenskaper är nyckel-värde-par som vi kan lägga till i dokumentet.
properties.Add("Authorized", true);
properties.Add("Authorized By", "John Doe");
properties.Add("Authorized Date", DateTime.Today);
properties.Add("Authorized Revision", doc.BuiltInDocumentProperties.RevisionNumber);
properties.Add("Authorized Amount", 123.45);

// Samlingen sorterar de anpassade egenskaperna i alfabetisk ordning.
Assert.AreEqual(1, properties.IndexOf("Authorized Amount"));
Assert.AreEqual(5, properties.Count);

// Skriv ut alla anpassade egenskaper i dokumentet.
using (IEnumerator<DocumentProperty> enumerator = properties.GetEnumerator())
{
    while (enumerator.MoveNext())
        Console.WriteLine($"Name: \"{enumerator.Current.Name}\"\n\tType: \"{enumerator.Current.Type}\"\n\tValue: \"{enumerator.Current.Value}\"");
}

// Visa värdet för en anpassad egenskap med hjälp av ett DOCPROPERTY-fält.
DocumentBuilder builder = new DocumentBuilder(doc);
FieldDocProperty field = (FieldDocProperty)builder.InsertField(" DOCPROPERTY \"Authorized By\"");
field.Update();

Assert.AreEqual("John Doe", field.Result);

// Vi hittar dessa anpassade egenskaper i Microsoft Word via "Arkiv" -> "Egenskaper" > "Avancerade egenskaper" > "Anpassad".
doc.Save(ArtifactsDir + "DocumentProperties.DocumentPropertyCollection.docx");

// Nedan följer tre sätt att ta bort anpassade egenskaper från ett dokument.
// 1 - Ta bort via index:
properties.RemoveAt(1);

Assert.False(properties.Contains("Authorized Amount"));
Assert.AreEqual(4, properties.Count);

// 2 - Ta bort efter namn:
properties.Remove("Authorized Revision");

Assert.False(properties.Contains("Authorized Revision"));
Assert.AreEqual(3, properties.Count);

// 3 - Töm hela samlingen på en gång:
properties.Clear();

Assert.AreEqual(0, properties.Count);
```

### Se även

* class [DocumentProperty](../../documentproperty/)
* class [CustomDocumentProperties](../)
* namnutrymme [Aspose.Words.Properties](../../../aspose.words.properties/)
* hopsättning [Aspose.Words](../../../)

---

## Add(*string, DateTime*) {#add_3}

Skapar en ny anpassad dokumentegenskap förDateTime datatyp.

```csharp
public DocumentProperty Add(string name, DateTime value)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| name | String | Fastighetens namn. |
| value | DateTime | Fastighetens värde. |

### Returvärde

Det nyskapade egenskapsobjektet.

## Exempel

Visar hur man skapar en anpassad dokumentegenskap som innehåller datum och tid.

```csharp
Document doc = new Document();

doc.CustomDocumentProperties.Add("AuthorizationDate", DateTime.Now);
DateTime authorizationDate = doc.CustomDocumentProperties["AuthorizationDate"].ToDateTime();
Console.WriteLine($"Document authorized on {authorizationDate}");
```

Visar hur man arbetar med ett dokuments anpassade egenskaper.

```csharp
Document doc = new Document();
CustomDocumentProperties properties = doc.CustomDocumentProperties;

Assert.AreEqual(0, properties.Count);

// Anpassade dokumentegenskaper är nyckel-värde-par som vi kan lägga till i dokumentet.
properties.Add("Authorized", true);
properties.Add("Authorized By", "John Doe");
properties.Add("Authorized Date", DateTime.Today);
properties.Add("Authorized Revision", doc.BuiltInDocumentProperties.RevisionNumber);
properties.Add("Authorized Amount", 123.45);

// Samlingen sorterar de anpassade egenskaperna i alfabetisk ordning.
Assert.AreEqual(1, properties.IndexOf("Authorized Amount"));
Assert.AreEqual(5, properties.Count);

// Skriv ut alla anpassade egenskaper i dokumentet.
using (IEnumerator<DocumentProperty> enumerator = properties.GetEnumerator())
{
    while (enumerator.MoveNext())
        Console.WriteLine($"Name: \"{enumerator.Current.Name}\"\n\tType: \"{enumerator.Current.Type}\"\n\tValue: \"{enumerator.Current.Value}\"");
}

// Visa värdet för en anpassad egenskap med hjälp av ett DOCPROPERTY-fält.
DocumentBuilder builder = new DocumentBuilder(doc);
FieldDocProperty field = (FieldDocProperty)builder.InsertField(" DOCPROPERTY \"Authorized By\"");
field.Update();

Assert.AreEqual("John Doe", field.Result);

// Vi hittar dessa anpassade egenskaper i Microsoft Word via "Arkiv" -> "Egenskaper" > "Avancerade egenskaper" > "Anpassad".
doc.Save(ArtifactsDir + "DocumentProperties.DocumentPropertyCollection.docx");

// Nedan följer tre sätt att ta bort anpassade egenskaper från ett dokument.
// 1 - Ta bort via index:
properties.RemoveAt(1);

Assert.False(properties.Contains("Authorized Amount"));
Assert.AreEqual(4, properties.Count);

// 2 - Ta bort efter namn:
properties.Remove("Authorized Revision");

Assert.False(properties.Contains("Authorized Revision"));
Assert.AreEqual(3, properties.Count);

// 3 - Töm hela samlingen på en gång:
properties.Clear();

Assert.AreEqual(0, properties.Count);
```

### Se även

* class [DocumentProperty](../../documentproperty/)
* class [CustomDocumentProperties](../)
* namnutrymme [Aspose.Words.Properties](../../../aspose.words.properties/)
* hopsättning [Aspose.Words](../../../)

---

## Add(*string, bool*) {#add}

Skapar en ny anpassad dokumentegenskap förBoolean datatyp.

```csharp
public DocumentProperty Add(string name, bool value)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| name | String | Fastighetens namn. |
| value | Boolean | Fastighetens värde. |

### Returvärde

Det nyskapade egenskapsobjektet.

## Exempel

Visar hur man arbetar med ett dokuments anpassade egenskaper.

```csharp
Document doc = new Document();
CustomDocumentProperties properties = doc.CustomDocumentProperties;

Assert.AreEqual(0, properties.Count);

// Anpassade dokumentegenskaper är nyckel-värde-par som vi kan lägga till i dokumentet.
properties.Add("Authorized", true);
properties.Add("Authorized By", "John Doe");
properties.Add("Authorized Date", DateTime.Today);
properties.Add("Authorized Revision", doc.BuiltInDocumentProperties.RevisionNumber);
properties.Add("Authorized Amount", 123.45);

// Samlingen sorterar de anpassade egenskaperna i alfabetisk ordning.
Assert.AreEqual(1, properties.IndexOf("Authorized Amount"));
Assert.AreEqual(5, properties.Count);

// Skriv ut alla anpassade egenskaper i dokumentet.
using (IEnumerator<DocumentProperty> enumerator = properties.GetEnumerator())
{
    while (enumerator.MoveNext())
        Console.WriteLine($"Name: \"{enumerator.Current.Name}\"\n\tType: \"{enumerator.Current.Type}\"\n\tValue: \"{enumerator.Current.Value}\"");
}

// Visa värdet för en anpassad egenskap med hjälp av ett DOCPROPERTY-fält.
DocumentBuilder builder = new DocumentBuilder(doc);
FieldDocProperty field = (FieldDocProperty)builder.InsertField(" DOCPROPERTY \"Authorized By\"");
field.Update();

Assert.AreEqual("John Doe", field.Result);

// Vi hittar dessa anpassade egenskaper i Microsoft Word via "Arkiv" -> "Egenskaper" > "Avancerade egenskaper" > "Anpassad".
doc.Save(ArtifactsDir + "DocumentProperties.DocumentPropertyCollection.docx");

// Nedan följer tre sätt att ta bort anpassade egenskaper från ett dokument.
// 1 - Ta bort via index:
properties.RemoveAt(1);

Assert.False(properties.Contains("Authorized Amount"));
Assert.AreEqual(4, properties.Count);

// 2 - Ta bort efter namn:
properties.Remove("Authorized Revision");

Assert.False(properties.Contains("Authorized Revision"));
Assert.AreEqual(3, properties.Count);

// 3 - Töm hela samlingen på en gång:
properties.Clear();

Assert.AreEqual(0, properties.Count);
```

### Se även

* class [DocumentProperty](../../documentproperty/)
* class [CustomDocumentProperties](../)
* namnutrymme [Aspose.Words.Properties](../../../aspose.words.properties/)
* hopsättning [Aspose.Words](../../../)

---

## Add(*string, double*) {#add_1}

Skapar en ny anpassad dokumentegenskap förDouble datatyp.

```csharp
public DocumentProperty Add(string name, double value)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| name | String | Fastighetens namn. |
| value | Double | Fastighetens värde. |

### Returvärde

Det nyskapade egenskapsobjektet.

## Exempel

Visar hur man arbetar med ett dokuments anpassade egenskaper.

```csharp
Document doc = new Document();
CustomDocumentProperties properties = doc.CustomDocumentProperties;

Assert.AreEqual(0, properties.Count);

// Anpassade dokumentegenskaper är nyckel-värde-par som vi kan lägga till i dokumentet.
properties.Add("Authorized", true);
properties.Add("Authorized By", "John Doe");
properties.Add("Authorized Date", DateTime.Today);
properties.Add("Authorized Revision", doc.BuiltInDocumentProperties.RevisionNumber);
properties.Add("Authorized Amount", 123.45);

// Samlingen sorterar de anpassade egenskaperna i alfabetisk ordning.
Assert.AreEqual(1, properties.IndexOf("Authorized Amount"));
Assert.AreEqual(5, properties.Count);

// Skriv ut alla anpassade egenskaper i dokumentet.
using (IEnumerator<DocumentProperty> enumerator = properties.GetEnumerator())
{
    while (enumerator.MoveNext())
        Console.WriteLine($"Name: \"{enumerator.Current.Name}\"\n\tType: \"{enumerator.Current.Type}\"\n\tValue: \"{enumerator.Current.Value}\"");
}

// Visa värdet för en anpassad egenskap med hjälp av ett DOCPROPERTY-fält.
DocumentBuilder builder = new DocumentBuilder(doc);
FieldDocProperty field = (FieldDocProperty)builder.InsertField(" DOCPROPERTY \"Authorized By\"");
field.Update();

Assert.AreEqual("John Doe", field.Result);

// Vi hittar dessa anpassade egenskaper i Microsoft Word via "Arkiv" -> "Egenskaper" > "Avancerade egenskaper" > "Anpassad".
doc.Save(ArtifactsDir + "DocumentProperties.DocumentPropertyCollection.docx");

// Nedan följer tre sätt att ta bort anpassade egenskaper från ett dokument.
// 1 - Ta bort via index:
properties.RemoveAt(1);

Assert.False(properties.Contains("Authorized Amount"));
Assert.AreEqual(4, properties.Count);

// 2 - Ta bort efter namn:
properties.Remove("Authorized Revision");

Assert.False(properties.Contains("Authorized Revision"));
Assert.AreEqual(3, properties.Count);

// 3 - Töm hela samlingen på en gång:
properties.Clear();

Assert.AreEqual(0, properties.Count);
```

### Se även

* class [DocumentProperty](../../documentproperty/)
* class [CustomDocumentProperties](../)
* namnutrymme [Aspose.Words.Properties](../../../aspose.words.properties/)
* hopsättning [Aspose.Words](../../../)
