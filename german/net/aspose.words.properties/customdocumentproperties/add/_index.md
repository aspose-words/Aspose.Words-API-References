---
title: CustomDocumentProperties.Add
linktitle: Add
articleTitle: Add
second_title: Aspose.Words für .NET
description: CustomDocumentProperties Add methode. Erstellt eine neue benutzerdefinierte Dokumenteigenschaft desString Datentyp in C#.
type: docs
weight: 10
url: /de/net/aspose.words.properties/customdocumentproperties/add/
---
## Add(*string, string*) {#add_4}

Erstellt eine neue benutzerdefinierte Dokumenteigenschaft desString Datentyp.

```csharp
public DocumentProperty Add(string name, string value)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| name | String | Der Name der Eigenschaft. |
| value | String | Der Wert der Immobilie. |

### Rückgabewert

Das neu erstellte Eigenschaftsobjekt.

## Beispiele

Zeigt, wie mit den benutzerdefinierten Eigenschaften eines Dokuments gearbeitet wird.

```csharp
Document doc = new Document();
CustomDocumentProperties properties = doc.CustomDocumentProperties;

Assert.AreEqual(0, properties.Count);

// Benutzerdefinierte Dokumenteigenschaften sind Schlüssel-Wert-Paare, die wir dem Dokument hinzufügen können.
properties.Add("Authorized", true);
properties.Add("Authorized By", "John Doe");
properties.Add("Authorized Date", DateTime.Today);
properties.Add("Authorized Revision", doc.BuiltInDocumentProperties.RevisionNumber);
properties.Add("Authorized Amount", 123.45);

// Die Sammlung sortiert die benutzerdefinierten Eigenschaften in alphabetischer Reihenfolge.
Assert.AreEqual(1, properties.IndexOf("Authorized Amount"));
Assert.AreEqual(5, properties.Count);

// Jede benutzerdefinierte Eigenschaft im Dokument drucken.
using (IEnumerator<DocumentProperty> enumerator = properties.GetEnumerator())
{
    while (enumerator.MoveNext())
        Console.WriteLine($"Name: \"{enumerator.Current.Name}\"\n\tType: \"{enumerator.Current.Type}\"\n\tValue: \"{enumerator.Current.Value}\"");
}

// Den Wert einer benutzerdefinierten Eigenschaft mithilfe eines DOCPROPERTY-Felds anzeigen.
DocumentBuilder builder = new DocumentBuilder(doc);
FieldDocProperty field = (FieldDocProperty)builder.InsertField(" DOCPROPERTY \"Authorized By\"");
field.Update();

Assert.AreEqual("John Doe", field.Result);

// Wir können diese benutzerdefinierten Eigenschaften in Microsoft Word über „Datei“ finden –> „Eigenschaften“ > „Erweiterte Eigenschaften“ > "Brauch".
doc.Save(ArtifactsDir + "DocumentProperties.DocumentPropertyCollection.docx");

// Im Folgenden finden Sie drei Möglichkeiten, benutzerdefinierte Eigenschaften aus einem Dokument zu entfernen.
// 1 - Nach Index entfernen:
properties.RemoveAt(1);

Assert.False(properties.Contains("Authorized Amount"));
Assert.AreEqual(4, properties.Count);

// 2 - Nach Namen entfernen:
properties.Remove("Authorized Revision");

Assert.False(properties.Contains("Authorized Revision"));
Assert.AreEqual(3, properties.Count);

// 3 – Die gesamte Sammlung auf einmal leeren:
properties.Clear();

Assert.AreEqual(0, properties.Count);
```

### Siehe auch

* class [DocumentProperty](../../documentproperty/)
* class [CustomDocumentProperties](../)
* namensraum [Aspose.Words.Properties](../../../aspose.words.properties/)
* Montage [Aspose.Words](../../../)

---

## Add(*string, int*) {#add_2}

Erstellt eine neue benutzerdefinierte Dokumenteigenschaft desNumber Datentyp.

```csharp
public DocumentProperty Add(string name, int value)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| name | String | Der Name der Eigenschaft. |
| value | Int32 | Der Wert der Immobilie. |

### Rückgabewert

Das neu erstellte Eigenschaftsobjekt.

## Beispiele

Zeigt, wie mit den benutzerdefinierten Eigenschaften eines Dokuments gearbeitet wird.

