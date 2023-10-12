---
title: LayoutOptions.ContinuousSectionPageNumberingRestart
second_title: Referencia de API de Aspose.Words para .NET
description: LayoutOptions propiedad. Obtiene o establece el modo de comportamiento para calcular los números de página cuando una sección continua reinicia la numeración de páginas.
type: docs
weight: 40
url: /es/net/aspose.words.layout/layoutoptions/continuoussectionpagenumberingrestart/
---
## LayoutOptions.ContinuousSectionPageNumberingRestart property

Obtiene o establece el modo de comportamiento para calcular los números de página cuando una sección continua reinicia la numeración de páginas.

```csharp
public ContinuousSectionRestart ContinuousSectionPageNumberingRestart { get; set; }
```

### Observaciones

El valor predeterminado esAlways. Coincide con el comportamiento de MS Word 2019, que era la última versión en el momento en que se introdujo la opción. La lógica de numeración de páginas anterior demostrada por MS Word 2016 está disponible a través de esta opción. Por favor[`ContinuousSectionRestart`](../../continuoussectionrestart/) para la descripción del comportamiento.

### Ejemplos

Muestra cómo controlar la numeración de páginas en una sección continua.

```csharp
Document doc = new Document(MyDir + "Continuous section page numbering.docx");

// De forma predeterminada, el comportamiento de Aspose.Words coincide con Microsoft Word 2019.
// Si necesita un comportamiento antiguo de Aspose.Words, repetitivo de Microsoft Word 2016, use 'ContinuousSectionRestart.FromNewPageOnly'.
// La numeración de páginas se reinicia solo si no hay otro contenido antes de la sección en la página donde comienza la sección,
// debido a eso la numeración se restablecerá a 2 desde la segunda página.
doc.LayoutOptions.ContinuousSectionPageNumberingRestart = ContinuousSectionRestart.FromNewPageOnly;
doc.UpdatePageLayout();

doc.Save(ArtifactsDir + "Layout.RestartPageNumberingInContinuousSection.pdf");
```

### Ver también

* enum [ContinuousSectionRestart](../../continuoussectionrestart/)
* class [LayoutOptions](../)
* espacio de nombres [Aspose.Words.Layout](../../layoutoptions/)
* asamblea [Aspose.Words](../../../)


