---
title: BuiltInDocumentProperties.Item
linktitle: Item
articleTitle: Item
second_title: Aspose.Words für .NET
description: Greifen Sie mühelos auf DocumentProperty-Objekte zu – mit der Item-Eigenschaft „BuiltInDocumentProperties“. Optimieren Sie noch heute Ihr Dokumentenmanagement!
type: docs
weight: 140
url: /de/net/aspose.words.properties/builtindocumentproperties/item/
---
## BuiltInDocumentProperties indexer

Gibt einen[`DocumentProperty`](../../documentproperty/) Objekt durch den Namen der Eigenschaft.

```csharp
public override DocumentProperty this[string name] { get; }
```

| Parameter | Beschreibung |
| --- | --- |
| name | Der Name der abzurufenden Eigenschaft (ohne Berücksichtigung der Groß-/Kleinschreibung). |

## Bemerkungen

Die Stringnamen der Eigenschaften entsprechen den Namen der typed -Eigenschaften, die verfügbar sind unter[`BuiltInDocumentProperties`](../).

Wenn Sie eine Eigenschaft anfordern, die im Dokument nicht vorhanden ist, der Name der Eigenschaft jedoch als gültiger integrierter Name erkannt wird, wird ein neuer[`DocumentProperty`](../../documentproperty/) wird erstellt, der Sammlung hinzugefügt und zurückgegeben. Der neu erstellten Eigenschaft wird ein Standardwert zugewiesen (leerer String, Null,`FALSCH` oder DateTime.MinValue, abhängig vom Typ der integrierten Eigenschaft).

Wenn Sie eine Eigenschaft anfordern, die im Dokument nicht vorhanden ist und der Name nicht als integrierter Name erkannt wird, wird ein`null` wird zurückgegeben.

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
* class [BuiltInDocumentProperties](../)
* namensraum [Aspose.Words.Properties](../../../aspose.words.properties/)
* Montage [Aspose.Words](../../../)
