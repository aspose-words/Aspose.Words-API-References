---
title: CustomDocumentProperties Class
linktitle: CustomDocumentProperties
articleTitle: CustomDocumentProperties
second_title: Aspose.Words für .NET
description: Entdecken Sie Aspose.Words.Properties.CustomDocumentProperties für die mühelose Verwaltung benutzerdefinierter Dokumenteigenschaften. Verbessern Sie noch heute Ihr Dokumentenmanagement!
type: docs
weight: 5190
url: /de/net/aspose.words.properties/customdocumentproperties/
---
## CustomDocumentProperties class

Eine Sammlung benutzerdefinierter Dokumenteigenschaften.

Um mehr zu erfahren, besuchen Sie die[Arbeiten mit Dokumenteigenschaften](https://docs.aspose.com/words/net/work-with-document-properties/) Dokumentationsartikel.

```csharp
public class CustomDocumentProperties : DocumentPropertyCollection
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
| [Add](../../aspose.words.properties/customdocumentproperties/add/#add)(*string, bool*) | Erstellt eine neue benutzerdefinierte Dokumenteigenschaft desBoolean Datentyp. |
| [Add](../../aspose.words.properties/customdocumentproperties/add/#add_3)(*string, DateTime*) | Erstellt eine neue benutzerdefinierte Dokumenteigenschaft desDateTime Datentyp. |
| [Add](../../aspose.words.properties/customdocumentproperties/add/#add_1)(*string, double*) | Erstellt eine neue benutzerdefinierte Dokumenteigenschaft desDouble Datentyp. |
| [Add](../../aspose.words.properties/customdocumentproperties/add/#add_2)(*string, int*) | Erstellt eine neue benutzerdefinierte Dokumenteigenschaft desNumber Datentyp. |
| [Add](../../aspose.words.properties/customdocumentproperties/add/#add_4)(*string, string*) | Erstellt eine neue benutzerdefinierte Dokumenteigenschaft desString Datentyp. |
| [AddLinkToContent](../../aspose.words.properties/customdocumentproperties/addlinktocontent/)(*string, string*) | Erstellt eine neue, mit dem Inhalt verknüpfte benutzerdefinierte Dokumenteigenschaft. |
| [Clear](../../aspose.words.properties/documentpropertycollection/clear/)() | Entfernt alle Eigenschaften aus der Sammlung. |
| [Contains](../../aspose.words.properties/documentpropertycollection/contains/)(*string*) | Rückgaben`WAHR` wenn eine Eigenschaft mit dem angegebenen Namen in der Sammlung vorhanden ist. |
| [GetEnumerator](../../aspose.words.properties/documentpropertycollection/getenumerator/)() | Gibt ein Enumeratorobjekt zurück, mit dem alle Elemente in der Sammlung durchlaufen werden können. |
| [IndexOf](../../aspose.words.properties/documentpropertycollection/indexof/)(*string*) | Ruft den Index einer Eigenschaft nach Namen ab. |
| [Remove](../../aspose.words.properties/documentpropertycollection/remove/)(*string*) | Entfernt eine Eigenschaft mit dem angegebenen Namen aus der Sammlung. |
| [RemoveAt](../../aspose.words.properties/documentpropertycollection/removeat/)(*int*) | Entfernt eine Eigenschaft am angegebenen Index. |

## Bemerkungen

Jede[`DocumentProperty`](../documentproperty/) Das Objekt stellt eine benutzerdefinierte Eigenschaft eines Containerdokuments dar.

Bei den Namen der Eigenschaften wird die Groß- und Kleinschreibung nicht berücksichtigt.

Die Eigenschaften in der Sammlung sind alphabetisch nach Namen sortiert.

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
