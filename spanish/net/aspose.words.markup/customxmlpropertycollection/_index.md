---
title: Class CustomXmlPropertyCollection
second_title: Referencia de API de Aspose.Words para .NET
description: Aspose.Words.Markup.CustomXmlPropertyCollection clase. Representa una colección de atributos XML personalizados o propiedades de etiquetas inteligentes.
type: docs
weight: 3710
url: /es/net/aspose.words.markup/customxmlpropertycollection/
---
## CustomXmlPropertyCollection class

Representa una colección de atributos XML personalizados o propiedades de etiquetas inteligentes.

```csharp
public class CustomXmlPropertyCollection : IEnumerable<CustomXmlProperty>
```

## Propiedades

| Nombre | Descripción |
| --- | --- |
| [Count](../../aspose.words.markup/customxmlpropertycollection/count/) { get; } | Obtiene el número de elementos que contiene la colección. |
| [Item](../../aspose.words.markup/customxmlpropertycollection/item/) { get; } | Obtiene una propiedad con el nombre especificado. (2 indexers) |

## Métodos

| Nombre | Descripción |
| --- | --- |
| [Add](../../aspose.words.markup/customxmlpropertycollection/add/)(CustomXmlProperty) | Agrega una propiedad a la colección. |
| [Clear](../../aspose.words.markup/customxmlpropertycollection/clear/)() | Elimina todos los elementos de la colección. |
| [Contains](../../aspose.words.markup/customxmlpropertycollection/contains/)(string) | Determina si la colección contiene una propiedad con el nombre dado. |
| [GetEnumerator](../../aspose.words.markup/customxmlpropertycollection/getenumerator/)() | Devuelve un objeto enumerador que se puede usar para iterar sobre todos los elementos de la colección. |
| [IndexOfKey](../../aspose.words.markup/customxmlpropertycollection/indexofkey/)(string) | Devuelve el índice basado en cero de la propiedad especificada en la colección. |
| [Remove](../../aspose.words.markup/customxmlpropertycollection/remove/)(string) | Elimina una propiedad con el nombre especificado de la colección. |
| [RemoveAt](../../aspose.words.markup/customxmlpropertycollection/removeat/)(int) | Elimina una propiedad en el índice especificado. |

### Observaciones

Los artículos son[`CustomXmlProperty`](../customxmlproperty/) objetos.

### Ejemplos

Muestra cómo trabajar con las propiedades de las etiquetas inteligentes para obtener información detallada sobre las etiquetas inteligentes.

```csharp
Document doc = new Document(MyDir + "Smart tags.doc");

// Aparece una etiqueta inteligente en un documento con Microsoft Word que reconoce una parte de su texto como algún tipo de datos,
// como un nombre, fecha o dirección, y lo convierte en un hipervínculo que muestra un subrayado punteado de color púrpura.
// En Word 2003, podemos habilitar etiquetas inteligentes a través de "Herramientas" -> "Opciones de Autocorrección..." -> "Etiquetas inteligentes".
// En nuestro documento de entrada, hay tres objetos que Microsoft Word registró como etiquetas inteligentes.
// Las etiquetas inteligentes se pueden anidar, por lo que esta colección contiene más.
SmartTag[] smartTags = doc.GetChildNodes(NodeType.SmartTag, true).OfType<SmartTag>().ToArray();

Assert.AreEqual(8, smartTags.Length);

// El miembro "Propiedades" de una etiqueta inteligente contiene sus metadatos, que serán diferentes para cada tipo de etiqueta inteligente.
// Las propiedades de una etiqueta inteligente de tipo "fecha" contienen su año, mes y día.
CustomXmlPropertyCollection properties = smartTags[7].Properties;

Assert.AreEqual(4, properties.Count);

using (IEnumerator<CustomXmlProperty> enumerator = properties.GetEnumerator())
{
    while (enumerator.MoveNext())
    {
        Console.WriteLine($"Property name: {enumerator.Current.Name}, value: {enumerator.Current.Value}");
        Assert.AreEqual("", enumerator.Current.Uri);
    }
}

// También podemos acceder a las propiedades de varias formas, como un par clave-valor.
Assert.True(properties.Contains("Day"));
Assert.AreEqual("22", properties["Day"].Value);
Assert.AreEqual("2003", properties[2].Value);
Assert.AreEqual(1, properties.IndexOfKey("Month"));

// A continuación se muestran tres formas de eliminar elementos de la colección de propiedades.
// 1 - Eliminar por índice:
properties.RemoveAt(3);

Assert.AreEqual(3, properties.Count);

// 2 - Eliminar por nombre:
properties.Remove("Year");

Assert.AreEqual(2, properties.Count);

// 3 - Borrar toda la colección de una sola vez:
properties.Clear();

Assert.AreEqual(0, properties.Count);
```

### Ver también

* class [CustomXmlProperty](../customxmlproperty/)
* espacio de nombres [Aspose.Words.Markup](../../aspose.words.markup/)
* asamblea [Aspose.Words](../../)


