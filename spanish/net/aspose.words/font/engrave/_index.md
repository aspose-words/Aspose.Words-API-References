---
title: Font.Engrave
linktitle: Engrave
articleTitle: Engrave
second_title: Aspose.Words para .NET
description: Font Engrave propiedad. Verdadero si la fuente tiene el formato grabado en C#.
type: docs
weight: 120
url: /es/net/aspose.words/font/engrave/
---
## Font.Engrave property

Verdadero si la fuente tiene el formato grabado.

```csharp
public bool Engrave { get; set; }
```

## Ejemplos

Muestra cómo aplicar efectos de grabado/relieve al texto.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Size = 36;
builder.Font.Color = Color.LightBlue;

// A continuación se muestran dos formas de utilizar sombras para aplicar un efecto similar a 3D al texto.
// 1 - Grabe el texto para que parezca que las letras están hundidas en la página:
builder.Font.Engrave = true;

builder.Writeln("This text is engraved.");

// 2 - Texto en relieve para que parezca que las letras salen de la página:
builder.Font.Engrave = false;
builder.Font.Emboss = true;

builder.Writeln("This text is embossed.");

doc.Save(ArtifactsDir + "Font.EngraveEmboss.docx");
```

### Ver también

* class [Font](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)