```csharp
Document doc = new Document();
CustomDocumentProperties properties = doc.CustomDocumentProperties;

Assert.AreEqual(0, properties.Count);

// Benutzerdefinierte Dokumenteigenschaften sind Schlüssel-Wert-Paare, die wir dem Dokument hinzufügen können.
properties.Add("Authorized", true);
properties.Add("Authorized By", "John Doe");
properties.Add("Authorized Date", DateTime.Today);
properties.Add("Authorized Revision", doc.BuiltInDocumentProperties.RevisionNumber);
properties.Add("Authorized Amount", 123.45);

// Die Sammlung sortiert die benutzerdefinierten Eigenschaften in alphabetischer Reihenfolge.
Assert.AreEqual(1, properties.IndexOf("Authorized Amount"));
Assert.AreEqual(5, properties.Count);

// Jede benutzerdefinierte Eigenschaft im Dokument drucken.
using (IEnumerator<DocumentProperty> enumerator = properties.GetEnumerator())
{
    while (enumerator.MoveNext())
        Console.WriteLine($"Name: \"{enumerator.Current.Name}\"\n\tType: \"{enumerator.Current.Type}\"\n\tValue: \"{enumerator.Current.Value}\"");
}

// Den Wert einer benutzerdefinierten Eigenschaft mithilfe eines DOCPROPERTY-Felds anzeigen.
DocumentBuilder builder = new DocumentBuilder(doc);
FieldDocProperty field = (FieldDocProperty)builder.InsertField(" DOCPROPERTY \"Authorized By\"");
field.Update();

Assert.AreEqual("John Doe", field.Result);

// Wir können diese benutzerdefinierten Eigenschaften in Microsoft Word über „Datei“ finden –> „Eigenschaften“ > „Erweiterte Eigenschaften“ > "Brauch".
doc.Save(ArtifactsDir + "DocumentProperties.DocumentPropertyCollection.docx");

// Im Folgenden finden Sie drei Möglichkeiten, benutzerdefinierte Eigenschaften aus einem Dokument zu entfernen.
// 1 - Nach Index entfernen:
properties.RemoveAt(1);

Assert.False(properties.Contains("Authorized Amount"));
Assert.AreEqual(4, properties.Count);

// 2 - Nach Namen entfernen:
properties.Remove("Authorized Revision");

Assert.False(properties.Contains("Authorized Revision"));
Assert.AreEqual(3, properties.Count);

// 3 – Die gesamte Sammlung auf einmal leeren:
properties.Clear();

Assert.AreEqual(0, properties.Count);
```

### Siehe auch

* class [DocumentProperty](../../documentproperty/)
* class [CustomDocumentProperties](../)
* namensraum [Aspose.Words.Properties](../../../aspose.words.properties/)
* Montage [Aspose.Words](../../../)

---

## Add(*string, DateTime*) {#add_3}

Erstellt eine neue benutzerdefinierte Dokumenteigenschaft desDateTime Datentyp.

```csharp
public DocumentProperty Add(string name, DateTime value)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| name | String | Der Name der Eigenschaft. |
| value | DateTime | Der Wert der Immobilie. |

### Rückgabewert

Das neu erstellte Eigenschaftsobjekt.

## Beispiele

Zeigt, wie eine benutzerdefinierte Dokumenteigenschaft erstellt wird, die ein Datum und eine Uhrzeit enthält.

```csharp
Document doc = new Document();

doc.CustomDocumentProperties.Add("AuthorizationDate", DateTime.Now);

Console.WriteLine($"Document authorized on {doc.CustomDocumentProperties["AuthorizationDate"].ToDateTime()}");
```

Zeigt, wie mit den benutzerdefinierten Eigenschaften eines Dokuments gearbeitet wird.

```csharp
Document doc = new Document();
CustomDocumentProperties properties = doc.CustomDocumentProperties;

Assert.AreEqual(0, properties.Count);

// Benutzerdefinierte Dokumenteigenschaften sind Schlüssel-Wert-Paare, die wir dem Dokument hinzufügen können.
properties.Add("Authorized", true);
properties.Add("Authorized By", "John Doe");
properties.Add("Authorized Date", DateTime.Today);
properties.Add("Authorized Revision", doc.BuiltInDocumentProperties.RevisionNumber);
properties.Add("Authorized Amount", 123.45);

