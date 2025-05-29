---
title: BuiltInDocumentProperties.HyperlinkBase
linktitle: HyperlinkBase
articleTitle: HyperlinkBase
second_title: Aspose.Words para .NET
description: Descubra la propiedad BuiltInDocumentProperties HyperlinkBase para optimizar los hipervínculos relativos en sus documentos para una navegación fluida y una experiencia de usuario mejorada.
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

// Inserta un hipervínculo relativo a un documento en el sistema de archivos local llamado "Documento.docx".
// Al hacer clic en el enlace en Microsoft Word, se abrirá el documento designado, si está disponible.
builder.InsertHyperlink("Relative hyperlink", "Document.docx", false);

Este enlace es relativo. Si no hay ningún archivo "Document.docx" en la misma carpeta
// como el documento que contiene este enlace, el enlace estará roto.
Assert.False(File.Exists(ArtifactsDir + "Document.docx"));
doc.Save(ArtifactsDir + "DocumentProperties.HyperlinkBase.BrokenLink.docx");

// El documento al que intentamos vincular está en un directorio diferente a aquel en el que planeamos guardar el documento.
 //Podríamos arreglar enlaces como este poniendo un nombre de archivo absoluto en cada uno.
// Alternativamente, podríamos proporcionar un enlace base que cada hipervínculo con un nombre de archivo relativo
 // se antepondrá a su enlace cuando hagamos clic en él.
BuiltInDocumentProperties properties = doc.BuiltInDocumentProperties;
properties.HyperlinkBase = MyDir;

Assert.True(File.Exists(properties.HyperlinkBase + ((FieldHyperlink)doc.Range.Fields[0]).Address));

doc.Save(ArtifactsDir + "DocumentProperties.HyperlinkBase.WorkingLink.docx");
```

### Ver también

* class [BuiltInDocumentProperties](../)
* espacio de nombres [Aspose.Words.Properties](../../../aspose.words.properties/)
* asamblea [Aspose.Words](../../../)
