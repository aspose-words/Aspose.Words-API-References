---
title: Style.Locked
linktitle: Locked
articleTitle: Locked
second_title: Aspose.Words för .NET
description: Upptäck egenskapen Style Locked, styr stillåsning för ökad designflexibilitet och konsekvens i dina projekt. Släpp lös din kreativitet idag!
type: docs
weight: 120
url: /sv/net/aspose.words/style/locked/
---
## Style.Locked property

Anger om den här stilen är låst.

```csharp
public bool Locked { get; set; }
```

## Exempel

Visar hur man låser stilen.

```csharp
Document doc = new Document();

Style styleHeading1 = doc.Styles[StyleIdentifier.Heading1];
if (!styleHeading1.Locked)
    styleHeading1.Locked = true;

doc.Save(ArtifactsDir + "Styles.LockStyle.docx");
```

### Se även

* class [Style](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