// Die Sammlung sortiert die benutzerdefinierten Eigenschaften in alphabetischer Reihenfolge.
Assert.AreEqual(1, properties.IndexOf("Authorized Amount"));
Assert.AreEqual(5, properties.Count);

// Jede benutzerdefinierte Eigenschaft im Dokument drucken.
using (IEnumerator<DocumentProperty> enumerator = properties.GetEnumerator())
{
    while (enumerator.MoveNext())
        Console.WriteLine($"Name: \"{enumerator.Current.Name}\"\n\tType: \"{enumerator.Current.Type}\"\n\tValue: \"{enumerator.Current.Value}\"");
}

// Den Wert einer benutzerdefinierten Eigenschaft mithilfe eines DOCPROPERTY-Felds anzeigen.
DocumentBuilder builder = new DocumentBuilder(doc);
FieldDocProperty field = (FieldDocProperty)builder.InsertField(" DOCPROPERTY \"Authorized By\"");
field.Update();

Assert.AreEqual("John Doe", field.Result);

// Wir können diese benutzerdefinierten Eigenschaften in Microsoft Word über „Datei“ finden –> „Eigenschaften“ > „Erweiterte Eigenschaften“ > "Brauch".
doc.Save(ArtifactsDir + "DocumentProperties.DocumentPropertyCollection.docx");

// Im Folgenden finden Sie drei Möglichkeiten, benutzerdefinierte Eigenschaften aus einem Dokument zu entfernen.
// 1 - Nach Index entfernen:
properties.RemoveAt(1);

Assert.False(properties.Contains("Authorized Amount"));
Assert.AreEqual(4, properties.Count);

// 2 - Nach Namen entfernen:
properties.Remove("Authorized Revision");

Assert.False(properties.Contains("Authorized Revision"));
Assert.AreEqual(3, properties.Count);

// 3 – Die gesamte Sammlung auf einmal leeren:
properties.Clear();

Assert.AreEqual(0, properties.Count);
```

### Siehe auch

* class [DocumentProperty](../../documentproperty/)
* class [CustomDocumentProperties](../)
* namensraum [Aspose.Words.Properties](../../../aspose.words.properties/)
* Montage [Aspose.Words](../../../)

---

## Add(*string, bool*) {#add}

Erstellt eine neue benutzerdefinierte Dokumenteigenschaft desBoolean Datentyp.

```csharp
public DocumentProperty Add(string name, bool value)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| name | String | Der Name der Eigenschaft. |
| value | Boolean | Der Wert der Immobilie. |

### Rückgabewert

Das neu erstellte Eigenschaftsobjekt.

## Beispiele

Zeigt, wie mit den benutzerdefinierten Eigenschaften eines Dokuments gearbeitet wird.

```csharp
Document doc = new Document();
CustomDocumentProperties properties = doc.CustomDocumentProperties;

Assert.AreEqual(0, properties.Count);

// Benutzerdefinierte Dokumenteigenschaften sind Schlüssel-Wert-Paare, die wir dem Dokument hinzufügen können.
properties.Add("Authorized", true);
properties.Add("Authorized By", "John Doe");
properties.Add("Authorized Date", DateTime.Today);
properties.Add("Authorized Revision", doc.BuiltInDocumentProperties.RevisionNumber);
properties.Add("Authorized Amount", 123.45);

// Die Sammlung sortiert die benutzerdefinierten Eigenschaften in alphabetischer Reihenfolge.
Assert.AreEqual(1, properties.IndexOf("Authorized Amount"));
Assert.AreEqual(5, properties.Count);

// Jede benutzerdefinierte Eigenschaft im Dokument drucken.
using (IEnumerator<DocumentProperty> enumerator = properties.GetEnumerator())
{
    while (enumerator.MoveNext())
        Console.WriteLine($"Name: \"{enumerator.Current.Name}\"\n\tType: \"{enumerator.Current.Type}\"\n\tValue: \"{enumerator.Current.Value}\"");
}

// Den Wert einer benutzerdefinierten Eigenschaft mithilfe eines DOCPROPERTY-Felds anzeigen.
DocumentBuilder builder = new DocumentBuilder(doc);
FieldDocProperty field = (FieldDocProperty)builder.InsertField(" DOCPROPERTY \"Authorized By\"");
field.Update();

Assert.AreEqual("John Doe", field.Result);

// Wir können diese benutzerdefinierten Eigenschaften in Microsoft Word über „Datei“ finden –> „Eigenschaften“ > „Erweiterte Eigenschaften“ > "Brauch".
doc.Save(ArtifactsDir + "DocumentProperties.DocumentPropertyCollection.docx");

// Im Folgenden finden Sie drei Möglichkeiten, benutzerdefinierte Eigenschaften aus einem Dokument zu entfernen.
// 1 - Nach Index entfernen:
properties.RemoveAt(1);

Assert.False(properties.Contains("Authorized Amount"));
Assert.AreEqual(4, properties.Count);

// 2 - Nach Namen entfernen:
properties.Remove("Authorized Revision");

Assert.False(properties.Contains("Authorized Revision"));
Assert.AreEqual(3, properties.Count);

// 3 – Die gesamte Sammlung auf einmal leeren:
properties.Clear();

Assert.AreEqual(0, properties.Count);
```

