---
title: MustacheTag Class
linktitle: MustacheTag
articleTitle: MustacheTag
second_title: Aspose.Words para .NET
description: Descubra la clase Aspose.Words.MailMerging.MustacheTag: gestione de forma eficiente las etiquetas Mustache para lograr una automatización perfecta de documentos y una mejor combinación de correo.
type: docs
weight: 4570
url: /es/net/aspose.words.mailmerging/mustachetag/
---
## MustacheTag class

Representa la etiqueta "bigote".

```csharp
public class MustacheTag
```

## Propiedades

| Nombre | Descripción |
| --- | --- |
| [ReferenceOffset](../../aspose.words.mailmerging/mustachetag/referenceoffset/) { get; } | Obtiene la posición inicial basada en cero de la etiqueta desde el inicio de la[`ReferenceRun`](./referencerun/) . |
| [ReferenceRun](../../aspose.words.mailmerging/mustachetag/referencerun/) { get; } | Obtiene la ejecución que contiene el comienzo de la etiqueta. |
| [Text](../../aspose.words.mailmerging/mustachetag/text/) { get; } | Obtiene el texto de la etiqueta. |

## Ejemplos

Muestra cómo trabajar con las etiquetas de bigote.

```csharp
Document document = new Document(MyDir + "Mail merge mustache tags.docx");
document.MailMerge.UseNonMergeFields = true;

MailMergeRegionInfo hierarchy = document.MailMerge.GetRegionsHierarchy();

foreach (MustacheTag mustacheTag in hierarchy.MustacheTags)
{
    Console.WriteLine(mustacheTag.Text);
    Console.WriteLine(mustacheTag.ReferenceOffset);
    Console.WriteLine(mustacheTag.ReferenceRun);
}

foreach (MailMergeRegionInfo region in hierarchy.Regions)
{
    Console.WriteLine(region.StartMustacheTag.Text);
    Console.WriteLine(region.EndMustacheTag.Text);
}
```

### Ver también

* espacio de nombres [Aspose.Words.MailMerging](../../aspose.words.mailmerging/)
* asamblea [Aspose.Words](../../)
