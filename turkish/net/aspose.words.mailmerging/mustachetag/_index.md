---
title: MustacheTag Class
linktitle: MustacheTag
articleTitle: MustacheTag
second_title: .NET için Aspose.Words
description: Aspose.Words.MailMerging.MustacheTag sınıfını keşfedin; sorunsuz belge otomasyonu ve gelişmiş e-posta birleştirme için bıyık etiketlerini verimli bir şekilde işleyin.
type: docs
weight: 4570
url: /tr/net/aspose.words.mailmerging/mustachetag/
---
## MustacheTag class

"bıyık" etiketini temsil eder.

```csharp
public class MustacheTag
```

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [ReferenceOffset](../../aspose.words.mailmerging/mustachetag/referenceoffset/) { get; } | Etiketin sıfır tabanlı başlangıç konumunu, etiketin başlangıcından itibaren alır.[`ReferenceRun`](./referencerun/) . |
| [ReferenceRun](../../aspose.words.mailmerging/mustachetag/referencerun/) { get; } | Etiketin başlangıcını içeren çalışmayı alır. |
| [Text](../../aspose.words.mailmerging/mustachetag/text/) { get; } | Etiketin metnini alır. |

## Örnekler

Bıyık etiketlerinin nasıl kullanılacağını gösterir.

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

### Ayrıca bakınız

* ad alanı [Aspose.Words.MailMerging](../../aspose.words.mailmerging/)
* toplantı [Aspose.Words](../../)
