---
title: BuiltInDocumentProperties.HyperlinkBase
linktitle: HyperlinkBase
articleTitle: HyperlinkBase
second_title: Aspose.Words para .NET
description: BuiltInDocumentProperties HyperlinkBase propiedad. Especifica la cadena base utilizada para evaluar hipervínculos relativos en este documento en C#.
type: docs
weight: 120
url: /es/net/aspose.words.properties/builtindocumentproperties/hyperlinkbase/
---
## BuiltInDocumentProperties.HyperlinkBase property

Especifica la cadena base utilizada para evaluar hipervínculos relativos en este documento.

```csharp
public string HyperlinkBase { get; set; }
```

## Observaciones

Aspose.Words no utiliza esta propiedad.

## Ejemplos

Muestra cómo almacenar la parte base de un hipervínculo en las propiedades del documento.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Inserte un hipervínculo relativo a un documento en el sistema de archivos local llamado "Documento.docx".
// Al hacer clic en el enlace de Microsoft Word se abrirá el documento designado, si está disponible.
builder.InsertHyperlink("Relative hyperlink", "Document.docx", false);

// Este enlace es relativo. Si no hay ningún "Document.docx" en la misma carpeta
// como documento que contiene este enlace, el enlace se romperá.
Assert.False(File.Exists(ArtifactsDir + "Document.docx"));
doc.Save(ArtifactsDir + "DocumentProperties.HyperlinkBase.BrokenLink.docx");

// El documento al que intentamos vincularnos se encuentra en un directorio diferente al que planeamos guardar.
 // Podríamos arreglar enlaces como este poniendo un nombre de archivo absoluto en cada uno.
// Alternativamente, podríamos proporcionar un enlace base que cada hipervínculo tenga un nombre de archivo relativo
 // antepondrá su enlace cuando hagamos clic en él.
BuiltInDocumentProperties properties = doc.BuiltInDocumentProperties;
properties.HyperlinkBase = MyDir;

Assert.True(File.Exists(properties.HyperlinkBase + ((FieldHyperlink)doc.Range.Fields[0]).Address));

doc.Save(ArtifactsDir + "DocumentProperties.HyperlinkBase.WorkingLink.docx");
```

### Ver también

* class [BuiltInDocumentProperties](../)
* espacio de nombres [Aspose.Words.Properties](../../../aspose.words.properties/)
* asamblea [Aspose.Words](../../../)
