---
title: BuiltInDocumentProperties.Item
second_title: Aspose.Words für .NET-API-Referenz
description: BuiltInDocumentProperties eigendom. Gibt a zurückDocumentProperty Objekt mit dem Namen der Eigenschaft.
type: docs
weight: 130
url: /de/net/aspose.words.properties/builtindocumentproperties/item/
---
## BuiltInDocumentProperties indexer

Gibt a zurück[`DocumentProperty`](../../documentproperty/) Objekt mit dem Namen der Eigenschaft.

```csharp
public override DocumentProperty this[string name] { get; }
```

| Parameter | Beschreibung |
| --- | --- |
| name | Der Name der abzurufenden Eigenschaft ohne Berücksichtigung der Groß-/Kleinschreibung. |

### Bemerkungen

Die Zeichenfolgennamen der Eigenschaften entsprechen den Namen der typed -Eigenschaften, die unter verfügbar sind[`BuiltInDocumentProperties`](../).

Wenn Sie eine Eigenschaft anfordern, die nicht im Dokument vorhanden ist, der Name der Eigenschaft jedoch als gültiger integrierter Name erkannt wird, wird ein neuer[`DocumentProperty`](../../documentproperty/) wird erstellt, der Sammlung hinzugefügt und zurückgegeben. Der neu erstellten Eigenschaft wird ein Standardwert zugewiesen (leerer String, Null,`FALSCH` oder DateTime.MinValue, abhängig vom Typ der integrierten Eigenschaft).

Wenn Sie eine Eigenschaft anfordern, die im Dokument nicht vorhanden ist und der Name nicht als integrierter Name erkannt wird, a`Null` ist zurück gekommen.

### Beispiele

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
* namensraum [Aspose.Words.Properties](../../builtindocumentproperties/)
* Montage [Aspose.Words](../../../)


