---
title: Font.NumberSpacing
linktitle: NumberSpacing
articleTitle: NumberSpacing
second_title: Aspose.Words para .NET
description: Descubre la propiedad Font NumberSpacing para personalizar el espaciado numérico y mejorar la legibilidad y el diseño. ¡Optimiza tu tipografía hoy mismo!
type: docs
weight: 290
url: /es/net/aspose.words/font/numberspacing/
---
## Font.NumberSpacing property

Obtiene o establece el tipo de espaciado del numeral que se muestra.

```csharp
public NumSpacing NumberSpacing { get; set; }
```

## Ejemplos

Muestra cómo establecer el tipo de espaciado del numeral.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Este efecto solo es compatible con versiones más nuevas de MS Word.
doc.CompatibilityOptions.OptimizeFor(MsWordVersion.Word2019);

builder.Write("1 ");
builder.Write("This is an example");

Run run = doc.FirstSection.Body.FirstParagraph.Runs[0];
if (run.Font.NumberSpacing == NumSpacing.Default)
    run.Font.NumberSpacing = NumSpacing.Proportional;

doc.Save(ArtifactsDir + "Fonts.NumberSpacing.docx");
```

### Ver también

* enum [NumSpacing](../../numspacing/)
* class [Font](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)
