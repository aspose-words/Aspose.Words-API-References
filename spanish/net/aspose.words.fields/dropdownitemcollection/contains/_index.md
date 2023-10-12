---
title: DropDownItemCollection.Contains
second_title: Referencia de API de Aspose.Words para .NET
description: DropDownItemCollection método. Determina si la colección contiene el valor especificado.
type: docs
weight: 50
url: /es/net/aspose.words.fields/dropdownitemcollection/contains/
---
## DropDownItemCollection.Contains method

Determina si la colección contiene el valor especificado.

```csharp
public bool Contains(string value)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| value | String | Valor que distingue entre mayúsculas y minúsculas para localizar. |

### Valor_devuelto

`verdadero` si el artículo se encuentra en la colección; de lo contrario,`FALSO`.

### Ejemplos

Muestra cómo insertar un campo de cuadro combinado y editar los elementos de su colección de elementos.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Inserta un cuadro combinado y luego verifica su colección de elementos desplegables.
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

// 2 - Insertar un elemento antes de otro elemento en un índice específico:
dropDownItems.Insert(3, "Three and a half");

Assert.AreEqual(5, dropDownItems.Count);

// Iterar sobre la colección e imprimir cada elemento.
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

// Vaciar toda la colección de elementos desplegables.
dropDownItems.Clear();
```

### Ver también

* class [DropDownItemCollection](../)
* espacio de nombres [Aspose.Words.Fields](../../dropdownitemcollection/)
* asamblea [Aspose.Words](../../../)


