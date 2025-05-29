---
title: Font.Emboss
linktitle: Emboss
articleTitle: Emboss
second_title: Aspose.Words para .NET
description: Descubre la propiedad Font Emboss, que realza tu texto con un elegante efecto de relieve para diseños llamativos. ¡Mejora tu tipografía hoy mismo!
type: docs
weight: 100
url: /es/net/aspose.words/font/emboss/
---
## Font.Emboss property

Verdadero si la fuente está formateada como en relieve.

```csharp
public bool Emboss { get; set; }
```

## Ejemplos

Muestra cómo aplicar efectos de grabado/relieve al texto.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Size = 36;
builder.Font.Color = Color.LightBlue;

// A continuación se muestran dos formas de utilizar sombras para aplicar un efecto 3D al texto.
// 1 - Grabar texto para que parezca que las letras están hundidas en la página:
builder.Font.Engrave = true;

builder.Writeln("This text is engraved.");

// 2 - Relieve el texto para que parezca que las letras salen de la página:
builder.Font.Engrave = false;
builder.Font.Emboss = true;

builder.Writeln("This text is embossed.");

doc.Save(ArtifactsDir + "Font.EngraveEmboss.docx");
```

### Ver también

* class [Font](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)
