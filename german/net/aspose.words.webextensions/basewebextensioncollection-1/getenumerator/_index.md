---
title: BaseWebExtensionCollection1.GetEnumerator
linktitle: GetEnumerator
articleTitle: GetEnumerator
second_title: Aspose.Words für .NET
description: Entdecken Sie die GetEnumerator-Methode von BaseWebExtensionCollection, um einfach durch Sammlungen zu iterieren und so Ihre Entwicklungseffizienz und Codeverwaltung zu verbessern.
type: docs
weight: 50
url: /de/net/aspose.words.webextensions/basewebextensioncollection-1/getenumerator/
---
## BaseWebExtensionCollection&lt;T&gt;.GetEnumerator method

Gibt einen Enumerator zurück, der eine Sammlung durchlaufen kann.

```csharp
public IEnumerator<T> GetEnumerator()
```

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

// Entfernen Sie die Weberweiterung.
doc.WebExtensionTaskPanes.Remove(0);

Assert.AreEqual(0, doc.WebExtensionTaskPanes.Count);
```

### Siehe auch

* class [BaseWebExtensionCollection&lt;T&gt;](../)
* namensraum [Aspose.Words.WebExtensions](../../../aspose.words.webextensions/)
* Montage [Aspose.Words](../../../)
