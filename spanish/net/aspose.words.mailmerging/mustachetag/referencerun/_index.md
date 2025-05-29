---
title: MustacheTag.ReferenceRun
linktitle: ReferenceRun
articleTitle: ReferenceRun
second_title: Aspose.Words para .NET
description: Descubre MustacheTag ReferenceRun. Accede a la ejecución que marca el inicio de tu etiqueta para una gestión de datos fluida y un rendimiento mejorado.
type: docs
weight: 20
url: /es/net/aspose.words.mailmerging/mustachetag/referencerun/
---
## MustacheTag.ReferenceRun property

Obtiene la ejecución que contiene el comienzo de la etiqueta.

```csharp
public Run ReferenceRun { get; }
```

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

* class [Run](../../../aspose.words/run/)
* class [MustacheTag](../)
* espacio de nombres [Aspose.Words.MailMerging](../../../aspose.words.mailmerging/)
* asamblea [Aspose.Words](../../../)