### Siehe auch

* class [DocumentProperty](../../documentproperty/)
* class [CustomDocumentProperties](../)
* namensraum [Aspose.Words.Properties](../../../aspose.words.properties/)
* Montage [Aspose.Words](../../../)

---

## Add(*string, double*) {#add_1}

Erstellt eine neue benutzerdefinierte Dokumenteigenschaft desDouble Datentyp.

```csharp
public DocumentProperty Add(string name, double value)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| name | String | Der Name der Eigenschaft. |
| value | Double | Der Wert der Immobilie. |

### Rückgabewert

Das neu erstellte Eigenschaftsobjekt.

## Beispiele

Zeigt, wie mit den benutzerdefinierten Eigenschaften eines Dokuments gearbeitet wird.

```csharp
Document doc = new Document();
CustomDocumentProperties properties = doc.CustomDocumentProperties;

Assert.AreEqual(0, properties.Count);

// Benutzerdefinierte Dokumenteigenschaften sind Schlüssel-Wert-Paare, die wir dem Dokument hinzufügen können.
properties.Add("Authorized", true);
properties.Add("Authorized By", "John Doe");
properties.Add("Authorized Date", DateTime.Today);
properties.Add("Authorized Revision", doc.BuiltInDocumentProperties.RevisionNumber);
properties.Add("Authorized Amount", 123.45);

// Die Sammlung sortiert die benutzerdefinierten Eigenschaften in alphabetischer Reihenfolge.
Assert.AreEqual(1, properties.IndexOf("Authorized Amount"));
Assert.AreEqual(5, properties.Count);

// Jede benutzerdefinierte Eigenschaft im Dokument drucken.
using (IEnumerator<DocumentProperty> enumerator = properties.GetEnumerator())
{
    while (enumerator.MoveNext())
        Console.WriteLine($"Name: \"{enumerator.Current.Name}\"\n\tType: \"{enumerator.Current.Type}\"\n\tValue: \"{enumerator.Current.Value}\"");
}

// Den Wert einer benutzerdefinierten Eigenschaft mithilfe eines DOCPROPERTY-Felds anzeigen.
DocumentBuilder builder = new DocumentBuilder(doc);
FieldDocProperty field = (FieldDocProperty)builder.InsertField(" DOCPROPERTY \"Authorized By\"");
field.Update();

Assert.AreEqual("John Doe", field.Result);

// Wir können diese benutzerdefinierten Eigenschaften in Microsoft Word über „Datei“ finden –> „Eigenschaften“ > „Erweiterte Eigenschaften“ > "Brauch".
doc.Save(ArtifactsDir + "DocumentProperties.DocumentPropertyCollection.docx");

// Im Folgenden finden Sie drei Möglichkeiten, benutzerdefinierte Eigenschaften aus einem Dokument zu entfernen.
// 1 - Nach Index entfernen:
properties.RemoveAt(1);

Assert.False(properties.Contains("Authorized Amount"));
Assert.AreEqual(4, properties.Count);

// 2 - Nach Namen entfernen:
properties.Remove("Authorized Revision");

Assert.False(properties.Contains("Authorized Revision"));
Assert.AreEqual(3, properties.Count);

// 3 – Die gesamte Sammlung auf einmal leeren:
properties.Clear();

Assert.AreEqual(0, properties.Count);
```

### Siehe auch

* class [DocumentProperty](../../documentproperty/)
* class [CustomDocumentProperties](../)
* namensraum [Aspose.Words.Properties](../../../aspose.words.properties/)
* Montage [Aspose.Words](../../../)
