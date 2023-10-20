---
title: ImportFormatOptions Class
linktitle: ImportFormatOptions
articleTitle: ImportFormatOptions
second_title: Aspose.Words para .NET
description: Aspose.Words.ImportFormatOptions clase. Permite especificar varias opciones de importación para formatear la salida en C#.
type: docs
weight: 3240
url: /es/net/aspose.words/importformatoptions/
---
## ImportFormatOptions class

Permite especificar varias opciones de importación para formatear la salida.

Para obtener más información, visite el[Especificar opciones de carga](https://docs.aspose.com/words/net/specify-load-options/) artículo de documentación.

```csharp
public class ImportFormatOptions
```

## Constructores

| Nombre | Descripción |
| --- | --- |
| [ImportFormatOptions](importformatoptions/)() | Constructor predeterminado |

## Propiedades

| Nombre | Descripción |
| --- | --- |
| [AdjustSentenceAndWordSpacing](../../aspose.words/importformatoptions/adjustsentenceandwordspacing/) { get; set; } | Obtiene o establece un valor booleano que especifica si se debe ajustar el espaciado entre oraciones y palabras automáticamente. El valor predeterminado es`FALSO` . |
| [ForceCopyStyles](../../aspose.words/importformatoptions/forcecopystyles/) { get; set; } | Obtiene o establece un valor booleano que indica si se deben copiar estilos conflictivos enKeepSourceFormatting mode. El valor predeterminado es`FALSO` . |
| [IgnoreHeaderFooter](../../aspose.words/importformatoptions/ignoreheaderfooter/) { get; set; } | Obtiene o establece un valor booleano que especifica que el formato de origen del contenido de encabezados/pies de página se ignora siKeepSourceFormatting Se utiliza el modo. El valor predeterminado es`verdadero` . |
| [IgnoreTextBoxes](../../aspose.words/importformatoptions/ignoretextboxes/) { get; set; } | Obtiene o establece un valor booleano que especifica que el formato de origen del contenido de los cuadros de texto se ignora siKeepSourceFormatting Se utiliza el modo. El valor predeterminado es`verdadero` . |
| [KeepSourceNumbering](../../aspose.words/importformatoptions/keepsourcenumbering/) { get; set; } | Obtiene o establece un valor booleano que especifica cómo se importará la numeración cuando entre en conflicto en los documentos de origen y de destino. El valor predeterminado es`FALSO` . |
| [MergePastedLists](../../aspose.words/importformatoptions/mergepastedlists/) { get; set; } | Obtiene o establece un valor booleano que especifica si las listas pegadas se fusionarán con las listas circundantes. El valor predeterminado es`FALSO` . |
| [SmartStyleBehavior](../../aspose.words/importformatoptions/smartstylebehavior/) { get; set; } | Obtiene o establece un valor booleano que especifica cómo se importarán los estilos cuando tienen nombres iguales en los documentos de origen y de destino. El valor predeterminado es`FALSO` . |

## Ejemplos

Muestra cómo resolver estilos duplicados al insertar documentos.

```csharp
Document dstDoc = new Document();
DocumentBuilder builder = new DocumentBuilder(dstDoc);

Style myStyle = builder.Document.Styles.Add(StyleType.Paragraph, "MyStyle");
myStyle.Font.Size = 14;
myStyle.Font.Name = "Courier New";
myStyle.Font.Color = Color.Blue;

builder.ParagraphFormat.StyleName = myStyle.Name;
builder.Writeln("Hello world!");

// Clona el documento y edita el estilo "MyStyle" del clon, para que tenga un color diferente al del original.
// Si insertamos el clon en el documento original, los dos estilos con el mismo nombre provocarán un choque.
Document srcDoc = dstDoc.Clone();
srcDoc.Styles["MyStyle"].Font.Color = Color.Red;

// Cuando habilitamos SmartStyleBehavior y usamos el modo de formato de importación KeepSourceFormatting,
// Aspose.Words resolverá los conflictos de estilos convirtiendo los estilos del documento fuente.
// con los mismos nombres que los estilos de destino en atributos de párrafo directo.
ImportFormatOptions options = new ImportFormatOptions();
options.SmartStyleBehavior = true;

builder.InsertDocument(srcDoc, ImportFormatMode.KeepSourceFormatting, options);

dstDoc.Save(ArtifactsDir + "DocumentBuilder.SmartStyleBehavior.docx");
```

### Ver también

* espacio de nombres [Aspose.Words](../../aspose.words/)
* asamblea [Aspose.Words](../../)
