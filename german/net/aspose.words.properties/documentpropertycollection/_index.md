---
title: DocumentPropertyCollection Class
linktitle: DocumentPropertyCollection
articleTitle: DocumentPropertyCollection
second_title: Aspose.Words für .NET
description: Entdecken Sie die Klasse Aspose.Words.Properties.DocumentPropertyCollection, Ihre Anlaufstelle für die effiziente Verwaltung integrierter und benutzerdefinierter Dokumenteigenschaften.
type: docs
weight: 5210
url: /de/net/aspose.words.properties/documentpropertycollection/
---
## DocumentPropertyCollection class

Basisklasse für[`BuiltInDocumentProperties`](../builtindocumentproperties/) Und[`CustomDocumentProperties`](../customdocumentproperties/) Sammlungen.

Um mehr zu erfahren, besuchen Sie die[Arbeiten mit Dokumenteigenschaften](https://docs.aspose.com/words/net/work-with-document-properties/) Dokumentationsartikel.

```csharp
public abstract class DocumentPropertyCollection : IEnumerable<DocumentProperty>
```

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| [Count](../../aspose.words.properties/documentpropertycollection/count/) { get; } | Ruft die Anzahl der Elemente in der Sammlung ab. |
| [Item](../../aspose.words.properties/documentpropertycollection/item/) { get; } | Gibt einen[`DocumentProperty`](../documentproperty/) Objekt nach Index. |
| virtual [Item](../../aspose.words.properties/documentpropertycollection/item/) { get; } | Gibt einen[`DocumentProperty`](../documentproperty/) Objekt durch den Namen der Eigenschaft. |

## Methoden

| Name | Beschreibung |
| --- | --- |
| [Clear](../../aspose.words.properties/documentpropertycollection/clear/)() | Entfernt alle Eigenschaften aus der Sammlung. |
| [Contains](../../aspose.words.properties/documentpropertycollection/contains/)(*string*) | Rückgaben`WAHR` wenn eine Eigenschaft mit dem angegebenen Namen in der Sammlung vorhanden ist. |
| [GetEnumerator](../../aspose.words.properties/documentpropertycollection/getenumerator/)() | Gibt ein Enumeratorobjekt zurück, mit dem alle Elemente in der Sammlung durchlaufen werden können. |
| [IndexOf](../../aspose.words.properties/documentpropertycollection/indexof/)(*string*) | Ruft den Index einer Eigenschaft nach Namen ab. |
| [Remove](../../aspose.words.properties/documentpropertycollection/remove/)(*string*) | Entfernt eine Eigenschaft mit dem angegebenen Namen aus der Sammlung. |
| [RemoveAt](../../aspose.words.properties/documentpropertycollection/removeat/)(*int*) | Entfernt eine Eigenschaft am angegebenen Index. |

## Bemerkungen

Bei den Namen der Eigenschaften wird die Groß- und Kleinschreibung nicht berücksichtigt.

Die Eigenschaften in der Sammlung sind alphabetisch nach Namen sortiert.

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

// Zeigen Sie den Wert einer benutzerdefinierten Eigenschaft mithilfe eines DOCPROPERTY-Felds an.
DocumentBuilder builder = new DocumentBuilder(doc);
FieldDocProperty field = (FieldDocProperty)builder.InsertField(" DOCPROPERTY \"Authorized By\"");
field.Update();

Assert.AreEqual("John Doe", field.Result);

// Diese benutzerdefinierten Eigenschaften finden wir in Microsoft Word über „Datei“ -> „Eigenschaften“ > „Erweiterte Eigenschaften“ > „Benutzerdefiniert“.
doc.Save(ArtifactsDir + "DocumentProperties.DocumentPropertyCollection.docx");

// Unten sind drei Möglichkeiten zum Entfernen benutzerdefinierter Eigenschaften aus einem Dokument aufgeführt.
// 1 - Entfernen nach Index:
properties.RemoveAt(1);

Assert.False(properties.Contains("Authorized Amount"));
Assert.AreEqual(4, properties.Count);

// 2 - Nach Namen entfernen:
properties.Remove("Authorized Revision");

Assert.False(properties.Contains("Authorized Revision"));
Assert.AreEqual(3, properties.Count);

// 3 - Die gesamte Sammlung auf einmal leeren:
properties.Clear();

Assert.AreEqual(0, properties.Count);
```

### Siehe auch

* class [BuiltInDocumentProperties](../builtindocumentproperties/)
* class [CustomDocumentProperties](../customdocumentproperties/)
* class [DocumentProperty](../documentproperty/)
* namensraum [Aspose.Words.Properties](../../aspose.words.properties/)
* Montage [Aspose.Words](../../)
