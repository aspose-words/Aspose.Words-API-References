---
title: DocumentPropertyCollection.Item
linktitle: Item
articleTitle: Item
second_title: Aspose.Words für .NET
description: Greifen Sie mit unserem DocumentPropertyCollection-Element mühelos auf DocumentProperty-Objekte zu. Rufen Sie Eigenschaften nach Namen ab, um ein nahtloses Dokumentenmanagement zu ermöglichen.
type: docs
weight: 20
url: /de/net/aspose.words.properties/documentpropertycollection/item/
---
## DocumentPropertyCollection indexer (1 of 2)

Gibt einen[`DocumentProperty`](../../documentproperty/) Objekt durch den Namen der Eigenschaft.

```csharp
public virtual DocumentProperty this[string name] { get; }
```

| Parameter | Beschreibung |
| --- | --- |
| name | Der Name der abzurufenden Eigenschaft (ohne Berücksichtigung der Groß-/Kleinschreibung). |

## Bemerkungen

Rückgaben`null` wenn eine Eigenschaft mit dem angegebenen Namen nicht gefunden wird.

## Beispiele

Zeigt, wie eine benutzerdefinierte Dokumenteigenschaft erstellt wird, die ein Datum und eine Uhrzeit enthält.

```csharp
Document doc = new Document();

doc.CustomDocumentProperties.Add("AuthorizationDate", DateTime.Now);
DateTime authorizationDate = doc.CustomDocumentProperties["AuthorizationDate"].ToDateTime();
Console.WriteLine($"Document authorized on {authorizationDate}");
```

### Siehe auch

* class [DocumentProperty](../../documentproperty/)
* class [DocumentPropertyCollection](../)
* namensraum [Aspose.Words.Properties](../../../aspose.words.properties/)
* Montage [Aspose.Words](../../../)

---

## DocumentPropertyCollection indexer (2 of 2)

Gibt einen[`DocumentProperty`](../../documentproperty/) Objekt nach Index.

```csharp
public DocumentProperty this[int index] { get; }
```

| Parameter | Beschreibung |
| --- | --- |
| index | Nullbasierter Index des[`DocumentProperty`](../../documentproperty/) abzurufen. |

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

* class [DocumentProperty](../../documentproperty/)
* class [DocumentPropertyCollection](../)
* namensraum [Aspose.Words.Properties](../../../aspose.words.properties/)
* Montage [Aspose.Words](../../../)
