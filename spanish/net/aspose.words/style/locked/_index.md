---
title: Style.Locked
linktitle: Locked
articleTitle: Locked
second_title: Aspose.Words para .NET
description: Descubre la propiedad Estilo Bloqueado y controla el bloqueo de estilos para mayor flexibilidad y consistencia en tus proyectos. ¡Libera tu creatividad hoy mismo!
type: docs
weight: 120
url: /es/net/aspose.words/style/locked/
---
## Style.Locked property

Especifica si este estilo está bloqueado.

```csharp
public bool Locked { get; set; }
```

## Ejemplos

Muestra cómo bloquear el estilo.

```csharp
Document doc = new Document();

Style styleHeading1 = doc.Styles[StyleIdentifier.Heading1];
if (!styleHeading1.Locked)
    styleHeading1.Locked = true;

doc.Save(ArtifactsDir + "Styles.LockStyle.docx");
```

### Ver también

* class [Style](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)
