---
title: PageSetup.BorderDistanceFrom
linktitle: BorderDistanceFrom
articleTitle: BorderDistanceFrom
second_title: Aspose.Words per .NET
description: Scopri la proprietà BorderDistanceFrom di PageSetup per controllare le misure dei bordi della pagina e ottenere una formattazione precisa dei documenti. Migliora il tuo layout oggi stesso!
type: docs
weight: 40
url: /it/net/aspose.words/pagesetup/borderdistancefrom/
---
## PageSetup.BorderDistanceFrom property

Ottiene o imposta un valore che indica se il bordo della pagina specificato viene misurato dal bordo della pagina o dal testo che la circonda.

```csharp
public PageBorderDistanceFrom BorderDistanceFrom { get; set; }
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

* enum [PageBorderDistanceFrom](../../pageborderdistancefrom/)
* class [PageSetup](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
