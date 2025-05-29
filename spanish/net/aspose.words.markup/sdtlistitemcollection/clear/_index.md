---
title: SdtListItemCollection.Clear
linktitle: Clear
articleTitle: Clear
second_title: Aspose.Words para .NET
description: Borre fácilmente todos los elementos de su SdtListItemCollection con el método Clear. Optimice la gestión de datos para un rendimiento óptimo.
type: docs
weight: 50
url: /es/net/aspose.words.markup/sdtlistitemcollection/clear/
---
## SdtListItemCollection.Clear method

Borra todos los elementos de esta colección.

```csharp
public void Clear()
```

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

* class [SdtListItemCollection](../)
* espacio de nombres [Aspose.Words.Markup](../../../aspose.words.markup/)
* asamblea [Aspose.Words](../../../)
