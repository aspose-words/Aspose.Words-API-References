---
title: PageSetup.BorderAppliesTo
linktitle: BorderAppliesTo
articleTitle: BorderAppliesTo
second_title: Aspose.Words per .NET
description: Scopri come la proprietà PageSetup BorderAppliesTo migliora il layout del tuo documento controllando la stampa dei bordi della pagina, per un aspetto curato e professionale.
type: docs
weight: 30
url: /it/net/aspose.words/pagesetup/borderappliesto/
---
## PageSetup.BorderAppliesTo property

Specifica su quali pagine viene stampato il bordo della pagina.

```csharp
public PageBorderAppliesTo BorderAppliesTo { get; set; }
```

## Esempi

Mostra come creare un bordo con una larga fascia blu nella parte superiore della prima pagina.

```csharp
Document doc = new Document();

PageSetup pageSetup = doc.Sections[0].PageSetup;
pageSetup.BorderAlwaysInFront = false;
pageSetup.BorderDistanceFrom = PageBorderDistanceFrom.PageEdge;
pageSetup.BorderAppliesTo = PageBorderAppliesTo.FirstPage;

Border border = pageSetup.Borders[BorderType.Top];
border.LineStyle = LineStyle.Single;
border.LineWidth = 30;
border.Color = Color.Blue;
border.DistanceFromText = 0;

doc.Save(ArtifactsDir + "PageSetup.PageBorderProperties.docx");
```

### Guarda anche

* enum [PageBorderAppliesTo](../../pageborderappliesto/)
* class [PageSetup](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
