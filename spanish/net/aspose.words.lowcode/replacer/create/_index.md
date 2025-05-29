---
title: Replacer.Create
linktitle: Create
articleTitle: Create
second_title: Aspose.Words para .NET
description: Descubra cómo el método Create de Replacer genera una nueva instancia del eficiente procesador de reemplazo para una transformación de datos perfecta.
type: docs
weight: 10
url: /es/net/aspose.words.lowcode/replacer/create/
---
## Replacer.Create method

Crea una nueva instancia del procesador de reemplazo.

```csharp
public static Replacer Create(ReplacerContext context)
```

## Ejemplos

Muestra cómo reemplazar una cadena con una expresión regular en el documento usando el contexto.

```csharp
// Hay varias formas de reemplazar una cadena con una expresión regular en el documento:
string doc = MyDir + "Footer.docx";
Regex pattern = new Regex("gr(a|e)y");
string replacement = "lavender";

ReplacerContext replacerContext = new ReplacerContext();
replacerContext.SetReplacement(pattern, replacement);
replacerContext.FindReplaceOptions.FindWholeWordsOnly = false;

Replacer.Create(replacerContext)
    .From(doc)
    .To(ArtifactsDir + "LowCode.ReplaceContextRegex.docx")
    .Execute();
```

Muestra cómo reemplazar una cadena en el documento usando el contexto.

```csharp
// Hay varias formas de reemplazar una cadena en el documento:
string doc = MyDir + "Footer.docx";
string pattern = "(C)2006 Aspose Pty Ltd.";
string replacement = "Copyright (C) 2024 by Aspose Pty Ltd.";

ReplacerContext replacerContext = new ReplacerContext();
replacerContext.SetReplacement(pattern, replacement);
replacerContext.FindReplaceOptions.FindWholeWordsOnly = false;

Replacer.Create(replacerContext)
    .From(doc)
    .To(ArtifactsDir + "LowCode.ReplaceContext.docx")
    .Execute();
```

Muestra cómo reemplazar una cadena en el documento usando documentos de la secuencia usando contexto.

```csharp
// Hay varias formas de reemplazar una cadena en el documento usando documentos del flujo:
string pattern = "(C)2006 Aspose Pty Ltd.";
string replacement = "Copyright (C) 2024 by Aspose Pty Ltd.";

using (FileStream streamIn = new FileStream(MyDir + "Footer.docx", FileMode.Open, FileAccess.Read))
{
    ReplacerContext replacerContext = new ReplacerContext();
    replacerContext.SetReplacement(pattern, replacement);
    replacerContext.FindReplaceOptions.FindWholeWordsOnly = false;

    using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.ReplaceContextStream.docx", FileMode.Create, FileAccess.ReadWrite))
        Replacer.Create(replacerContext)
        .From(streamIn)
        .To(streamOut, SaveFormat.Docx)
        .Execute();
}
```

Muestra cómo reemplazar una cadena con una expresión regular en el documento usando documentos de la secuencia que usa el contexto.

```csharp
// Hay varias formas de reemplazar una cadena con una expresión regular en el documento usando documentos del flujo:
Regex pattern = new Regex("gr(a|e)y");
string replacement = "lavender";

using (FileStream streamIn = new FileStream(MyDir + "Replace regex.docx", FileMode.Open, FileAccess.Read))
{
    ReplacerContext replacerContext = new ReplacerContext();
    replacerContext.SetReplacement(pattern, replacement);
    replacerContext.FindReplaceOptions.FindWholeWordsOnly = false;

    using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.ReplaceContextStreamRegex.docx", FileMode.Create, FileAccess.ReadWrite))
        Replacer.Create(replacerContext)
            .From(streamIn)
            .To(streamOut, SaveFormat.Docx)
            .Execute();
}
```

### Ver también

* class [ReplacerContext](../../replacercontext/)
* class [Replacer](../)
* espacio de nombres [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* asamblea [Aspose.Words](../../../)
