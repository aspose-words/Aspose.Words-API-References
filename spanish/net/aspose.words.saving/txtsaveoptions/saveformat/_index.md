---
title: TxtSaveOptions.SaveFormat
second_title: Referencia de API de Aspose.Words para .NET
description: TxtSaveOptions propiedad. Especifica el formato en el que se guardará el documento si se utiliza este objeto de opciones de guardado. Solo se puedeText .
type: docs
weight: 60
url: /es/net/aspose.words.saving/txtsaveoptions/saveformat/
---
## TxtSaveOptions.SaveFormat property

Especifica el formato en el que se guardará el documento si se utiliza este objeto de opciones de guardado. Solo se puedeText .

```csharp
public override SaveFormat SaveFormat { get; set; }
```

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

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [TxtSaveOptions](../)
* espacio de nombres [Aspose.Words.Saving](../../txtsaveoptions/)
* asamblea [Aspose.Words](../../../)


