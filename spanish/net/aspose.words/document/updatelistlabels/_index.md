---
title: Document.UpdateListLabels
second_title: Referencia de API de Aspose.Words para .NET
description: Document método. Actualiza las etiquetas de la lista para todos los elementos de la lista en el documento.
type: docs
weight: 780
url: /es/net/aspose.words/document/updatelistlabels/
---
## Document.UpdateListLabels method

Actualiza las etiquetas de la lista para todos los elementos de la lista en el documento.

```csharp
public void UpdateListLabels()
```

### Observaciones

Este método actualiza las propiedades de la etiqueta de la lista, como[`LabelValue`](../../../aspose.words.lists/listlabel/labelvalue/) y [`LabelString`](../../../aspose.words.lists/listlabel/labelstring/) para cada[`ListLabel`](../../paragraph/listlabel/)objeto en el documento.

Además, a veces este método se llama implícitamente al actualizar campos en el documento. Esto es obligatorio porque algunos campos que pueden hacer referencia a números de lista (como TOC o REF) necesitan que estén actualizados.

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

* class [Document](../)
* espacio de nombres [Aspose.Words](../../document/)
* asamblea [Aspose.Words](../../../)


