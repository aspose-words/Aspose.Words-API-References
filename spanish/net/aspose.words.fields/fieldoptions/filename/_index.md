---
title: FieldOptions.FileName
linktitle: FileName
articleTitle: FileName
second_title: Aspose.Words para .NET
description: FieldOptions FileName propiedad. Obtiene o establece el nombre de archivo del documento en C#.
type: docs
weight: 140
url: /es/net/aspose.words.fields/fieldoptions/filename/
---
## FieldOptions.FileName property

Obtiene o establece el nombre de archivo del documento.

```csharp
public string FileName { get; set; }
```

## Observaciones

Esta propiedad es utilizada por el[`FieldFileName`](../../fieldfilename/) campo con mayor prioridad que el[`OriginalFileName`](../../../aspose.words/document/originalfilename/) propiedad.

## Ejemplos

Muestra cómo utilizar FieldOptions para anular el valor predeterminado para el campo NOMBRE DE ARCHIVO.

```csharp
Document doc = new Document(MyDir + "Document.docx");
DocumentBuilder builder = new DocumentBuilder(doc);

builder.MoveToDocumentEnd();
builder.Writeln();

// Este campo FILENAME mostrará el nombre del archivo del sistema local del documento que cargamos.
FieldFileName field = (FieldFileName)builder.InsertField(FieldType.FieldFileName, true);
field.Update();

Assert.AreEqual(" FILENAME ", field.GetFieldCode());
Assert.AreEqual("Document.docx", field.Result);

builder.Writeln();

// De forma predeterminada, el campo FILENAME muestra el nombre del archivo, pero no la ruta completa del sistema de archivos local.
// Podemos establecer una bandera para que muestre la ruta completa del archivo.
field = (FieldFileName)builder.InsertField(FieldType.FieldFileName, true);
field.IncludeFullPath = true;
field.Update();

Assert.AreEqual(MyDir + "Document.docx", field.Result);

// También podemos establecer un valor para esta propiedad en
// anula el valor que muestra el campo NOMBRE DE ARCHIVO.
doc.FieldOptions.FileName = "FieldOptions.FILENAME.docx";
field.Update();

Assert.AreEqual(" FILENAME  \\p", field.GetFieldCode());
Assert.AreEqual("FieldOptions.FILENAME.docx", field.Result);

doc.UpdateFields();
doc.Save(ArtifactsDir + doc.FieldOptions.FileName);
```

### Ver también

* class [FieldOptions](../)
* espacio de nombres [Aspose.Words.Fields](../../../aspose.words.fields/)
* asamblea [Aspose.Words](../../../)
