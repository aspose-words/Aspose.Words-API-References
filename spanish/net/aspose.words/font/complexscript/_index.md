---
title: Font.ComplexScript
linktitle: ComplexScript
articleTitle: ComplexScript
second_title: Aspose.Words para .NET
description: Font ComplexScript propiedad. Especifica si el contenido de esta ejecución se tratará como texto de script complejo independientemente de sus valores de caracteres Unicode al determinar el formato para esta ejecución en C#.
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

Muestra cómo agregar texto que siempre se trata como un script complejo.

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
