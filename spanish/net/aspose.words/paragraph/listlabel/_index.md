---
title: Paragraph.ListLabel
linktitle: ListLabel
articleTitle: ListLabel
second_title: Aspose.Words para .NET
description: Acceda y formatee la numeración de listas con la propiedad ListLabel de párrafo. ¡Mejore la organización y claridad de su documento sin esfuerzo!
type: docs
weight: 160
url: /es/net/aspose.words/paragraph/listlabel/
---
## Paragraph.ListLabel property

Obtiene un`ListLabel`objeto que proporciona acceso al valor de numeración de lista y formato para este párrafo.

```csharp
public ListLabel ListLabel { get; }
```

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

* class [ListLabel](../../../aspose.words.lists/listlabel/)
* class [Paragraph](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)
