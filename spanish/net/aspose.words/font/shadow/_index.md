---
title: Font.Shadow
linktitle: Shadow
articleTitle: Shadow
second_title: Aspose.Words para .NET
description: Descubra la propiedad Font Shadow, mejore su texto con elegantes efectos de sombra para lograr un atractivo visual sorprendente en sus diseños.
type: docs
weight: 340
url: /es/net/aspose.words/font/shadow/
---
## Font.Shadow property

Verdadero si la fuente está formateada como sombreada.

```csharp
public bool Shadow { get; set; }
```

## Ejemplos

Muestra cómo crear una serie de texto formateada con sombra.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Establezca la bandera Sombra para aplicar un efecto de sombra desplazado,
//haciendo que parezca que las letras flotan sobre la página.
builder.Font.Shadow = true;
builder.Font.Size = 36;

builder.Writeln("This text has a shadow.");

doc.Save(ArtifactsDir + "Font.Shadow.docx");
```

### Ver también

* class [Font](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)
