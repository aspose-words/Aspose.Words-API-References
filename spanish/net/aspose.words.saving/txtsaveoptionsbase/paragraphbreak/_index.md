---
title: TxtSaveOptionsBase.ParagraphBreak
second_title: Referencia de API de Aspose.Words para .NET
description: TxtSaveOptionsBase propiedad. Especifica la cadena que se utilizará como salto de párrafo al exportar en formatos de texto.
type: docs
weight: 40
url: /es/net/aspose.words.saving/txtsaveoptionsbase/paragraphbreak/
---
## TxtSaveOptionsBase.ParagraphBreak property

Especifica la cadena que se utilizará como salto de párrafo al exportar en formatos de texto.

```csharp
public string ParagraphBreak { get; set; }
```

### Observaciones

El valor predeterminado es[`CrLf`](../../../aspose.words/controlchar/crlf/).

### Ejemplos

Muestra cómo guardar un documento .txt con un salto de párrafo personalizado.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Paragraph 1.");
builder.Writeln("Paragraph 2.");
builder.Write("Paragraph 3.");

// Crear un objeto "TxtSaveOptions", que podemos pasar al método "Guardar" del documento
// para modificar cómo guardamos el documento en texto sin formato.
TxtSaveOptions txtSaveOptions = new TxtSaveOptions();

Assert.AreEqual(SaveFormat.Text, txtSaveOptions.SaveFormat);

// Establecer "ParagraphBreak" en un valor personalizado que deseamos poner al final de cada párrafo.
txtSaveOptions.ParagraphBreak = " End of paragraph.\n\n\t";

doc.Save(ArtifactsDir + "TxtSaveOptions.ParagraphBreak.txt", txtSaveOptions);

string docText = File.ReadAllText(ArtifactsDir + "TxtSaveOptions.ParagraphBreak.txt");

Assert.AreEqual("Paragraph 1. End of paragraph.\n\n\t" +
                "Paragraph 2. End of paragraph.\n\n\t" +
                "Paragraph 3. End of paragraph.\n\n\t", docText);
```

### Ver también

* class [TxtSaveOptionsBase](../)
* espacio de nombres [Aspose.Words.Saving](../../txtsaveoptionsbase/)
* asamblea [Aspose.Words](../../../)


