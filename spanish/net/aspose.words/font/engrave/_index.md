---
title: Font.Engrave
linktitle: Engrave
articleTitle: Engrave
second_title: Aspose.Words para .NET
description: Descubra la propiedad Font Engrave. Formatee fácilmente las fuentes para lograr un elegante aspecto grabado, realzando la sofisticación y el atractivo de su diseño.
type: docs
weight: 120
url: /es/net/aspose.words/font/engrave/
---
## Font.Engrave property

Verdadero si la fuente está formateada como grabada.

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
