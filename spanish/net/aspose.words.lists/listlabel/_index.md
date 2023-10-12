---
title: Class ListLabel
second_title: Referencia de API de Aspose.Words para .NET
description: Aspose.Words.Lists.ListLabel clase. Define propiedades específicas de una etiqueta de lista.
type: docs
weight: 3490
url: /es/net/aspose.words.lists/listlabel/
---
## ListLabel class

Define propiedades específicas de una etiqueta de lista.

Para obtener más información, visite el[Trabajar con listas](https://docs.aspose.com/words/net/working-with-lists/) artículo de documentación.

```csharp
public class ListLabel
```

## Propiedades

| Nombre | Descripción |
| --- | --- |
| [Font](../../aspose.words.lists/listlabel/font/) { get; } | Obtiene la fuente de la etiqueta de la lista. |
| [LabelString](../../aspose.words.lists/listlabel/labelstring/) { get; } | Obtiene una representación de cadena de la etiqueta de la lista. |
| [LabelValue](../../aspose.words.lists/listlabel/labelvalue/) { get; } | Obtiene un valor numérico para esta etiqueta. |

### Ejemplos

Muestra cómo extraer las etiquetas de la lista de todos los párrafos que son elementos de la lista.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");
doc.UpdateListLabels();

NodeCollection paras = doc.GetChildNodes(NodeType.Paragraph, true);

// Encuentra si tenemos la lista de párrafos. En nuestro documento, nuestra lista utiliza números arábigos simples,
// que empieza a las tres y termina a las seis.
foreach (Paragraph paragraph in paras.OfType<Paragraph>().Where(p => p.ListFormat.IsListItem))
{
    Console.WriteLine($"List item paragraph #{paras.IndexOf(paragraph)}");

    // Este es el texto que obtenemos cuando enviamos este nodo al formato de texto.
     // Esta salida de texto omitirá las etiquetas de la lista. Recorte los caracteres de formato de párrafo.
    string paragraphText = paragraph.ToString(SaveFormat.Text).Trim();
    Console.WriteLine($"\tExported Text: {paragraphText}");

    ListLabel label = paragraph.ListLabel;

    // Esto obtiene la posición del párrafo en el nivel actual de la lista. Si tenemos una lista con múltiples niveles,
    // esto nos dirá en qué posición se encuentra en ese nivel.
    Console.WriteLine($"\tNumerical Id: {label.LabelValue}");

    // Combínalos para incluir la etiqueta de la lista con el texto en la salida.
    Console.WriteLine($"\tList label combined with text: {label.LabelString} {paragraphText}");
}
```

### Ver también

* espacio de nombres [Aspose.Words.Lists](../../aspose.words.lists/)
* asamblea [Aspose.Words](../../)


