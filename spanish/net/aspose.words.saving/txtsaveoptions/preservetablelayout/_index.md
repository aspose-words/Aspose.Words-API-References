---
title: TxtSaveOptions.PreserveTableLayout
linktitle: PreserveTableLayout
articleTitle: PreserveTableLayout
second_title: Aspose.Words para .NET
description: Descubra la función PreserveTableLayout de TxtSaveOptions, que garantiza que sus tablas conserven su diseño al guardarlas como texto sin formato. ¡Mejore la legibilidad de sus documentos!
type: docs
weight: 50
url: /es/net/aspose.words.saving/txtsaveoptions/preservetablelayout/
---
## TxtSaveOptions.PreserveTableLayout property

Especifica si el programa debe intentar conservar el diseño de las tablas al guardar en formato de texto sin formato. El valor predeterminado es`FALSO` .

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

// Crea un objeto "TxtSaveOptions", que podemos pasar al método "Guardar" del documento
// para modificar la forma en que guardamos el documento en texto plano.
TxtSaveOptions txtSaveOptions = new TxtSaveOptions();

// Establezca la propiedad "PreserveTableLayout" en "verdadero" para aplicar relleno de espacios en blanco al contenido
// del documento de texto simple de salida para preservar la mayor parte posible del diseño de la tabla.
// Establezca la propiedad "PreserveTableLayout" en "falso" para guardar el contenido de todas las tablas
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
