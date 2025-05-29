---
title: ListLabel Class
linktitle: ListLabel
articleTitle: ListLabel
second_title: Aspose.Words para .NET
description: Explore la clase Aspose.Words.Lists.ListLabel para mejorar el formato de su documento con propiedades de etiqueta de lista personalizables para un mejor control y presentación.
type: docs
weight: 3940
url: /es/net/aspose.words.lists/listlabel/
---
## ListLabel class

Define propiedades específicas de una etiqueta de lista.

Para obtener más información, visite el[Trabajar con listas](https://docs.aspose.com/words/net/working-with-lists/) Artículo de documentación.

```csharp
public class ListLabel
```

## Propiedades

| Nombre | Descripción |
| --- | --- |
| [Font](../../aspose.words.lists/listlabel/font/) { get; } | Obtiene la fuente de la etiqueta de la lista. |
| [LabelString](../../aspose.words.lists/listlabel/labelstring/) { get; } | Obtiene una representación de cadena de la etiqueta de la lista. |
| [LabelValue](../../aspose.words.lists/listlabel/labelvalue/) { get; } | Obtiene un valor numérico para esta etiqueta. |

## Ejemplos

Muestra cómo extraer las etiquetas de lista de todos los párrafos que son elementos de lista.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");
doc.UpdateListLabels();

NodeCollection paras = doc.GetChildNodes(NodeType.Paragraph, true);

// Averigüe si tenemos la lista de párrafos. En nuestro documento, la lista usa números arábigos simples.
// que empiezan en tres y terminan en seis.
foreach (Paragraph paragraph in paras.OfType<Paragraph>().Where(p => p.ListFormat.IsListItem).ToList())
{
    Console.WriteLine($"List item paragraph #{paras.IndexOf(paragraph)}");

    // Este es el texto que obtenemos cuando enviamos este nodo al formato de texto.
     Esta salida de texto omitirá las etiquetas de lista. Recorte los caracteres de formato de párrafo.
    string paragraphText = paragraph.ToString(SaveFormat.Text).Trim();
    Console.WriteLine($"\tExported Text: {paragraphText}");

    ListLabel label = paragraph.ListLabel;

    // Esto obtiene la posición del párrafo en el nivel actual de la lista. Si tenemos una lista con varios niveles,
    //Esto nos dirá qué posición tiene en ese nivel.
    Console.WriteLine($"\tNumerical Id: {label.LabelValue}");

    // Combínalos para incluir la etiqueta de lista con el texto en la salida.
    Console.WriteLine($"\tList label combined with text: {label.LabelString} {paragraphText}");
}
```

### Ver también

* espacio de nombres [Aspose.Words.Lists](../../aspose.words.lists/)
* asamblea [Aspose.Words](../../)
