---
title: ListLabel.LabelValue
second_title: Referencia de API de Aspose.Words para .NET
description: ListLabel propiedad. Obtiene un valor numérico para esta etiqueta.
type: docs
weight: 30
url: /es/net/aspose.words.lists/listlabel/labelvalue/
---
## ListLabel.LabelValue property

Obtiene un valor numérico para esta etiqueta.

```csharp
public int LabelValue { get; }
```

### Observaciones

Utilice el[`UpdateListLabels`](../../../aspose.words/document/updatelistlabels/) método para actualizar el valor de esta propiedad.

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

* class [ListLabel](../)
* espacio de nombres [Aspose.Words.Lists](../../listlabel/)
* asamblea [Aspose.Words](../../../)


