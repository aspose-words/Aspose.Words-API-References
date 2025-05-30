---
title: DropDownItemCollection Class
linktitle: DropDownItemCollection
articleTitle: DropDownItemCollection
second_title: Aspose.Words para .NET
description: Explore la clase Aspose.Words.Fields.DropDownItemCollection ¡su solución ideal para administrar elementos desplegables en campos de formulario sin esfuerzo!
type: docs
weight: 1910
url: /es/net/aspose.words.fields/dropdownitemcollection/
---
## DropDownItemCollection class

Una colección de cadenas que representan todos los elementos de un campo de formulario desplegable.

Para obtener más información, visite el[Trabajar con campos](https://docs.aspose.com/words/net/working-with-fields/) Artículo de documentación.

```csharp
public class DropDownItemCollection : IEnumerable<string>
```

## Propiedades

| Nombre | Descripción |
| --- | --- |
| [Count](../../aspose.words.fields/dropdownitemcollection/count/) { get; } | Obtiene el número de elementos contenidos en la colección. |
| [Item](../../aspose.words.fields/dropdownitemcollection/item/) { get; set; } | Obtiene o establece el elemento en el índice especificado. |

## Métodos

| Nombre | Descripción |
| --- | --- |
| [Add](../../aspose.words.fields/dropdownitemcollection/add/)(*string*) | Agrega una cadena al final de la colección. |
| [Clear](../../aspose.words.fields/dropdownitemcollection/clear/)() | Elimina todos los elementos de la colección. |
| [Contains](../../aspose.words.fields/dropdownitemcollection/contains/)(*string*) | Determina si la colección contiene el valor especificado. |
| [GetEnumerator](../../aspose.words.fields/dropdownitemcollection/getenumerator/)() | Devuelve un objeto enumerador que se puede utilizar para iterar sobre todos los elementos de la colección. |
| [IndexOf](../../aspose.words.fields/dropdownitemcollection/indexof/)(*string*) | Devuelve el índice basado en cero del valor especificado en la colección. |
| [Insert](../../aspose.words.fields/dropdownitemcollection/insert/)(*int, string*) | Inserta una cadena en la colección en el índice especificado. |
| [Remove](../../aspose.words.fields/dropdownitemcollection/remove/)(*string*) | Elimina el valor especificado de la colección. |
| [RemoveAt](../../aspose.words.fields/dropdownitemcollection/removeat/)(*int*) | Elimina un valor en el índice especificado. |

## Ejemplos

Muestra cómo insertar un campo de cuadro combinado y editar los elementos en su colección de elementos.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Inserte un cuadro combinado y luego verifique su colección de elementos desplegables.
// En Microsoft Word, el usuario hará clic en el cuadro combinado,
// y luego elija uno de los elementos de texto de la colección para mostrar.
string[] items = { "One", "Two", "Three" };
FormField comboBoxField = builder.InsertComboBox("DropDown", items, 0);
DropDownItemCollection dropDownItems = comboBoxField.DropDownItems;

Assert.AreEqual(3, dropDownItems.Count);
Assert.AreEqual("One", dropDownItems[0]);
Assert.AreEqual(1, dropDownItems.IndexOf("Two"));
Assert.IsTrue(dropDownItems.Contains("Three"));

// Hay dos formas de agregar un nuevo elemento a una colección existente de elementos del cuadro desplegable.
// 1 - Agrega un elemento al final de la colección:
dropDownItems.Add("Four");

// 2 - Insertar un elemento antes de otro elemento en un índice especificado:
dropDownItems.Insert(3, "Three and a half");

Assert.AreEqual(5, dropDownItems.Count);

// Itera sobre la colección e imprime cada elemento.
using (IEnumerator<string> dropDownCollectionEnumerator = dropDownItems.GetEnumerator())
    while (dropDownCollectionEnumerator.MoveNext())
        Console.WriteLine(dropDownCollectionEnumerator.Current);

// Hay dos formas de eliminar elementos de una colección de elementos desplegables.
// 1 - Eliminar un elemento con contenido igual a la cadena pasada:
dropDownItems.Remove("Four");

// 2 - Eliminar un elemento en un índice:
dropDownItems.RemoveAt(3);

Assert.AreEqual(3, dropDownItems.Count);
Assert.IsFalse(dropDownItems.Contains("Three and a half"));
Assert.IsFalse(dropDownItems.Contains("Four"));

doc.Save(ArtifactsDir + "FormFields.DropDownItemCollection.html");

// Vacía toda la colección de elementos desplegables.
dropDownItems.Clear();
```

### Ver también

* class [FormField](../formfield/)
* property [DropDownItems](../formfield/dropdownitems/)
* espacio de nombres [Aspose.Words.Fields](../../aspose.words.fields/)
* asamblea [Aspose.Words](../../)
