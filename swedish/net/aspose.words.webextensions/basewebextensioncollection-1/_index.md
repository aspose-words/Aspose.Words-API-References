---
title: Class BaseWebExtensionCollectionT
second_title: Aspose.Words för .NET API Referens
description: Aspose.Words.WebExtensions.BaseWebExtensionCollection1T klass. Basklass förTaskPaneCollection WebExtensionBindingCollection  WebExtensionPropertyCollection ochWebExtensionReferenceCollection samlingar.
type: docs
weight: 6700
url: /sv/net/aspose.words.webextensions/basewebextensioncollection-1/
---
## BaseWebExtensionCollection&lt;T&gt; class

Basklass för[`TaskPaneCollection`](../taskpanecollection/) ,[`WebExtensionBindingCollection`](../webextensionbindingcollection/) , [`WebExtensionPropertyCollection`](../webextensionpropertycollection/) och[`WebExtensionReferenceCollection`](../webextensionreferencecollection/) samlingar.

För att lära dig mer, besök[Arbeta med Office-tillägg](https://docs.aspose.com/words/net/work-with-office-add-ins/) dokumentationsartikel.

```csharp
public abstract class BaseWebExtensionCollection<T> : IEnumerable<T>
    where T : class
```

| Parameter | Beskrivning |
| --- | --- |
| T | Typ av samlingsobjekt. |

## Egenskaper

| namn | Beskrivning |
| --- | --- |
| [Count](../../aspose.words.webextensions/basewebextensioncollection-1/count/) { get; } | Hämtar antalet element som finns i samlingen. |
| [Item](../../aspose.words.webextensions/basewebextensioncollection-1/item/) { get; set; } | Hämtar eller ställer in ett objekt på angivet index. |

## Metoder

| namn | Beskrivning |
| --- | --- |
| [Add](../../aspose.words.webextensions/basewebextensioncollection-1/add/)(T) | Lägger till angivet objekt till samlingen. |
| [Clear](../../aspose.words.webextensions/basewebextensioncollection-1/clear/)() | Tar bort alla element från samlingen. |
| [GetEnumerator](../../aspose.words.webextensions/basewebextensioncollection-1/getenumerator/)() | Returnerar en uppräkning som kan iterera genom en samling. |
| [Remove](../../aspose.words.webextensions/basewebextensioncollection-1/remove/)(int) | Tar bort objektet vid det angivna indexet från samlingen. |

### Exempel

Visar hur man arbetar med ett dokuments samling av webbtillägg.

```csharp
Document doc = new Document(MyDir + "Web extension.docx");

Assert.AreEqual(1, doc.WebExtensionTaskPanes.Count);

// Skriv ut alla egenskaper för dokumentets webbtillägg.
WebExtensionPropertyCollection webExtensionPropertyCollection = doc.WebExtensionTaskPanes[0].WebExtension.Properties;
using (IEnumerator<WebExtensionProperty> enumerator = webExtensionPropertyCollection.GetEnumerator())
{
    while (enumerator.MoveNext())
    {
        WebExtensionProperty webExtensionProperty = enumerator.Current;
        Console.WriteLine($"Binding name: {webExtensionProperty.Name}; Binding value: {webExtensionProperty.Value}");
    }
}

// Ta bort webbtillägget.
doc.WebExtensionTaskPanes.Remove(0);

Assert.AreEqual(0, doc.WebExtensionTaskPanes.Count);
```

### Se även

* namnutrymme [Aspose.Words.WebExtensions](../../aspose.words.webextensions/)
* hopsättning [Aspose.Words](../../)


