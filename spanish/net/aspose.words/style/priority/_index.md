---
title: Style.Priority
linktitle: Priority
articleTitle: Priority
second_title: Aspose.Words para .NET
description: Descubra cómo gestionar la configuración de Prioridad de Estilo para optimizar la ordenación de estilos en su panel de tareas. ¡Mejore su flujo de trabajo con una organización de estilos eficiente!
type: docs
weight: 160
url: /es/net/aspose.words/style/priority/
---
## Style.Priority property

Obtiene/establece el valor entero que representa la prioridad para ordenar los estilos en el panel de tareas Estilos.

```csharp
public int Priority { get; set; }
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
