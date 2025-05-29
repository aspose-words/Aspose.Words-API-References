---
title: BaseWebExtensionCollection1.Remove
linktitle: Remove
articleTitle: Remove
second_title: Aspose.Words para .NET
description: Elimina elementos de tu BaseWebExtensionCollection fácilmente con nuestro intuitivo método de eliminación. ¡Optimiza la gestión de tus datos hoy mismo!
type: docs
weight: 60
url: /es/net/aspose.words.webextensions/basewebextensioncollection-1/remove/
---
## BaseWebExtensionCollection&lt;T&gt;.Remove method

Elimina el elemento en el índice especificado de la colección.

```csharp
public void Remove(int index)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| index | Int32 | El índice basado en cero del elemento de la colección. |

## Ejemplos

Muestra cómo trabajar con la colección de extensiones web de un documento.

```csharp
Document doc = new Document(MyDir + "Web extension.docx");

Assert.AreEqual(1, doc.WebExtensionTaskPanes.Count);

//Imprimir todas las propiedades de la extensión web del documento.
WebExtensionPropertyCollection webExtensionPropertyCollection = doc.WebExtensionTaskPanes[0].WebExtension.Properties;
using (IEnumerator<WebExtensionProperty> enumerator = webExtensionPropertyCollection.GetEnumerator())
{
    while (enumerator.MoveNext())
    {
        WebExtensionProperty webExtensionProperty = enumerator.Current;
        Console.WriteLine($"Binding name: {webExtensionProperty.Name}; Binding value: {webExtensionProperty.Value}");
    }
}

//Eliminar la extensión web.
doc.WebExtensionTaskPanes.Remove(0);

Assert.AreEqual(0, doc.WebExtensionTaskPanes.Count);
```

### Ver también

* class [BaseWebExtensionCollection&lt;T&gt;](../)
* espacio de nombres [Aspose.Words.WebExtensions](../../../aspose.words.webextensions/)
* asamblea [Aspose.Words](../../../)
