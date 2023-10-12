---
title: Class BaseWebExtensionCollectionT
second_title: Aspose.Words für .NET-API-Referenz
description: Aspose.Words.WebExtensions.BaseWebExtensionCollection1T klas. Basisklasse fürTaskPaneCollection WebExtensionBindingCollection  WebExtensionPropertyCollection UndWebExtensionReferenceCollection Sammlungen.
type: docs
weight: 6700
url: /de/net/aspose.words.webextensions/basewebextensioncollection-1/
---
## BaseWebExtensionCollection&lt;T&gt; class

Basisklasse für[`TaskPaneCollection`](../taskpanecollection/) ,[`WebExtensionBindingCollection`](../webextensionbindingcollection/) , [`WebExtensionPropertyCollection`](../webextensionpropertycollection/) Und[`WebExtensionReferenceCollection`](../webextensionreferencecollection/) Sammlungen.

Um mehr zu erfahren, besuchen Sie die[Arbeiten Sie mit Office-Add-Ins](https://docs.aspose.com/words/net/work-with-office-add-ins/) Dokumentationsartikel.

```csharp
public abstract class BaseWebExtensionCollection<T> : IEnumerable<T>
    where T : class
```

| Parameter | Beschreibung |
| --- | --- |
| T | Typ eines Sammlungselements. |

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| [Count](../../aspose.words.webextensions/basewebextensioncollection-1/count/) { get; } | Ruft die Anzahl der in der Sammlung enthaltenen Elemente ab. |
| [Item](../../aspose.words.webextensions/basewebextensioncollection-1/item/) { get; set; } | Ruft ein Element am angegebenen Index ab oder legt es fest. |

## Methoden

| Name | Beschreibung |
| --- | --- |
| [Add](../../aspose.words.webextensions/basewebextensioncollection-1/add/)(T) | Fügt das angegebene Element zur Sammlung hinzu. |
| [Clear](../../aspose.words.webextensions/basewebextensioncollection-1/clear/)() | Entfernt alle Elemente aus der Sammlung. |
| [GetEnumerator](../../aspose.words.webextensions/basewebextensioncollection-1/getenumerator/)() | Gibt einen Enumerator zurück, der eine Sammlung durchlaufen kann. |
| [Remove](../../aspose.words.webextensions/basewebextensioncollection-1/remove/)(int) | Entfernt das Element am angegebenen Index aus der Sammlung. |

### Beispiele

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

* namensraum [Aspose.Words.WebExtensions](../../aspose.words.webextensions/)
* Montage [Aspose.Words](../../)


