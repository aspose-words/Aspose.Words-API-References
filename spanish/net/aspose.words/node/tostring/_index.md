---
title: ToString
second_title: Referencia de API de Aspose.Words para .NET
description: Exporta el contenido del nodo a una cadena en el formato especificado.
type: docs
weight: 160
url: /es/net/aspose.words/node/tostring/
---
## ToString(SaveFormat) {#tostring_1}

Exporta el contenido del nodo a una cadena en el formato especificado.

```csharp
public string ToString(SaveFormat saveFormat)
```

### Valor_devuelto

El contenido del nodo en el formato especificado.

### Ejemplos

Muestra la diferencia entre llamar a los métodos GetText y ToString en un nodo.

```csharp
Document doc = new Document();

DocumentBuilder builder = new DocumentBuilder(doc);
builder.InsertField("MERGEFIELD Field");

// GetText recuperará el texto visible, así como los códigos de campo y los caracteres especiales.
Assert.AreEqual("\u0013MERGEFIELD Field\u0014«Field»\u0015\u000c", doc.GetText());

// ToString nos dará la apariencia del documento si se guarda en un formato de guardado aprobado.
Assert.AreEqual("«Field»\r\n", doc.ToString(SaveFormat.Text));
```

Exporta el contenido de un nodo a String en formato HTML.

```csharp
Document doc = new Document(MyDir + "Document.docx");

Node node = doc.LastSection.Body.LastParagraph;

// Cuando llamamos al método ToString usando la sobrecarga html SaveFormat,
// convierte el contenido del nodo a su representación html sin procesar.
Assert.AreEqual("<p style=\"margin-top:0pt; margin-bottom:8pt; line-height:108%; font-size:12pt\">" +
                "<span style=\"font-family:'Times New Roman'\">Hello World!</span>" +
                "</p>", node.ToString(SaveFormat.Html));

// También podemos modificar el resultado de esta conversión utilizando un objeto SaveOptions.
HtmlSaveOptions saveOptions = new HtmlSaveOptions();
saveOptions.ExportRelativeFontSize = true;

Assert.AreEqual("<p style=\"margin-top:0pt; margin-bottom:8pt; line-height:108%\">" +
                "<span style=\"font-family:'Times New Roman'\">Hello World!</span>" +
                "</p>", node.ToString(saveOptions));
```

Muestra cómo extraer las etiquetas de lista de todos los párrafos que son elementos de lista.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");
doc.UpdateListLabels();

NodeCollection paras = doc.GetChildNodes(NodeType.Paragraph, true);

// Encuentra si tenemos la lista de párrafos. En nuestro documento, nuestra lista usa números arábigos simples,
// que comienzan a las tres y terminan a las seis.
foreach (Paragraph paragraph in paras.OfType<Paragraph>().Where(p => p.ListFormat.IsListItem))
{
    Console.WriteLine($"List item paragraph #{paras.IndexOf(paragraph)}");

    // Este es el texto que obtenemos cuando enviamos este nodo a formato de texto.
    // Esta salida de texto omitirá las etiquetas de lista. Recorte cualquier carácter de formato de párrafo. 
    string paragraphText = paragraph.ToString(SaveFormat.Text).Trim();
    Console.WriteLine($"\tExported Text: {paragraphText}");

    ListLabel label = paragraph.ListLabel;

    // Esto obtiene la posición del párrafo en el nivel actual de la lista. Si tenemos una lista con múltiples niveles,
    // esto nos dirá en qué posición está en ese nivel.
    Console.WriteLine($"\tNumerical Id: {label.LabelValue}");

    // Combinarlos para incluir la etiqueta de la lista con el texto en la salida.
    Console.WriteLine($"\tList label combined with text: {label.LabelString} {paragraphText}");
}
```

### Ver también

* enum [SaveFormat](../../saveformat/)
* class [Node](../)
* espacio de nombres [Aspose.Words](../../node/)
* asamblea [Aspose.Words](../../../)

---

## ToString(SaveOptions) {#tostring_2}

Exporta el contenido del nodo a una cadena utilizando las opciones de guardado especificadas.

```csharp
public string ToString(SaveOptions saveOptions)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| saveOptions | SaveOptions | Especifica las opciones que controlan cómo se guarda el nodo. |

### Valor_devuelto

El contenido del nodo en el formato especificado.

### Ejemplos

Exporta el contenido de un nodo a String en formato HTML.

```csharp
Document doc = new Document(MyDir + "Document.docx");

Node node = doc.LastSection.Body.LastParagraph;

// Cuando llamamos al método ToString usando la sobrecarga html SaveFormat,
// convierte el contenido del nodo a su representación html sin procesar.
Assert.AreEqual("<p style=\"margin-top:0pt; margin-bottom:8pt; line-height:108%; font-size:12pt\">" +
                "<span style=\"font-family:'Times New Roman'\">Hello World!</span>" +
                "</p>", node.ToString(SaveFormat.Html));

// También podemos modificar el resultado de esta conversión utilizando un objeto SaveOptions.
HtmlSaveOptions saveOptions = new HtmlSaveOptions();
saveOptions.ExportRelativeFontSize = true;

Assert.AreEqual("<p style=\"margin-top:0pt; margin-bottom:8pt; line-height:108%\">" +
                "<span style=\"font-family:'Times New Roman'\">Hello World!</span>" +
                "</p>", node.ToString(saveOptions));
```

### Ver también

* class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* class [Node](../)
* espacio de nombres [Aspose.Words](../../node/)
* asamblea [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
