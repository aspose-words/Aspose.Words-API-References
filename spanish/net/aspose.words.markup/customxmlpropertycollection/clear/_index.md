---
title: CustomXmlPropertyCollection.Clear
second_title: Referencia de API de Aspose.Words para .NET
description: CustomXmlPropertyCollection método. Elimina todos los elementos de la colección.
type: docs
weight: 40
url: /es/net/aspose.words.markup/customxmlpropertycollection/clear/
---
## CustomXmlPropertyCollection.Clear method

Elimina todos los elementos de la colección.

```csharp
public void Clear()
```

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

* class [CustomXmlPropertyCollection](../)
* espacio de nombres [Aspose.Words.Markup](../../customxmlpropertycollection/)
* asamblea [Aspose.Words](../../../)


