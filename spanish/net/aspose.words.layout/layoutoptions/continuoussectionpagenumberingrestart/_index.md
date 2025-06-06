---
title: LayoutOptions.ContinuousSectionPageNumberingRestart
linktitle: ContinuousSectionPageNumberingRestart
articleTitle: ContinuousSectionPageNumberingRestart
second_title: Aspose.Words para .NET
description: Descubra la propiedad LayoutOptions ContinuousSectionPageNumberingRestart para un control preciso de la numeración de páginas en secciones continuas. ¡Optimice el diseño de su documento hoy mismo!
type: docs
weight: 40
url: /es/net/aspose.words.layout/layoutoptions/continuoussectionpagenumberingrestart/
---
## LayoutOptions.ContinuousSectionPageNumberingRestart property

Obtiene o establece el modo de comportamiento para calcular los números de página cuando una sección continua reinicia la numeración de páginas.

```csharp
public ContinuousSectionRestart ContinuousSectionPageNumberingRestart { get; set; }
```

## Observaciones

El valor predeterminado esAlways . Coincide con el comportamiento de MS Word 2019, que era la última versión en el momento en que se introdujo la opción. La lógica de numeración de páginas más antigua demostrada por MS Word 2016 está disponible a través de esta opción. Por favor[`ContinuousSectionRestart`](../../continuoussectionrestart/) para la descripción del comportamiento.

## Ejemplos

Muestra cómo controlar la numeración de páginas en una sección continua.

```csharp
Document doc = new Document(MyDir + "Continuous section page numbering.docx");

// De forma predeterminada, el comportamiento de Aspose.Words coincide con Microsoft Word 2019.
// Si necesita el comportamiento antiguo de Aspose.Words, repetitivo de Microsoft Word 2016, utilice 'ContinuousSectionRestart.FromNewPageOnly'.
// La numeración de páginas se reinicia solo si no hay otro contenido antes de la sección en la página donde comienza la sección.
// debido a esto la numeración se restablecerá a 2 a partir de la segunda página.
doc.LayoutOptions.ContinuousSectionPageNumberingRestart = ContinuousSectionRestart.FromNewPageOnly;
doc.UpdatePageLayout();

doc.Save(ArtifactsDir + "Layout.RestartPageNumberingInContinuousSection.pdf");
```

### Ver también

* enum [ContinuousSectionRestart](../../continuoussectionrestart/)
* class [LayoutOptions](../)
* espacio de nombres [Aspose.Words.Layout](../../../aspose.words.layout/)
* asamblea [Aspose.Words](../../../)
