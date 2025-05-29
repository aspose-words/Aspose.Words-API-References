---
title: MustacheTag.Text
linktitle: Text
articleTitle: Text
second_title: Aspose.Words für .NET
description: Entdecken Sie die MustacheTag-Texteigenschaft, um Tag-Text mühelos abzurufen und zu verwenden, um die Datenverarbeitung zu verbessern und eine nahtlose Integration zu ermöglichen.
type: docs
weight: 30
url: /de/net/aspose.words.mailmerging/mustachetag/text/
---
## MustacheTag.Text property

Ruft den Text des Tags ab.

```csharp
public string Text { get; }
```

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

* class [MustacheTag](../)
* namensraum [Aspose.Words.MailMerging](../../../aspose.words.mailmerging/)
* Montage [Aspose.Words](../../../)
