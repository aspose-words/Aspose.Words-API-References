---
title: ImportFormatOptions.IgnoreHeaderFooter
linktitle: IgnoreHeaderFooter
articleTitle: IgnoreHeaderFooter
second_title: Aspose.Words para .NET
description: Descubra la propiedad ImportFormatOptions IgnoreHeaderFooter, que controla el formato de encabezado/pie de página en el modo KeepSourceFormatting. ¡Simplifique la importación de sus documentos hoy mismo!
type: docs
weight: 40
url: /es/net/aspose.words/importformatoptions/ignoreheaderfooter/
---
## ImportFormatOptions.IgnoreHeaderFooter property

Obtiene o establece un valor booleano que especifica que se ignora el formato de origen del contenido de encabezados/pies de página siKeepSourceFormatting Se utiliza el modo. El valor predeterminado es`verdadero` .

```csharp
public bool IgnoreHeaderFooter { get; set; }
```

## Ejemplos

Muestra cómo especificar si se debe ignorar o no el formato de origen del contenido de encabezados y pies de página.

```csharp
Document dstDoc = new Document(MyDir + "Document.docx");
Document srcDoc = new Document(MyDir + "Header and footer types.docx");

// Si 'IgnoreHeaderFooter' es falso, entonces se mantendrá el formato original para el contenido del encabezado/pie de página.
// Se utilizará el archivo "Tipos de encabezado y pie de página.docx".
// Si 'IgnoreHeaderFooter' es verdadero, entonces el formato para el contenido del encabezado/pie de página
//Se utilizará el archivo "Document.docx".
ImportFormatOptions importFormatOptions = new ImportFormatOptions();
importFormatOptions.IgnoreHeaderFooter = false;

dstDoc.AppendDocument(srcDoc, ImportFormatMode.KeepSourceFormatting, importFormatOptions);

dstDoc.Save(ArtifactsDir + "DocumentBuilder.DoNotIgnoreHeaderFooter.docx");
```

### Ver también

* class [ImportFormatOptions](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)
