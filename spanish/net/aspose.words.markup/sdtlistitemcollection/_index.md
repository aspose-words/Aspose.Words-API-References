---
title: Class SdtListItemCollection
second_title: Referencia de API de Aspose.Words para .NET
description: Aspose.Words.Markup.SdtListItemCollection clase. Proporciona acceso aSdtListItemelementos de un documento estructurado tag.
type: docs
weight: 3790
url: /es/net/aspose.words.markup/sdtlistitemcollection/
---
## SdtListItemCollection class

Proporciona acceso a[`SdtListItem`](../sdtlistitem/)elementos de un documento estructurado tag.

```csharp
public class SdtListItemCollection : IEnumerable<SdtListItem>
```

## Propiedades

| Nombre | Descripción |
| --- | --- |
| [Count](../../aspose.words.markup/sdtlistitemcollection/count/) { get; } | Obtiene el número de elementos de la colección. |
| [Item](../../aspose.words.markup/sdtlistitemcollection/item/) { get; } | Devuelve un[`SdtListItem`](../sdtlistitem/) objeto dado su índice basado en cero en la colección. |
| [SelectedValue](../../aspose.words.markup/sdtlistitemcollection/selectedvalue/) { get; set; } | Especifica el valor seleccionado actualmente en esta lista. Valor nulo permitido, lo que significa que ninguna entrada seleccionada actualmente está asociada con esta colección de elementos de lista. |

## Métodos

| Nombre | Descripción |
| --- | --- |
| [Add](../../aspose.words.markup/sdtlistitemcollection/add/)(SdtListItem) | Agrega un artículo a esta colección. |
| [Clear](../../aspose.words.markup/sdtlistitemcollection/clear/)() | Borra todos los elementos de esta colección. |
| [GetEnumerator](../../aspose.words.markup/sdtlistitemcollection/getenumerator/)() | Devuelve un objeto enumerador que se puede usar para iterar sobre todos los elementos de la colección. |
| [RemoveAt](../../aspose.words.markup/sdtlistitemcollection/removeat/)(int) | Elimina un elemento de la lista en el índice especificado. |

### Ejemplos

Muestra cómo trabajar con etiquetas de documentos estructurados de lista desplegable.

```csharp
Document doc = new Document();
StructuredDocumentTag tag = new StructuredDocumentTag(doc, SdtType.DropDownList, MarkupLevel.Block);
doc.FirstSection.Body.AppendChild(tag);

// Una etiqueta de documento estructurado de lista desplegable es un formulario que permite al usuario
// seleccione una opción de una lista haciendo clic izquierdo y abriendo el formulario en Microsoft Word.
// La propiedad "ListItems" contiene todos los elementos de la lista y cada elemento de la lista es un "SdtListItem".
SdtListItemCollection listItems = tag.ListItems;
listItems.Add(new SdtListItem("Value 1"));

Assert.AreEqual(listItems[0].DisplayText, listItems[0].Value);

// Agregue 3 elementos de lista más. Inicialice estos elementos usando un constructor diferente al primer elemento
// para mostrar cadenas que son diferentes de sus valores.
listItems.Add(new SdtListItem("Item 2", "Value 2"));
listItems.Add(new SdtListItem("Item 3", "Value 3"));
listItems.Add(new SdtListItem("Item 4", "Value 4"));

Assert.AreEqual(4, listItems.Count);

// La lista desplegable muestra el primer elemento. Asigne un elemento de lista diferente al "Valor seleccionado" para mostrarlo.
listItems.SelectedValue = listItems[3];

Assert.AreEqual("Value 4", listItems.SelectedValue.Value);

// Enumerar sobre la colección e imprimir cada elemento.
using (IEnumerator<SdtListItem> enumerator = listItems.GetEnumerator())
{
    while (enumerator.MoveNext())
        if (enumerator.Current != null)
            Console.WriteLine($"List item: {enumerator.Current.DisplayText}, value: {enumerator.Current.Value}");
}

  // Elimina el último elemento de la lista.
listItems.RemoveAt(3);

Assert.AreEqual(3, listItems.Count);

// Dado que nuestro control desplegable está configurado para mostrar el elemento eliminado de forma predeterminada, asígnele un elemento para mostrar que existe.
listItems.SelectedValue = listItems[1];

doc.Save(ArtifactsDir + "StructuredDocumentTag.ListItemCollection.docx");

// Use el método "Borrar" para vaciar toda la colección de elementos desplegables a la vez.
listItems.Clear();

Assert.AreEqual(0, listItems.Count);
```

### Ver también

* class [SdtListItem](../sdtlistitem/)
* espacio de nombres [Aspose.Words.Markup](../../aspose.words.markup/)
* asamblea [Aspose.Words](../../)


