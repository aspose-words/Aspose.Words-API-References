---
title: Class VariableCollection
second_title: Referencia de API de Aspose.Words para .NET
description: Aspose.Words.VariableCollection clase. Una colección de variables de documento.
type: docs
weight: 6230
url: /es/net/aspose.words/variablecollection/
---
## VariableCollection class

Una colección de variables de documento.

```csharp
public class VariableCollection : IEnumerable<KeyValuePair<string, string>>
```

## Propiedades

| Nombre | Descripción |
| --- | --- |
| [Count](../../aspose.words/variablecollection/count/) { get; } | Obtiene el número de elementos que contiene la colección. |
| [Item](../../aspose.words/variablecollection/item/) { get; set; } | Obtiene o establece una variable de documento por el nombre que no distingue entre mayúsculas y minúsculas. Los valores nulos no están permitidos como lado derecho de la asignación y serán reemplazados por una cadena vacía. (2 indexers) |

## Métodos

| Nombre | Descripción |
| --- | --- |
| [Add](../../aspose.words/variablecollection/add/)(string, string) | Agrega una variable de documento a la colección. |
| [Clear](../../aspose.words/variablecollection/clear/)() | Elimina todos los elementos de la colección. |
| [Contains](../../aspose.words/variablecollection/contains/)(string) | Determina si la colección contiene una variable de documento con el nombre dado. |
| [GetEnumerator](../../aspose.words/variablecollection/getenumerator/)() | Devuelve un objeto enumerador que se puede usar para iterar sobre todas las variables de la colección. |
| [IndexOfKey](../../aspose.words/variablecollection/indexofkey/)(string) | Devuelve el índice de base cero de la variable de documento especificada en la colección. |
| [Remove](../../aspose.words/variablecollection/remove/)(string) | Elimina una variable de documento con el nombre especificado de la colección. |
| [RemoveAt](../../aspose.words/variablecollection/removeat/)(int) | Elimina una variable de documento en el índice especificado. |

### Observaciones

Los nombres y valores de las variables son cadenas.

Los nombres de las variables no distinguen entre mayúsculas y minúsculas.

### Ejemplos

Muestra cómo trabajar con la colección de variables de un documento.

```csharp
Document doc = new Document();
VariableCollection variables = doc.Variables;

// Cada documento tiene una colección de variables de par clave/valor, a las que podemos agregar elementos.
variables.Add("Home address", "123 Main St.");
variables.Add("City", "London");
variables.Add("Bedrooms", "3");

Assert.AreEqual(3, variables.Count);

// Podemos mostrar los valores de las variables en el cuerpo del documento usando campos DOCVARIABLE.
DocumentBuilder builder = new DocumentBuilder(doc);
FieldDocVariable field = (FieldDocVariable)builder.InsertField(FieldType.FieldDocVariable, true);
field.VariableName = "Home address";
field.Update();

Assert.AreEqual("123 Main St.", field.Result);

// La asignación de valores a las claves existentes las actualizará.
variables.Add("Home address", "456 Queen St.");

// Luego tendremos que actualizar los campos DOCVARIABLE para asegurarnos de que muestren un valor actualizado.
Assert.AreEqual("123 Main St.", field.Result);

field.Update();

Assert.AreEqual("456 Queen St.", field.Result);

// Verificar que existan las variables del documento con un determinado nombre o valor.
Assert.True(variables.Contains("City"));
Assert.True(variables.Any(v => v.Value == "London"));

// La colección de variables ordena automáticamente las variables alfabéticamente por nombre.
Assert.AreEqual(0, variables.IndexOfKey("Bedrooms"));
Assert.AreEqual(1, variables.IndexOfKey("City"));
Assert.AreEqual(2, variables.IndexOfKey("Home address"));

// Enumerar sobre la colección de variables.
using (IEnumerator<KeyValuePair<string, string>> enumerator = doc.Variables.GetEnumerator())
    while (enumerator.MoveNext())
        Console.WriteLine($"Name: {enumerator.Current.Key}, Value: {enumerator.Current.Value}");

// A continuación se muestran tres formas de eliminar variables de documentos de una colección.
// 1 - Por nombre:
variables.Remove("City");

Assert.False(variables.Contains("City"));

// 2 - Por índice:
variables.RemoveAt(1);

Assert.False(variables.Contains("Home address"));

// 3 - Borrar toda la colección de una vez:
variables.Clear();

Assert.That(variables, Is.Empty);
```

### Ver también

* espacio de nombres [Aspose.Words](../../aspose.words/)
* asamblea [Aspose.Words](../../)


