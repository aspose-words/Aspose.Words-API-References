---
title: DropDownItemCollection.IndexOf
linktitle: IndexOf
articleTitle: IndexOf
second_title: Aspose.Words para .NET
description: Descubra el método IndexOf de DropDownItemCollection, encuentre de manera eficiente el índice basado en cero de cualquier valor en su colección para una gestión optimizada de datos.
type: docs
weight: 70
url: /es/net/aspose.words.fields/dropdownitemcollection/indexof/
---
## DropDownItemCollection.IndexOf method

Devuelve el índice basado en cero del valor especificado en la colección.

```csharp
public int IndexOf(string value)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| value | String | El valor que distingue entre mayúsculas y minúsculas que se va a localizar. |

### Valor_devuelto

Índice basado en cero. Valor negativo si no se encuentra.

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

* class [DropDownItemCollection](../)
* espacio de nombres [Aspose.Words.Fields](../../../aspose.words.fields/)
* asamblea [Aspose.Words](../../../)
