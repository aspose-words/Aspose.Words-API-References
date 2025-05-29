---
title: ImportFormatOptions.SmartStyleBehavior
linktitle: SmartStyleBehavior
articleTitle: SmartStyleBehavior
second_title: Aspose.Words para .NET
description: Descubra cómo la propiedad SmartStyleBehavior ImportFormatOptions optimiza las importaciones de estilos con nombres iguales en los documentos. ¡Personalice su proceso de importación fácilmente!
type: docs
weight: 80
url: /es/net/aspose.words/importformatoptions/smartstylebehavior/
---
## ImportFormatOptions.SmartStyleBehavior property

Obtiene o establece un valor booleano que especifica cómo se importarán los estilos cuando tengan nombres iguales en los documentos de origen y destino. El valor predeterminado es`FALSO` .

```csharp
public bool SmartStyleBehavior { get; set; }
```

## Observaciones

Cuando esta opción está**activado** , el estilo de origen se expandirá a atributos directos dentro del documento de destino a , siKeepSourceFormatting Se utiliza el modo de importación.

Cuando esta opción está**desactivado**El estilo de origen se expandirá solo si está numerado. Los atributos de destino existentes no se sobrescribirán, incluidas las listas.

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

* class [ImportFormatOptions](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)
