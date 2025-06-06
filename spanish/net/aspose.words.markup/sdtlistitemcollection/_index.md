---
title: SdtListItemCollection Class
linktitle: SdtListItemCollection
articleTitle: SdtListItemCollection
second_title: Aspose.Words para .NET
description: Explore la clase Aspose.Words.Markup.SdtListItemCollection para obtener acceso perfecto a los elementos SdtListItem, mejorando la gestión de documentos estructurados sin esfuerzo.
type: docs
weight: 4720
url: /es/net/aspose.words.markup/sdtlistitemcollection/
---
## SdtListItemCollection class

Proporciona acceso a[`SdtListItem`](../sdtlistitem/) elementos de una etiqueta de documento estructurado.

Para obtener más información, visite el[Etiquetas de documentos estructurados o control de contenido](https://docs.aspose.com/words/net/working-with-content-control-sdt/) Artículo de documentación.

```csharp
public class SdtListItemCollection : IEnumerable<SdtListItem>
```

## Propiedades

| Nombre | Descripción |
| --- | --- |
| [Count](../../aspose.words.markup/sdtlistitemcollection/count/) { get; } | Obtiene el número de elementos en la colección. |
| [Item](../../aspose.words.markup/sdtlistitemcollection/item/) { get; } | Devuelve un[`SdtListItem`](../sdtlistitem/) objeto dado su índice basado en cero en la colección. |
| [SelectedValue](../../aspose.words.markup/sdtlistitemcollection/selectedvalue/) { get; set; } | Especifica el valor seleccionado actualmente en esta lista. Se permite un valor nulo, lo que significa que ninguna entrada seleccionada actualmente está asociada con esta colección de elementos de la lista. |

## Métodos

| Nombre | Descripción |
| --- | --- |
| [Add](../../aspose.words.markup/sdtlistitemcollection/add/)(*[SdtListItem](../sdtlistitem/)*) | Agrega un elemento a esta colección. |
| [Clear](../../aspose.words.markup/sdtlistitemcollection/clear/)() | Borra todos los elementos de esta colección. |
| [GetEnumerator](../../aspose.words.markup/sdtlistitemcollection/getenumerator/)() | Devuelve un objeto enumerador que se puede utilizar para iterar sobre todos los elementos de la colección. |
| [RemoveAt](../../aspose.words.markup/sdtlistitemcollection/removeat/)(*int*) | Elimina un elemento de la lista en el índice especificado. |

## Ejemplos

Muestra cómo trabajar con etiquetas de documentos estructurados con listas desplegables.

```csharp
Document doc = new Document();
StructuredDocumentTag tag = new StructuredDocumentTag(doc, SdtType.DropDownList, MarkupLevel.Block);
doc.FirstSection.Body.AppendChild(tag);

// Una etiqueta de documento estructurado de lista desplegable es un formulario que permite al usuario
// seleccione una opción de una lista haciendo clic izquierdo y abriendo el formulario en Microsoft Word.
// La propiedad "ListItems" contiene todos los elementos de la lista, y cada elemento de la lista es un "SdtListItem".
SdtListItemCollection listItems = tag.ListItems;
listItems.Add(new SdtListItem("Value 1"));

Assert.AreEqual(listItems[0].DisplayText, listItems[0].Value);

// Agregue 3 elementos más a la lista. Inicialice estos elementos con un constructor diferente al del primer elemento.
// para mostrar cadenas que son diferentes de sus valores.
listItems.Add(new SdtListItem("Item 2", "Value 2"));
listItems.Add(new SdtListItem("Item 3", "Value 3"));
listItems.Add(new SdtListItem("Item 4", "Value 4"));

Assert.AreEqual(4, listItems.Count);

La lista desplegable muestra el primer elemento. Asigne un elemento diferente a "SelectedValue" para mostrarlo.
listItems.SelectedValue = listItems[3];

Assert.AreEqual("Value 4", listItems.SelectedValue.Value);

// Enumera la colección e imprime cada elemento.
using (IEnumerator<SdtListItem> enumerator = listItems.GetEnumerator())
{
    while (enumerator.MoveNext())
        if (enumerator.Current != null)
            Console.WriteLine($"List item: {enumerator.Current.DisplayText}, value: {enumerator.Current.Value}");
}

 //Eliminar el último elemento de la lista.
listItems.RemoveAt(3);

Assert.AreEqual(3, listItems.Count);

// Dado que nuestro control desplegable está configurado para mostrar el elemento eliminado de manera predeterminada, asígnele un elemento para mostrar que exista.
listItems.SelectedValue = listItems[1];

doc.Save(ArtifactsDir + "StructuredDocumentTag.ListItemCollection.docx");

// Utilice el método "Borrar" para vaciar toda la colección de elementos desplegables de una vez.
listItems.Clear();

Assert.AreEqual(0, listItems.Count);
```

### Ver también

* class [SdtListItem](../sdtlistitem/)
* espacio de nombres [Aspose.Words.Markup](../../aspose.words.markup/)
* asamblea [Aspose.Words](../../)
