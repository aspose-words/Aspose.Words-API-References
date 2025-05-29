---
title: ImportFormatOptions.IgnoreTextBoxes
linktitle: IgnoreTextBoxes
articleTitle: IgnoreTextBoxes
second_title: Aspose.Words para .NET
description: Descubra cómo la propiedad ImportFormatOptions IgnoreTextBoxes mejora el formato de su documento controlando el contenido de los cuadros de texto. ¡Optimice fácilmente hoy mismo!
type: docs
weight: 50
url: /es/net/aspose.words/importformatoptions/ignoretextboxes/
---
## ImportFormatOptions.IgnoreTextBoxes property

Obtiene o establece un valor booleano que especifica que se ignora el formato de origen del contenido de los cuadros de texto siKeepSourceFormatting Se utiliza el modo. El valor predeterminado es`verdadero` .

```csharp
public bool IgnoreTextBoxes { get; set; }
```

## Ejemplos

Muestra cómo administrar el formato del cuadro de texto al agregar un documento.

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

// Establezca un indicador para especificar si se debe borrar o conservar el formato del cuadro de texto
// al importarlos a otros documentos.
ImportFormatOptions importFormatOptions = new ImportFormatOptions();
importFormatOptions.IgnoreTextBoxes = ignoreTextBoxes;

// Importar el cuadro de texto del documento de origen al documento de destino,
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
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)
