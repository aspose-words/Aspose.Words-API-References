---
title: ImportFormatOptions.IgnoreHeaderFooter
linktitle: IgnoreHeaderFooter
articleTitle: IgnoreHeaderFooter
second_title: Aspose.Words para .NET
description: ImportFormatOptions IgnoreHeaderFooter propiedad. Obtiene o establece un valor booleano que especifica que el formato de origen del contenido de encabezados/pies de página se ignora siKeepSourceFormatting Se utiliza el modo. El valor predeterminado esverdadero  en C#.
type: docs
weight: 40
url: /es/net/aspose.words/importformatoptions/ignoreheaderfooter/
---
## ImportFormatOptions.IgnoreHeaderFooter property

Obtiene o establece un valor booleano que especifica que el formato de origen del contenido de encabezados/pies de página se ignora siKeepSourceFormatting Se utiliza el modo. El valor predeterminado es`verdadero` .

```csharp
public bool IgnoreHeaderFooter { get; set; }
```

## Ejemplos

Muestra cómo especificar ignorar o no el formato de origen del contenido de encabezados/pies de página.

```csharp
Document dstDoc = new Document(MyDir + "Document.docx");
Document srcDoc = new Document(MyDir + "Header and footer types.docx");

ImportFormatOptions importFormatOptions = new ImportFormatOptions();
importFormatOptions.IgnoreHeaderFooter = false;

dstDoc.AppendDocument(srcDoc, ImportFormatMode.KeepSourceFormatting, importFormatOptions);

dstDoc.Save(ArtifactsDir + "DocumentBuilder.DoNotIgnoreHeaderFooter.docx");
```

### Ver también

* class [ImportFormatOptions](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)
