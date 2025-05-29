---
title: Style.Locked
linktitle: Locked
articleTitle: Locked
second_title: .NET için Aspose.Words
description: Style Locked özelliğini keşfedin, projelerinizde gelişmiş tasarım esnekliği ve tutarlılık için stil kilitlemeyi kontrol edin. Bugün yaratıcılığınızın kilidini açın!
type: docs
weight: 120
url: /tr/net/aspose.words/style/locked/
---
## Style.Locked property

Bu stilin kilitli olup olmadığını belirtir.

```csharp
public bool Locked { get; set; }
```

## Örnekler

Stilin nasıl kilitleneceğini gösterir.

```csharp
Document doc = new Document();

Style styleHeading1 = doc.Styles[StyleIdentifier.Heading1];
if (!styleHeading1.Locked)
    styleHeading1.Locked = true;

doc.Save(ArtifactsDir + "Styles.LockStyle.docx");
```

### Ayrıca bakınız

* class [Style](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
