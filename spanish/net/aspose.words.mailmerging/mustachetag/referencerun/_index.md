---
title: MustacheTag.ReferenceRun
second_title: Referencia de API de Aspose.Words para .NET
description: MustacheTag propiedad. Obtiene la ejecución que contiene el comienzo de la etiqueta.
type: docs
weight: 20
url: /es/net/aspose.words.mailmerging/mustachetag/referencerun/
---
## MustacheTag.ReferenceRun property

Obtiene la ejecución que contiene el comienzo de la etiqueta.

```csharp
public Run ReferenceRun { get; }
```

### Ejemplos

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
* espacio de nombres [Aspose.Words.MailMerging](../../mustachetag/)
* asamblea [Aspose.Words](../../../)


