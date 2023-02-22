---
title: Font.Shadow
second_title: Referencia de API de Aspose.Words para .NET
description: Font propiedad. Verdadero si la fuente está formateada como sombreada.
type: docs
weight: 330
url: /es/net/aspose.words/font/shadow/
---
## Font.Shadow property

Verdadero si la fuente está formateada como sombreada.

```csharp
public bool Shadow { get; set; }
```

### Ejemplos

Muestra cómo crear una tirada de texto formateado con una sombra.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Establecer la bandera Sombra para aplicar un efecto de sombra desplazada,
// haciendo que parezca que las letras flotan sobre la página.
builder.Font.Shadow = true;
builder.Font.Size = 36;

builder.Writeln("This text has a shadow.");

doc.Save(ArtifactsDir + "Font.Shadow.docx");
```

### Ver también

* class [Font](../)
* espacio de nombres [Aspose.Words](../../font/)
* asamblea [Aspose.Words](../../../)


