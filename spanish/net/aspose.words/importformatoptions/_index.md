---
title: ImportFormatOptions Class
linktitle: ImportFormatOptions
articleTitle: ImportFormatOptions
second_title: Aspose.Words para .NET
description: Descubra Aspose.Words.ImportFormatOptions para personalizar el formato de sus documentos. Mejore sus resultados con configuraciones de importación personalizadas para obtener resultados óptimos.
type: docs
weight: 3690
url: /es/net/aspose.words/importformatoptions/
---
## ImportFormatOptions class

Permite especificar varias opciones de importación para formatear la salida.

Para obtener más información, visite el[Especificar opciones de carga](https://docs.aspose.com/words/net/specify-load-options/) Artículo de documentación.

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
| [AdjustSentenceAndWordSpacing](../../aspose.words/importformatoptions/adjustsentenceandwordspacing/) { get; set; } | Obtiene o establece un valor booleano que especifica si se debe ajustar automáticamente el espaciado entre oraciones y palabras. El valor predeterminado es`FALSO` . |
| [ForceCopyStyles](../../aspose.words/importformatoptions/forcecopystyles/) { get; set; } | Obtiene o establece un valor booleano que indica que se deben copiar los estilos conflictivos enKeepSourceFormatting mode. El valor predeterminado es`FALSO` . |
| [IgnoreHeaderFooter](../../aspose.words/importformatoptions/ignoreheaderfooter/) { get; set; } | Obtiene o establece un valor booleano que especifica que se ignora el formato de origen del contenido de encabezados/pies de página siKeepSourceFormatting Se utiliza el modo. El valor predeterminado es`verdadero` . |
| [IgnoreTextBoxes](../../aspose.words/importformatoptions/ignoretextboxes/) { get; set; } | Obtiene o establece un valor booleano que especifica que se ignora el formato de origen del contenido de los cuadros de texto siKeepSourceFormatting Se utiliza el modo. El valor predeterminado es`verdadero` . |
| [KeepSourceNumbering](../../aspose.words/importformatoptions/keepsourcenumbering/) { get; set; } | Obtiene o establece un valor booleano que especifica cómo se importará la numeración cuando entre en conflicto en los documentos de origen y destino. El valor predeterminado es`FALSO` . |
| [MergePastedLists](../../aspose.words/importformatoptions/mergepastedlists/) { get; set; } | Obtiene o establece un valor booleano que especifica si las listas pegadas se fusionarán con las listas circundantes. El valor predeterminado es`FALSO` . |
| [SmartStyleBehavior](../../aspose.words/importformatoptions/smartstylebehavior/) { get; set; } | Obtiene o establece un valor booleano que especifica cómo se importarán los estilos cuando tengan nombres iguales en los documentos de origen y destino. El valor predeterminado es`FALSO` . |

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

// Clona el documento y edita el estilo "MyStyle" del clon, para que sea de un color diferente al del original.
// Si insertamos el clon en el documento original, los dos estilos con el mismo nombre provocarán un conflicto.
Document srcDoc = dstDoc.Clone();
srcDoc.Styles["MyStyle"].Font.Color = Color.Red;

// Cuando habilitamos SmartStyleBehavior y usamos el modo de formato de importación KeepSourceFormatting,
// Aspose.Words resolverá los conflictos de estilo convirtiendo los estilos del documento fuente.
// con los mismos nombres que los estilos de destino en atributos de párrafo directo.
ImportFormatOptions options = new ImportFormatOptions();
options.SmartStyleBehavior = true;

builder.InsertDocument(srcDoc, ImportFormatMode.KeepSourceFormatting, options);

dstDoc.Save(ArtifactsDir + "DocumentBuilder.SmartStyleBehavior.docx");
```

### Ver también

* espacio de nombres [Aspose.Words](../../aspose.words/)
* asamblea [Aspose.Words](../../)
