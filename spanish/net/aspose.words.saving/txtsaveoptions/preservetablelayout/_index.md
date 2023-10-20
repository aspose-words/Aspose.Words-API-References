---
title: TxtSaveOptions.PreserveTableLayout
linktitle: PreserveTableLayout
articleTitle: PreserveTableLayout
second_title: Aspose.Words para .NET
description: TxtSaveOptions PreserveTableLayout propiedad. Especifica si el programa debe intentar conservar el diseño de las tablas al guardarlas en formato de texto sin formato. El valor predeterminado esFALSO  en C#.
type: docs
weight: 50
url: /es/net/aspose.words.saving/txtsaveoptions/preservetablelayout/
---
## TxtSaveOptions.PreserveTableLayout property

Especifica si el programa debe intentar conservar el diseño de las tablas al guardarlas en formato de texto sin formato. El valor predeterminado es`FALSO` .

```csharp
public bool PreserveTableLayout { get; set; }
```

## Ejemplos

Muestra cómo conservar el diseño de las tablas al convertirlas a texto sin formato.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.StartTable();
builder.InsertCell();
builder.Write("Row 1, cell 1");
builder.InsertCell();
builder.Write("Row 1, cell 2");
builder.EndRow();
builder.InsertCell();
builder.Write("Row 2, cell 1");
builder.InsertCell();
builder.Write("Row 2, cell 2");
builder.EndTable();

// Crea un objeto "TxtSaveOptions", que podemos pasar al método "Guardar" del documento.
// para modificar cómo guardamos el documento en texto plano.
TxtSaveOptions txtSaveOptions = new TxtSaveOptions();

// Establece la propiedad "PreserveTableLayout" en "true" para aplicar relleno de espacios en blanco al contenido
// del documento de texto sin formato de salida para preservar la mayor cantidad posible del diseño de la tabla.
// Establece la propiedad "PreserveTableLayout" en "false" para guardar el contenido de todas las tablas
// como un cuerpo de texto continuo, con solo una nueva línea para cada fila.
txtSaveOptions.PreserveTableLayout = preserveTableLayout;

doc.Save(ArtifactsDir + "TxtSaveOptions.PreserveTableLayout.txt", txtSaveOptions);

string docText = File.ReadAllText(ArtifactsDir + "TxtSaveOptions.PreserveTableLayout.txt");

if (preserveTableLayout)
    Assert.AreEqual("Row 1, cell 1                                            Row 1, cell 2\r\n" +
                    "Row 2, cell 1                                            Row 2, cell 2\r\n\r\n", docText);
else
    Assert.AreEqual("Row 1, cell 1\r" +
                    "Row 1, cell 2\r" +
                    "Row 2, cell 1\r" +
                    "Row 2, cell 2\r\r\n", docText);
```

### Ver también

* class [TxtSaveOptions](../)
* espacio de nombres [Aspose.Words.Saving](../../../aspose.words.saving/)
* asamblea [Aspose.Words](../../../)
