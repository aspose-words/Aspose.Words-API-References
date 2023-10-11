---
title: MustacheTag.ReferenceOffset
second_title: Aspose.Words für .NET-API-Referenz
description: MustacheTag eigendom. Ruft die nullbasierte Startposition des Tags ab dem Anfang abReferenceRun .
type: docs
weight: 10
url: /de/net/aspose.words.mailmerging/mustachetag/referenceoffset/
---
## MustacheTag.ReferenceOffset property

Ruft die nullbasierte Startposition des Tags ab dem Anfang ab[`ReferenceRun`](../referencerun/) .

```csharp
public int ReferenceOffset { get; }
```

### Beispiele

Zeigt, wie mit den Moustache-Tags gearbeitet wird.

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

* class [MustacheTag](../)
* namensraum [Aspose.Words.MailMerging](../../mustachetag/)
* Montage [Aspose.Words](../../../)


