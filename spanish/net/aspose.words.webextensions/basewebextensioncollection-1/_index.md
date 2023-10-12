---
title: Class BaseWebExtensionCollectionT
second_title: Referencia de API de Aspose.Words para .NET
description: Aspose.Words.WebExtensions.BaseWebExtensionCollection1T clase. Clase base paraTaskPaneCollection WebExtensionBindingCollection  WebExtensionPropertyCollection yWebExtensionReferenceCollection colecciones.
type: docs
weight: 6700
url: /es/net/aspose.words.webextensions/basewebextensioncollection-1/
---
## BaseWebExtensionCollection&lt;T&gt; class

Clase base para[`TaskPaneCollection`](../taskpanecollection/) ,[`WebExtensionBindingCollection`](../webextensionbindingcollection/) , [`WebExtensionPropertyCollection`](../webextensionpropertycollection/) y[`WebExtensionReferenceCollection`](../webextensionreferencecollection/) colecciones.

Para obtener más información, visite el[Trabajar con complementos de Office](https://docs.aspose.com/words/net/work-with-office-add-ins/) artículo de documentación.

```csharp
public abstract class BaseWebExtensionCollection<T> : IEnumerable<T>
    where T : class
```

| Parámetro | Descripción |
| --- | --- |
| T | Tipo de artículo de colección. |

## Propiedades

| Nombre | Descripción |
| --- | --- |
| [Count](../../aspose.words.webextensions/basewebextensioncollection-1/count/) { get; } | Obtiene el número de elementos contenidos en la colección. |
| [Item](../../aspose.words.webextensions/basewebextensioncollection-1/item/) { get; set; } | Obtiene o establece un elemento en el índice especificado. |

## Métodos

| Nombre | Descripción |
| --- | --- |
| [Add](../../aspose.words.webextensions/basewebextensioncollection-1/add/)(T) | Agrega el elemento especificado a la colección. |
| [Clear](../../aspose.words.webextensions/basewebextensioncollection-1/clear/)() | Elimina todos los elementos de la colección. |
| [GetEnumerator](../../aspose.words.webextensions/basewebextensioncollection-1/getenumerator/)() | Devuelve un enumerador que puede iterar a través de una colección. |
| [Remove](../../aspose.words.webextensions/basewebextensioncollection-1/remove/)(int) | Elimina el elemento en el índice especificado de la colección. |

### Ejemplos

Muestra cómo trabajar con la colección de extensiones web de un documento.

```csharp
Document doc = new Document(MyDir + "Web extension.docx");

Assert.AreEqual(1, doc.WebExtensionTaskPanes.Count);

// Imprime todas las propiedades de la extensión web del documento.
WebExtensionPropertyCollection webExtensionPropertyCollection = doc.WebExtensionTaskPanes[0].WebExtension.Properties;
using (IEnumerator<WebExtensionProperty> enumerator = webExtensionPropertyCollection.GetEnumerator())
{
    while (enumerator.MoveNext())
    {
        WebExtensionProperty webExtensionProperty = enumerator.Current;
        Console.WriteLine($"Binding name: {webExtensionProperty.Name}; Binding value: {webExtensionProperty.Value}");
    }
}

// Elimina la extensión web.
doc.WebExtensionTaskPanes.Remove(0);

Assert.AreEqual(0, doc.WebExtensionTaskPanes.Count);
```

### Ver también

* espacio de nombres [Aspose.Words.WebExtensions](../../aspose.words.webextensions/)
* asamblea [Aspose.Words](../../)


