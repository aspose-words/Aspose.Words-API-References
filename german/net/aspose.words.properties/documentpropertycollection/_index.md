---
title: DocumentPropertyCollection Class
linktitle: DocumentPropertyCollection
articleTitle: DocumentPropertyCollection
second_title: Aspose.Words für .NET
description: Aspose.Words.Properties.DocumentPropertyCollection klas. Basisklasse fürBuiltInDocumentProperties UndCustomDocumentProperties Sammlungen in C#.
type: docs
weight: 4480
url: /de/net/aspose.words.properties/documentpropertycollection/
---
## DocumentPropertyCollection class

Basisklasse für[`BuiltInDocumentProperties`](../builtindocumentproperties/) Und[`CustomDocumentProperties`](../customdocumentproperties/) Sammlungen.

Um mehr zu erfahren, besuchen Sie die[Arbeiten Sie mit Dokumenteigenschaften](https://docs.aspose.com/words/net/work-with-document-properties/) Dokumentationsartikel.

```csharp
public abstract class DocumentPropertyCollection : IEnumerable<DocumentProperty>
```

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| [Count](../../aspose.words.properties/documentpropertycollection/count/) { get; } | Ruft die Anzahl der Elemente in der Sammlung ab. |
| [Item](../../aspose.words.properties/documentpropertycollection/item/) { get; } | Gibt a zurück[`DocumentProperty`](../documentproperty/) Objekt nach index. |
| virtual [Item](../../aspose.words.properties/documentpropertycollection/item/) { get; } | Gibt a zurück[`DocumentProperty`](../documentproperty/) Objekt mit dem Namen der Eigenschaft. |

## Methoden

| Name | Beschreibung |
| --- | --- |
| [Clear](../../aspose.words.properties/documentpropertycollection/clear/)() | Entfernt alle Eigenschaften aus der Sammlung. |
| [Contains](../../aspose.words.properties/documentpropertycollection/contains/)(*string*) | Gibt zurück`WAHR` wenn eine Eigenschaft mit dem angegebenen Namen in der Sammlung vorhanden ist. |
| [GetEnumerator](../../aspose.words.properties/documentpropertycollection/getenumerator/)() | Gibt ein Enumeratorobjekt zurück, das zum Durchlaufen aller Elemente in der Sammlung verwendet werden kann. |
| [IndexOf](../../aspose.words.properties/documentpropertycollection/indexof/)(*string*) | Ruft den Index einer Eigenschaft nach Namen ab. |
| [Remove](../../aspose.words.properties/documentpropertycollection/remove/)(*string*) | Entfernt eine Eigenschaft mit dem angegebenen Namen aus der Sammlung. |
| [RemoveAt](../../aspose.words.properties/documentpropertycollection/removeat/)(*int*) | Entfernt eine Eigenschaft am angegebenen Index. |

## Bemerkungen

Bei den Namen der Eigenschaften wird die Groß-/Kleinschreibung nicht beachtet.

Die Eigenschaften in der Sammlung werden alphabetisch nach Namen sortiert.

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

* class [BuiltInDocumentProperties](../builtindocumentproperties/)
* class [CustomDocumentProperties](../customdocumentproperties/)
* class [DocumentProperty](../documentproperty/)
* namensraum [Aspose.Words.Properties](../../aspose.words.properties/)
* Montage [Aspose.Words](../../)
