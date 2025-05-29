---
title: VariableCollection.IndexOfKey
linktitle: IndexOfKey
articleTitle: IndexOfKey
second_title: Aspose.Words para .NET
description: Descubra el método IndexOfKey de VariableCollection. Encuentre rápidamente el índice de base cero de la variable de su documento para una gestión eficiente de los datos.
type: docs
weight: 70
url: /es/net/aspose.words/variablecollection/indexofkey/
---
## VariableCollection.IndexOfKey method

Devuelve el índice basado en cero de la variable de documento especificada en la colección.

```csharp
public int IndexOfKey(string name)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| name | String | El nombre de la variable que no distingue entre mayúsculas y minúsculas. |

### Valor_devuelto

Índice basado en cero. Valor negativo si no se encuentra.

## Ejemplos

Muestra cómo trabajar con la colección de variables de un documento.

```csharp
Document doc = new Document();
VariableCollection variables = doc.Variables;

// Cada documento tiene una colección de variables de pares clave/valor, a las que podemos agregar elementos.
variables.Add("Home address", "123 Main St.");
variables.Add("City", "London");
variables.Add("Bedrooms", "3");

Assert.AreEqual(3, variables.Count);

// Podemos mostrar los valores de las variables en el cuerpo del documento utilizando campos DOCVARIABLE.
DocumentBuilder builder = new DocumentBuilder(doc);
FieldDocVariable field = (FieldDocVariable)builder.InsertField(FieldType.FieldDocVariable, true);
field.VariableName = "Home address";
field.Update();

Assert.AreEqual("123 Main St.", field.Result);

// Asignar valores a claves existentes las actualizará.
variables.Add("Home address", "456 Queen St.");

Luego tendremos que actualizar los campos DOCVARIABLE para asegurarnos de que muestren un valor actualizado.
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

Assert.AreEqual("3", variables[0]);
Assert.AreEqual("London", variables["City"]);

// Enumerar sobre la colección de variables.
using (IEnumerator<KeyValuePair<string, string>> enumerator = doc.Variables.GetEnumerator())
    while (enumerator.MoveNext())
        Console.WriteLine($"Name: {enumerator.Current.Key}, Value: {enumerator.Current.Value}");

A continuación se muestran tres formas de eliminar variables de documento de una colección.
// 1 - Por nombre:
variables.Remove("City");

Assert.False(variables.Contains("City"));

// 2 - Por índice:
variables.RemoveAt(1);

Assert.False(variables.Contains("Home address"));

// 3 - Limpiar toda la colección a la vez:
variables.Clear();

Assert.AreEqual(0, variables.Count);
```

### Ver también

* class [VariableCollection](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)
