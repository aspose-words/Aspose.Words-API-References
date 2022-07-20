---
title: SdtListItem
second_title: Referencia de API de Aspose.Words para .NET
description: Inicializa una nueva instancia de esta clase.
type: docs
weight: 10
url: /es/net/aspose.words.markup/sdtlistitem/sdtlistitem/
---
## SdtListItem(string, string) {#constructor_1}

Inicializa una nueva instancia de esta clase.

```csharp
public SdtListItem(string displayText, string value)
```

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

* class [SdtListItem](../../sdtlistitem)
* espacio de nombres [Aspose.Words.Markup](../../sdtlistitem)
* asamblea [Aspose.Words](../../../)

---

## SdtListItem(string) {#constructor}

Inicializa una nueva instancia de esta clase.

```csharp
public SdtListItem(string value)
```

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

* class [SdtListItem](../../sdtlistitem)
* espacio de nombres [Aspose.Words.Markup](../../sdtlistitem)
* asamblea [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->