---
title: ComparerContext Class
linktitle: ComparerContext
articleTitle: ComparerContext
second_title: Aspose.Words para .NET
description: Descubra la clase Aspose.Words LowCode ComparerContext para una comparación eficiente de documentos, mejorando su flujo de trabajo con una integración perfecta y funciones potentes.
type: docs
weight: 4220
url: /es/net/aspose.words.lowcode/comparercontext/
---
## ComparerContext class

Contexto comparador de documentos

```csharp
public class ComparerContext : ProcessorContext
```

## Constructores

| Nombre | Descripción |
| --- | --- |
| [ComparerContext](comparercontext/)() | Constructor predeterminado |

## Propiedades

| Nombre | Descripción |
| --- | --- |
| [AcceptRevisions](../../aspose.words.lowcode/comparercontext/acceptrevisions/) { get; set; } | Indica si se deben aceptar revisiones en los documentos antes de compararlos. Si los documentos comparados contienen revisiones y este indicador se establece en falso, el procesador rechazará las revisiones. El valor predeterminado es`verdadero` . |
| [Author](../../aspose.words.lowcode/comparercontext/author/) { get; set; } | El autor que se asignará a las revisiones creadas durante la comparación de documentos. |
| [CompareOptions](../../aspose.words.lowcode/comparercontext/compareoptions/) { get; } | Opciones utilizadas al comparar documentos. |
| [DateTime](../../aspose.words.lowcode/comparercontext/datetime/) { get; set; } | La fecha y hora asignadas a las revisiones creadas durante la comparación de documentos. |
| [FontSettings](../../aspose.words.lowcode/processorcontext/fontsettings/) { get; set; } | Configuración de fuentes utilizada por el procesador. |
| [LayoutOptions](../../aspose.words.lowcode/processorcontext/layoutoptions/) { get; } | Opciones de diseño de documento utilizadas por el procesador. |
| [WarningCallback](../../aspose.words.lowcode/processorcontext/warningcallback/) { get; set; } | Devolución de llamada de advertencia utilizada por el procesador. |

## Ejemplos

Muestra cómo comparar documentos de forma sencilla utilizando el contexto.

```csharp
//Hay varias formas de comparar documentos:
string firstDoc = MyDir + "Table column bookmarks.docx";
string secondDoc = MyDir + "Table column bookmarks.doc";

ComparerContext comparerContext = new ComparerContext();
comparerContext.CompareOptions.IgnoreCaseChanges = true;
comparerContext.Author = "Author";
comparerContext.DateTime = new DateTime();

Comparer.Create(comparerContext)
    .From(firstDoc)
    .From(secondDoc)
    .To(ArtifactsDir + "LowCode.CompareContextDocuments.docx")
    .Execute();
```

Muestra cómo comparar documentos de la secuencia utilizando el contexto.

```csharp
// Hay varias formas de comparar documentos de la secuencia:
using (FileStream firstStreamIn = new FileStream(MyDir + "Table column bookmarks.docx", FileMode.Open, FileAccess.Read))
{
    using (FileStream secondStreamIn = new FileStream(MyDir + "Table column bookmarks.doc", FileMode.Open, FileAccess.Read))
    {
        ComparerContext comparerContext = new ComparerContext();
        comparerContext.CompareOptions.IgnoreCaseChanges = true;
        comparerContext.Author = "Author";
        comparerContext.DateTime = new DateTime();

        using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.CompareContextStreamDocuments.docx", FileMode.Create, FileAccess.ReadWrite))
            Comparer.Create(comparerContext)
                .From(firstStreamIn)
                .From(secondStreamIn)
                .To(streamOut, SaveFormat.Docx)
                .Execute();
    }
}
```

### Ver también

* class [ProcessorContext](../processorcontext/)
* espacio de nombres [Aspose.Words.LowCode](../../aspose.words.lowcode/)
* asamblea [Aspose.Words](../../)
