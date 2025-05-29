---
title: FieldAdvance.UpOffset
linktitle: UpOffset
articleTitle: UpOffset
second_title: Aspose.Words para .NET
description: Descubra cómo la propiedad FieldAdvance UpOffset mejora el posicionamiento del texto en sus documentos ajustando el texto posterior hacia arriba para lograr una apariencia mejorada.
type: docs
weight: 60
url: /es/net/aspose.words.fields/fieldadvance/upoffset/
---
## FieldAdvance.UpOffset property

Obtiene o establece el número de puntos que debe moverse hacia arriba el texto que sigue al campo.

```csharp
public string UpOffset { get; set; }
```

## Ejemplos

Muestra cómo insertar un campo ADVANCE y editar sus propiedades.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("This text is in its normal place.");

// A continuación se muestran dos formas de utilizar el campo AVANCE para ajustar la posición del texto que lo sigue.
// Los efectos de un campo ADVANCE continúan aplicándose hasta que finaliza el párrafo,
// u otro campo ADVANCE actualiza los valores de desplazamiento/coordenadas.
// 1 - Especifique un desplazamiento direccional:
FieldAdvance field = (FieldAdvance)builder.InsertField(FieldType.FieldAdvance, true);
field.RightOffset = "5";
field.UpOffset = "5";

Assert.AreEqual(" ADVANCE  \\r 5 \\u 5", field.GetFieldCode());

builder.Write("This text will be moved up and to the right.");

field = (FieldAdvance)builder.InsertField(FieldType.FieldAdvance, true);
field.DownOffset = "5";
field.LeftOffset = "100";

Assert.AreEqual(" ADVANCE  \\d 5 \\l 100", field.GetFieldCode());

builder.Writeln("This text is moved down and to the left, overlapping the previous text.");

// 2 - Mover el texto a una posición especificada por coordenadas:
field = (FieldAdvance)builder.InsertField(FieldType.FieldAdvance, true);
field.HorizontalPosition = "-100";
field.VerticalPosition = "200";

Assert.AreEqual(" ADVANCE  \\x -100 \\y 200", field.GetFieldCode());

builder.Write("This text is in a custom position.");

doc.Save(ArtifactsDir + "Field.ADVANCE.docx");
```

### Ver también

* class [FieldAdvance](../)
* espacio de nombres [Aspose.Words.Fields](../../../aspose.words.fields/)
* asamblea [Aspose.Words](../../../)
