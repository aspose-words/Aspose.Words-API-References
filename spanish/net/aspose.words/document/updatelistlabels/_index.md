---
title: Document.UpdateListLabels
linktitle: UpdateListLabels
articleTitle: UpdateListLabels
second_title: Aspose.Words para .NET
description: Actualice sin esfuerzo todas las etiquetas de los elementos de la lista en su documento con el método UpdateListLabels, garantizando la coherencia y la claridad de su contenido.
type: docs
weight: 820
url: /es/net/aspose.words/document/updatelistlabels/
---
## Document.UpdateListLabels method

Actualiza las etiquetas de lista para todos los elementos de lista en el documento.

```csharp
public void UpdateListLabels()
```

## Observaciones

Este método actualiza las propiedades de la etiqueta de la lista, como[`LabelValue`](../../../aspose.words.lists/listlabel/labelvalue/) y [`LabelString`](../../../aspose.words.lists/listlabel/labelstring/) para cada uno[`ListLabel`](../../paragraph/listlabel/) objeto en el documento.

Además, este método a veces se llama implícitamente al actualizar campos en el documento. Esto es obligatorio porque algunos campos que pueden hacer referencia a números de lista (como TOC o REF) requieren que estén actualizados.

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

* class [Document](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)
