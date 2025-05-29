---
title: WarningInfo.Source
linktitle: Source
articleTitle: Source
second_title: .NET için Aspose.Words
description: Uyarıların kaynağını ortaya çıkaran WarningInfo Source özelliğini keşfedin, böylece uygulamanızın güvenilirliğini ve kullanıcı deneyimini artırın.
type: docs
weight: 20
url: /tr/net/aspose.words/warninginfo/source/
---
## WarningInfo.Source property

Uyarının kaynağını döndürür.

```csharp
public WarningSource Source { get; }
```

## Örnekler

Uyarı kaynağıyla nasıl çalışılacağını gösterir.

```csharp
Document doc = new Document(MyDir + "Emphases markdown warning.docx");

WarningInfoCollection warnings = new WarningInfoCollection();
doc.WarningCallback = warnings;
doc.Save(ArtifactsDir + "DocumentBuilder.EmphasesWarningSourceMarkdown.md");

foreach (WarningInfo warningInfo in warnings)
{
    if (warningInfo.Source == WarningSource.Markdown)
        Assert.AreEqual("The (*, 0:11) cannot be properly written into Markdown.", warningInfo.Description);
}
```

### Ayrıca bakınız

* enum [WarningSource](../../warningsource/)
* class [WarningInfo](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
