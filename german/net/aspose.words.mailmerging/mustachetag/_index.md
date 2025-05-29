---
title: MustacheTag Class
linktitle: MustacheTag
articleTitle: MustacheTag
second_title: Aspose.Words für .NET
description: Entdecken Sie die Klasse Aspose.Words.MailMerging.MustacheTag – handhaben Sie Mustache-Tags effizient für eine nahtlose Dokumentautomatisierung und verbesserte Serienbrieffunktion.
type: docs
weight: 4570
url: /de/net/aspose.words.mailmerging/mustachetag/
---
## MustacheTag class

Stellt das Tag „Schnurrbart“ dar.

```csharp
public class MustacheTag
```

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| [ReferenceOffset](../../aspose.words.mailmerging/mustachetag/referenceoffset/) { get; } | Ruft die nullbasierte Startposition des Tags vom Anfang des[`ReferenceRun`](./referencerun/) . |
| [ReferenceRun](../../aspose.words.mailmerging/mustachetag/referencerun/) { get; } | Ruft den Lauf ab, der den Anfang des Tags enthält. |
| [Text](../../aspose.words.mailmerging/mustachetag/text/) { get; } | Ruft den Text des Tags ab. |

## Beispiele

Zeigt, wie mit den Mustache-Tags gearbeitet wird.

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

### Siehe auch

* namensraum [Aspose.Words.MailMerging](../../aspose.words.mailmerging/)
* Montage [Aspose.Words](../../)
