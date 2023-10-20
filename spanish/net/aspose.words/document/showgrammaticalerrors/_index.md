---
title: Document.ShowGrammaticalErrors
linktitle: ShowGrammaticalErrors
articleTitle: ShowGrammaticalErrors
second_title: Aspose.Words para .NET
description: Document ShowGrammaticalErrors propiedad. Especifica si se muestran errores gramaticales en este documento en C#.
type: docs
weight: 390
url: /es/net/aspose.words/document/showgrammaticalerrors/
---
## Document.ShowGrammaticalErrors property

Especifica si se muestran errores gramaticales en este documento.

```csharp
public bool ShowGrammaticalErrors { get; set; }
```

## Ejemplos

Muestra cómo mostrar/ocultar errores en el documento.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Inserta dos oraciones con errores que se detectarían
// por los correctores ortográficos y gramaticales de Microsoft Word.
builder.Writeln("There is a speling error in this sentence.");
builder.Writeln("Their is a grammatical error in this sentence.");

// Si estas opciones están habilitadas, los errores ortográficos se subrayarán
// en el documento de salida por una línea roja irregular, y una doble línea azul resaltará los errores gramaticales.
doc.ShowGrammaticalErrors = showErrors;
doc.ShowSpellingErrors = showErrors;

doc.Save(ArtifactsDir + "Document.SpellingAndGrammarErrors.docx");
```

### Ver también

* class [Document](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)
