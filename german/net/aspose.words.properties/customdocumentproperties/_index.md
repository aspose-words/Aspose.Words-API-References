---
title: CustomDocumentProperties Class
linktitle: CustomDocumentProperties
articleTitle: CustomDocumentProperties
second_title: Aspose.Words für .NET
description: Aspose.Words.Properties.CustomDocumentProperties klas. Eine Sammlung benutzerdefinierter Dokumenteigenschaften in C#.
type: docs
weight: 4460
url: /de/net/aspose.words.properties/customdocumentproperties/
---
## CustomDocumentProperties class

Eine Sammlung benutzerdefinierter Dokumenteigenschaften.

Um mehr zu erfahren, besuchen Sie die[Arbeiten Sie mit Dokumenteigenschaften](https://docs.aspose.com/words/net/work-with-document-properties/) Dokumentationsartikel.

```csharp
public class CustomDocumentProperties : DocumentPropertyCollection
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
| [Add](../../aspose.words.properties/customdocumentproperties/add/#add)(*string, bool*) | Erstellt eine neue benutzerdefinierte Dokumenteigenschaft desBoolean Datentyp. |
| [Add](../../aspose.words.properties/customdocumentproperties/add/#add_3)(*string, DateTime*) | Erstellt eine neue benutzerdefinierte Dokumenteigenschaft desDateTime Datentyp. |
| [Add](../../aspose.words.properties/customdocumentproperties/add/#add_1)(*string, double*) | Erstellt eine neue benutzerdefinierte Dokumenteigenschaft desDouble Datentyp. |
| [Add](../../aspose.words.properties/customdocumentproperties/add/#add_2)(*string, int*) | Erstellt eine neue benutzerdefinierte Dokumenteigenschaft desNumber Datentyp. |
| [Add](../../aspose.words.properties/customdocumentproperties/add/#add_4)(*string, string*) | Erstellt eine neue benutzerdefinierte Dokumenteigenschaft desString Datentyp. |
| [AddLinkToContent](../../aspose.words.properties/customdocumentproperties/addlinktocontent/)(*string, string*) | Erstellt eine neue mit dem Inhalt verknüpfte benutzerdefinierte Dokumenteigenschaft. |
| [Clear](../../aspose.words.properties/documentpropertycollection/clear/)() | Entfernt alle Eigenschaften aus der Sammlung. |
| [Contains](../../aspose.words.properties/documentpropertycollection/contains/)(*string*) | Gibt zurück`WAHR` wenn eine Eigenschaft mit dem angegebenen Namen in der Sammlung vorhanden ist. |
| [GetEnumerator](../../aspose.words.properties/documentpropertycollection/getenumerator/)() | Gibt ein Enumeratorobjekt zurück, das zum Durchlaufen aller Elemente in der Sammlung verwendet werden kann. |
| [IndexOf](../../aspose.words.properties/documentpropertycollection/indexof/)(*string*) | Ruft den Index einer Eigenschaft nach Namen ab. |
| [Remove](../../aspose.words.properties/documentpropertycollection/remove/)(*string*) | Entfernt eine Eigenschaft mit dem angegebenen Namen aus der Sammlung. |
| [RemoveAt](../../aspose.words.properties/documentpropertycollection/removeat/)(*int*) | Entfernt eine Eigenschaft am angegebenen Index. |

## Bemerkungen

Jede[`DocumentProperty`](../documentproperty/) Das Objekt stellt eine benutzerdefinierte Eigenschaft eines Containerdokuments dar.

Bei den Namen der Eigenschaften wird die Groß-/Kleinschreibung nicht beachtet.

Die Eigenschaften in der Sammlung werden alphabetisch nach Namen sortiert.

## Beispiele

Zeigt, wie mit benutzerdefinierten Dokumenteigenschaften gearbeitet wird.

```csharp
Document doc = new Document(MyDir + "Properties.docx");

// Jedes Dokument enthält eine Sammlung benutzerdefinierter Eigenschaften, die wie die integrierten Eigenschaften Schlüssel-Wert-Paare sind.
 // Das Dokument verfügt über eine feste Liste integrierter Eigenschaften. Der Benutzer erstellt alle benutzerdefinierten Eigenschaften.
Assert.AreEqual("Value of custom document property", doc.CustomDocumentProperties["CustomProperty"].ToString());

doc.CustomDocumentProperties.Add("CustomProperty2", "Value of custom document property #2");

Console.WriteLine("Custom Properties:");
foreach (var customDocumentProperty in doc.CustomDocumentProperties)
{
    Console.WriteLine(customDocumentProperty.Name);
    Console.WriteLine($"\tType:\t{customDocumentProperty.Type}");
    Console.WriteLine($"\tValue:\t\"{customDocumentProperty.Value}\"");
}
```

### Siehe auch

* class [Document](../../aspose.words/document/)
* property [BuiltInDocumentProperties](../../aspose.words/document/builtindocumentproperties/)
* property [CustomDocumentProperties](../../aspose.words/document/customdocumentproperties/)
* class [DocumentPropertyCollection](../documentpropertycollection/)
* namensraum [Aspose.Words.Properties](../../aspose.words.properties/)
* Montage [Aspose.Words](../../)
