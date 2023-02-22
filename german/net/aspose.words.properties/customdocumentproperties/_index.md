---
title: Class CustomDocumentProperties
second_title: Aspose.Words für .NET-API-Referenz
description: Aspose.Words.Properties.CustomDocumentProperties klas. Eine Sammlung benutzerdefinierter Dokumenteigenschaften.
type: docs
weight: 4210
url: /de/net/aspose.words.properties/customdocumentproperties/
---
## CustomDocumentProperties class

Eine Sammlung benutzerdefinierter Dokumenteigenschaften.

```csharp
public class CustomDocumentProperties : DocumentPropertyCollection
```

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| [Count](../../aspose.words.properties/documentpropertycollection/count/) { get; } | Ruft die Anzahl der Elemente in der Sammlung ab. |
| [Item](../../aspose.words.properties/documentpropertycollection/item/) { get; } | Gibt a zurück[`DocumentProperty`](../documentproperty/) Objekt nach Index. |
| virtual [Item](../../aspose.words.properties/documentpropertycollection/item/) { get; } | Gibt a zurück[`DocumentProperty`](../documentproperty/) Objekt nach dem Namen der Eigenschaft. |

## Methoden

| Name | Beschreibung |
| --- | --- |
| [Add](../../aspose.words.properties/customdocumentproperties/add/#add)(string, bool) | Erstellt eine neue benutzerdefinierte Dokumenteigenschaft des **PropertyType.Boolean** Datentyp. |
| [Add](../../aspose.words.properties/customdocumentproperties/add/#add_3)(string, DateTime) | Erstellt eine neue benutzerdefinierte Dokumenteigenschaft des **PropertyType.DateTime** Datentyp. |
| [Add](../../aspose.words.properties/customdocumentproperties/add/#add_1)(string, double) | Erstellt eine neue benutzerdefinierte Dokumenteigenschaft des **PropertyType.Float** Datentyp. |
| [Add](../../aspose.words.properties/customdocumentproperties/add/#add_2)(string, int) | Erstellt eine neue benutzerdefinierte Dokumenteigenschaft des **PropertyType.Number** Datentyp. |
| [Add](../../aspose.words.properties/customdocumentproperties/add/#add_4)(string, string) | Erstellt eine neue benutzerdefinierte Dokumenteigenschaft des **PropertyType.String** Datentyp. |
| [AddLinkToContent](../../aspose.words.properties/customdocumentproperties/addlinktocontent/)(string, string) | Erstellt eine neue, mit Inhalt verknüpfte benutzerdefinierte Dokumenteigenschaft. |
| [Clear](../../aspose.words.properties/documentpropertycollection/clear/)() | Entfernt alle Eigenschaften aus der Sammlung. |
| [Contains](../../aspose.words.properties/documentpropertycollection/contains/)(string) | Gibt „true“ zurück, wenn eine Eigenschaft mit dem angegebenen Namen in der Sammlung vorhanden ist. |
| [GetEnumerator](../../aspose.words.properties/documentpropertycollection/getenumerator/)() | Gibt ein Aufzählungsobjekt zurück, das verwendet werden kann, um alle Elemente in der Sammlung zu durchlaufen. |
| [IndexOf](../../aspose.words.properties/documentpropertycollection/indexof/)(string) | Ruft den Index einer Eigenschaft nach Namen ab. |
| [Remove](../../aspose.words.properties/documentpropertycollection/remove/)(string) | Entfernt eine Eigenschaft mit dem angegebenen Namen aus der Sammlung. |
| [RemoveAt](../../aspose.words.properties/documentpropertycollection/removeat/)(int) | Entfernt eine Eigenschaft am angegebenen Index. |

### Bemerkungen

Jeder[`DocumentProperty`](../documentproperty/) Objekt stellt eine benutzerdefinierte Eigenschaft eines Containerdokuments dar.

Bei den Namen der Eigenschaften wird die Groß-/Kleinschreibung nicht beachtet.

Die Eigenschaften in der Sammlung sind alphabetisch nach Namen sortiert.

### Beispiele

Zeigt, wie Sie mit benutzerdefinierten Dokumenteigenschaften arbeiten.

```csharp
Document doc = new Document(MyDir + "Properties.docx");

// Jedes Dokument enthält eine Sammlung benutzerdefinierter Eigenschaften, die wie die integrierten Eigenschaften Schlüssel-Wert-Paare sind.
// Das Dokument hat eine feste Liste eingebauter Eigenschaften. Der Benutzer erstellt alle benutzerdefinierten Eigenschaften. 
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


