---
title: Style.UnhideWhenUsed
linktitle: UnhideWhenUsed
articleTitle: UnhideWhenUsed
second_title: Aspose.Words para .NET
description: Descubra cómo administrar la propiedad UnhideWhenUsed para los estilos. Controle la visibilidad en la galería de estilos y el panel de tareas para mejorar el diseño de su documento.
type: docs
weight: 210
url: /es/net/aspose.words/style/unhidewhenused/
---
## Style.UnhideWhenUsed property

Obtiene/establece si el estilo usado en el documento actual se muestra en la galería de Estilos y en el panel de tareas Estilos. Verdadero cuando el estilo usado debe mostrarse en la galería de Estilos.

```csharp
public bool UnhideWhenUsed { get; set; }
```

## Ejemplos

Muestra cómo priorizar y ocultar un estilo.

```csharp
Document doc = new Document();
Style styleTitle = doc.Styles[StyleIdentifier.Subtitle];

if (styleTitle.Priority == 9)
    styleTitle.Priority = 10;

if (!styleTitle.UnhideWhenUsed)
    styleTitle.UnhideWhenUsed = true;

if (styleTitle.SemiHidden)
    styleTitle.SemiHidden = true;

doc.Save(ArtifactsDir + "Styles.StylePriority.docx");
```

### Ver también

* class [Style](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)
