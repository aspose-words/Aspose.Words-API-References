---
title: BaseWebExtensionCollection1.Remove
linktitle: Remove
articleTitle: Remove
second_title: Aspose.Words für .NET
description: BaseWebExtensionCollection Remove methode. Entfernt das Element am angegebenen Index aus der Sammlung in C#.
type: docs
weight: 60
url: /de/net/aspose.words.webextensions/basewebextensioncollection-1/remove/
---
## BaseWebExtensionCollection&lt;T&gt;.Remove method

Entfernt das Element am angegebenen Index aus der Sammlung.

```csharp
public void Remove(int index)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| index | Int32 | Der nullbasierte Index des Sammlungselements. |

## Beispiele

Zeigt, wie mit der Sammlung von Weberweiterungen eines Dokuments gearbeitet wird.

```csharp
Document doc = new Document(MyDir + "Web extension.docx");

Assert.AreEqual(1, doc.WebExtensionTaskPanes.Count);

// Alle Eigenschaften der Weberweiterung des Dokuments drucken.
WebExtensionPropertyCollection webExtensionPropertyCollection = doc.WebExtensionTaskPanes[0].WebExtension.Properties;
using (IEnumerator<WebExtensionProperty> enumerator = webExtensionPropertyCollection.GetEnumerator())
{
    while (enumerator.MoveNext())
    {
        WebExtensionProperty webExtensionProperty = enumerator.Current;
        Console.WriteLine($"Binding name: {webExtensionProperty.Name}; Binding value: {webExtensionProperty.Value}");
    }
}

// Web-Erweiterung entfernen.
doc.WebExtensionTaskPanes.Remove(0);

Assert.AreEqual(0, doc.WebExtensionTaskPanes.Count);
```

### Siehe auch

* class [BaseWebExtensionCollection&lt;T&gt;](../)
* namensraum [Aspose.Words.WebExtensions](../../../aspose.words.webextensions/)
* Montage [Aspose.Words](../../../)
