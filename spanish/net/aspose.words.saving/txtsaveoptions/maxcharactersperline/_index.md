---
title: TxtSaveOptions.MaxCharactersPerLine
linktitle: MaxCharactersPerLine
articleTitle: MaxCharactersPerLine
second_title: Aspose.Words para .NET
description: TxtSaveOptions MaxCharactersPerLine propiedad. Obtiene o establece un valor entero que especifica el número máximo de caracteres por línea. El valor predeterminado es 0 lo que significa que no hay límite en C#.
type: docs
weight: 40
url: /es/net/aspose.words.saving/txtsaveoptions/maxcharactersperline/
---
## TxtSaveOptions.MaxCharactersPerLine property

Obtiene o establece un valor entero que especifica el número máximo de caracteres por línea. El valor predeterminado es 0, lo que significa que no hay límite.

```csharp
public int MaxCharactersPerLine { get; set; }
```

## Ejemplos

Muestra cómo establecer el número máximo de caracteres por línea.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. " +
              "Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.");

// Establece 30 caracteres como máximo permitido por línea.
TxtSaveOptions saveOptions = new TxtSaveOptions { MaxCharactersPerLine = 30 };

doc.Save(ArtifactsDir + "TxtSaveOptions.MaxCharactersPerLine.txt", saveOptions);
```

### Ver también

* class [TxtSaveOptions](../)
* espacio de nombres [Aspose.Words.Saving](../../../aspose.words.saving/)
* asamblea [Aspose.Words](../../../)
