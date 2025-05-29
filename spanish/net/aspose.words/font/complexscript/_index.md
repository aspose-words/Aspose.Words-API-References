---
title: Font.ComplexScript
linktitle: ComplexScript
articleTitle: ComplexScript
second_title: Aspose.Words para .NET
description: Descubra la propiedad Font ComplexScript, que garantiza que su texto tenga formato de escritura compleja para mejorar la legibilidad y el estilo, independientemente de los valores Unicode.
type: docs
weight: 80
url: /es/net/aspose.words/font/complexscript/
---
## Font.ComplexScript property

Especifica si el contenido de esta ejecución se tratará como texto de script complejo independientemente de sus valores de caracteres Unicode al determinar el formato para esta ejecución.

```csharp
public bool ComplexScript { get; set; }
```

## Ejemplos

Muestra cómo agregar texto que siempre se trata como una escritura compleja.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.ComplexScript = true;

builder.Writeln("Text treated as complex script.");

doc.Save(ArtifactsDir + "Font.ComplexScript.docx");
```

### Ver también

* class [Font](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)
