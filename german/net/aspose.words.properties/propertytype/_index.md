---
title: Enum PropertyType
second_title: Aspose.Words für .NET-API-Referenz
description: Aspose.Words.Properties.PropertyType opsomming. Gibt den Datentyp einer Dokumenteigenschaft an.
type: docs
weight: 4500
url: /de/net/aspose.words.properties/propertytype/
---
## PropertyType enumeration

Gibt den Datentyp einer Dokumenteigenschaft an.

```csharp
public enum PropertyType
```

### Werte

| Name | Wert | Beschreibung |
| --- | --- | --- |
| Boolean | `0` | Die Eigenschaft ist ein boolescher Wert. |
| DateTime | `1` | Die Eigenschaft ist ein Datum-Uhrzeit-Wert. |
| Double | `2` | Die Eigenschaft ist eine Gleitkommazahl. |
| Number | `3` | Die Eigenschaft ist eine Ganzzahl. |
| String | `4` | Die Eigenschaft ist ein Zeichenfolgenwert. |
| StringArray | `5` | Die Eigenschaft ist ein Array von Strings. |
| ObjectArray | `6` | Die Eigenschaft ist ein Array von Objekten. |
| ByteArray | `7` | Die Eigenschaft ist ein Array von Bytes. |
| Other | `8` | Die Eigenschaft ist von einem anderen Typ. |

### Beispiele

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

* class [DocumentProperty](../documentproperty/)
* property [Type](../documentproperty/type/)
* namensraum [Aspose.Words.Properties](../../aspose.words.properties/)
* Montage [Aspose.Words](../../)


