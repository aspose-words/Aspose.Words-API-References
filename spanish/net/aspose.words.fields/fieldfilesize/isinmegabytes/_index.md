---
title: FieldFileSize.IsInMegabytes
linktitle: IsInMegabytes
articleTitle: IsInMegabytes
second_title: Aspose.Words para .NET
description: FieldFileSize IsInMegabytes propiedad. Obtiene o establece si se muestra el tamaño del archivo en megabytes en C#.
type: docs
weight: 30
url: /es/net/aspose.words.fields/fieldfilesize/isinmegabytes/
---
## FieldFileSize.IsInMegabytes property

Obtiene o establece si se muestra el tamaño del archivo en megabytes.

```csharp
public bool IsInMegabytes { get; set; }
```

## Ejemplos

Muestra cómo mostrar el tamaño de archivo de un documento con un campo FILESIZE.

```csharp
Document doc = new Document(MyDir + "Document.docx");

Assert.AreEqual(18105, doc.BuiltInDocumentProperties.Bytes);

DocumentBuilder builder = new DocumentBuilder(doc);
builder.MoveToDocumentEnd();
builder.InsertParagraph();

// A continuación se muestran tres unidades de medida diferentes
// con qué campos FILESIZE pueden mostrar el tamaño del archivo del documento.
// 1 - Bytes:
FieldFileSize field = (FieldFileSize)builder.InsertField(FieldType.FieldFileSize, true);
field.Update();

Assert.AreEqual(" FILESIZE ", field.GetFieldCode());
Assert.AreEqual("18105", field.Result);

// 2 - Kilobytes:
builder.InsertParagraph();
field = (FieldFileSize)builder.InsertField(FieldType.FieldFileSize, true);
field.IsInKilobytes = true;
field.Update();

Assert.AreEqual(" FILESIZE  \\k", field.GetFieldCode());
Assert.AreEqual("18", field.Result);

// 3 - Megabytes:
builder.InsertParagraph();
field = (FieldFileSize)builder.InsertField(FieldType.FieldFileSize, true);
field.IsInMegabytes = true;
field.Update();

Assert.AreEqual(" FILESIZE  \\m", field.GetFieldCode());
Assert.AreEqual("0", field.Result);

// Para actualizar los valores de estos campos mientras se editan en Microsoft Word,
// primero debemos guardar los cambios y luego actualizar manualmente estos campos.
doc.Save(ArtifactsDir + "Field.FILESIZE.docx");
```

### Ver también

* class [FieldFileSize](../)
* espacio de nombres [Aspose.Words.Fields](../../../aspose.words.fields/)
* asamblea [Aspose.Words](../../../)
