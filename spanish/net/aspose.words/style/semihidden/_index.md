---
title: Style.SemiHidden
linktitle: SemiHidden
articleTitle: SemiHidden
second_title: Aspose.Words para .NET
description: Descubra cómo la propiedad SemiHidden controla la visibilidad del estilo en la galería Estilos y el panel de tareas, mejorando su flujo de trabajo y eficiencia de diseño.
type: docs
weight: 170
url: /es/net/aspose.words/style/semihidden/
---
## Style.SemiHidden property

Obtiene/establece si el estilo se oculta en la galería de Estilos y en el panel de tareas Estilos.

```csharp
public bool SemiHidden { get; set; }
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
