---
title: ReplacerContext Class
linktitle: ReplacerContext
articleTitle: ReplacerContext
second_title: Aspose.Words para .NET
description: Descubra la clase Aspose.Words LowCode ReplacerContext para realizar operaciones de búsqueda y reemplazo sin inconvenientes, mejorando la automatización y la eficiencia de sus documentos.
type: docs
weight: 4350
url: /es/net/aspose.words.lowcode/replacercontext/
---
## ReplacerContext class

Contexto de la operación de búsqueda y reemplazo.

```csharp
public class ReplacerContext : ProcessorContext
```

## Constructores

| Nombre | Descripción |
| --- | --- |
| [ReplacerContext](replacercontext/)() | Constructor predeterminado |

## Propiedades

| Nombre | Descripción |
| --- | --- |
| [FindReplaceOptions](../../aspose.words.lowcode/replacercontext/findreplaceoptions/) { get; } | Opciones de búsqueda y reemplazo. |
| [FontSettings](../../aspose.words.lowcode/processorcontext/fontsettings/) { get; set; } | Configuración de fuentes utilizada por el procesador. |
| [LayoutOptions](../../aspose.words.lowcode/processorcontext/layoutoptions/) { get; } | Opciones de diseño de documento utilizadas por el procesador. |
| [WarningCallback](../../aspose.words.lowcode/processorcontext/warningcallback/) { get; set; } | Devolución de llamada de advertencia utilizada por el procesador. |

## Métodos

| Nombre | Descripción |
| --- | --- |
| [SetReplacement](../../aspose.words.lowcode/replacercontext/setreplacement/#setreplacement_1)(*Regex, string*) | Establece el patrón y el reemplazo utilizados por la operación de búsqueda/reemplazo. |
| [SetReplacement](../../aspose.words.lowcode/replacercontext/setreplacement/#setreplacement)(*string, string*) | Establece el patrón y el reemplazo utilizados por la operación de búsqueda/reemplazo. |

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

* class [ProcessorContext](../processorcontext/)
* espacio de nombres [Aspose.Words.LowCode](../../aspose.words.lowcode/)
* asamblea [Aspose.Words](../../)
