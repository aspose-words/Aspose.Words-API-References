---
title: SdtListItem Class
linktitle: SdtListItem
articleTitle: SdtListItem
second_title: Aspose.Words para .NET
description: Descubra la clase Aspose.Words.Markup.SdtListItem, diseñada para la gestión eficiente de elementos de lista en documentos estructurados ComboBox y DropDownList.
type: docs
weight: 4710
url: /es/net/aspose.words.markup/sdtlistitem/
---
## SdtListItem class

Este elemento especifica un solo elemento de lista dentro de una lista padreComboBox oDropDownList etiqueta de documento estructurado.

Para obtener más información, visite el[Etiquetas de documentos estructurados o control de contenido](https://docs.aspose.com/words/net/working-with-content-control-sdt/) Artículo de documentación.

```csharp
public class SdtListItem
```

## Constructores

| Nombre | Descripción |
| --- | --- |
| [SdtListItem](sdtlistitem/#constructor)(*string*) | Inicializa una nueva instancia de esta clase. |
| [SdtListItem](sdtlistitem/#constructor_1)(*string, string*) | Inicializa una nueva instancia de esta clase. |

## Propiedades

| Nombre | Descripción |
| --- | --- |
| [DisplayText](../../aspose.words.markup/sdtlistitem/displaytext/) { get; } | Obtiene el texto que se mostrará en el contenido de la ejecución en lugar de[`Value`](./value/) contenido de los atributos para este elemento de la lista. |
| [Value](../../aspose.words.markup/sdtlistitem/value/) { get; } | Obtiene el valor de este elemento de la lista. |

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

* espacio de nombres [Aspose.Words.Markup](../../aspose.words.markup/)
* asamblea [Aspose.Words](../../)
