---
title: ImportFormatOptions.IgnoreTextBoxes
second_title: Referencia de API de Aspose.Words para .NET
description: ImportFormatOptions propiedad. Obtiene o establece un valor booleano que especifica que el formato de origen del contenido de los cuadros de texto se ignora siKeepSourceFormatting Se utiliza el modo. El valor predeterminado esverdadero .
type: docs
weight: 50
url: /es/net/aspose.words/importformatoptions/ignoretextboxes/
---
## ImportFormatOptions.IgnoreTextBoxes property

Obtiene o establece un valor booleano que especifica que el formato de origen del contenido de los cuadros de texto se ignora siKeepSourceFormatting Se utiliza el modo. El valor predeterminado es`verdadero` .

```csharp
public bool IgnoreTextBoxes { get; set; }
```

### Ejemplos

Muestra cómo administrar el formato de cuadro de texto al agregar un documento.

```csharp
// Crea un documento que tendrá nodos de otro documento insertados en él.
Document dstDoc = new Document();
DocumentBuilder builder = new DocumentBuilder(dstDoc);

builder.Writeln("Hello world!");

// Crea otro documento con un cuadro de texto, que importaremos al primer documento.
Document srcDoc = new Document();
builder = new DocumentBuilder(srcDoc);

Shape textBox = builder.InsertShape(ShapeType.TextBox, 300, 100);
builder.MoveTo(textBox.FirstParagraph);
builder.ParagraphFormat.Style.Font.Name = "Courier New";
builder.ParagraphFormat.Style.Font.Size = 24;
builder.Write("Textbox contents");

// Establece una bandera para especificar si se borra o conserva el formato del cuadro de texto
// mientras los importa a otros documentos.
ImportFormatOptions importFormatOptions = new ImportFormatOptions();
importFormatOptions.IgnoreTextBoxes = ignoreTextBoxes;

// Importa el cuadro de texto del documento de origen al documento de destino,
// y luego verificar si hemos conservado el estilo de su contenido de texto.
NodeImporter importer = new NodeImporter(srcDoc, dstDoc, ImportFormatMode.KeepSourceFormatting, importFormatOptions);
Shape importedTextBox = (Shape)importer.ImportNode(textBox, true);
dstDoc.FirstSection.Body.Paragraphs[1].AppendChild(importedTextBox);

if (ignoreTextBoxes)
{
    Assert.AreEqual(12.0d, importedTextBox.FirstParagraph.Runs[0].Font.Size);
    Assert.AreEqual("Times New Roman", importedTextBox.FirstParagraph.Runs[0].Font.Name);
}
else
{
    Assert.AreEqual(24.0d, importedTextBox.FirstParagraph.Runs[0].Font.Size);
    Assert.AreEqual("Courier New", importedTextBox.FirstParagraph.Runs[0].Font.Name);
}

dstDoc.Save(ArtifactsDir + "DocumentBuilder.IgnoreTextBoxes.docx");
```

### Ver también

* class [ImportFormatOptions](../)
* espacio de nombres [Aspose.Words](../../importformatoptions/)
* asamblea [Aspose.Words](../../../)


