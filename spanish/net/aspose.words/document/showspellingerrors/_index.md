---
title: Document.ShowSpellingErrors
linktitle: ShowSpellingErrors
articleTitle: ShowSpellingErrors
second_title: Aspose.Words para .NET
description: Controle la visibilidad de los errores ortográficos en su documento con la propiedad ShowSpellingErrors. Optimice su proceso de edición y mejore la calidad del documento.
type: docs
weight: 420
url: /es/net/aspose.words/document/showspellingerrors/
---
## Document.ShowSpellingErrors property

Especifica si se deben mostrar errores ortográficos en este documento.

```csharp
public bool ShowSpellingErrors { get; set; }
```

## Ejemplos

Muestra cómo mostrar/ocultar errores en el documento.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Insertar dos oraciones con errores que se detectarían
// por los correctores ortográficos y gramaticales de Microsoft Word.
builder.Writeln("There is a speling error in this sentence.");
builder.Writeln("Their is a grammatical error in this sentence.");

// Si estas opciones están habilitadas, los errores ortográficos se subrayarán.
// en el documento de salida mediante una línea roja irregular y una línea azul doble resaltará los errores gramaticales.
doc.ShowGrammaticalErrors = showErrors;
doc.ShowSpellingErrors = showErrors;

doc.Save(ArtifactsDir + "Document.SpellingAndGrammarErrors.docx");
```

### Ver también

* class [Document](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)
