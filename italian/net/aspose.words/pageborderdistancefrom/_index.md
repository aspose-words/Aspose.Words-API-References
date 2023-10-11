---
title: Enum PageBorderDistanceFrom
second_title: Aspose.Words per .NET API Reference
description: Aspose.Words.PageBorderDistanceFrom enum. Specifica il posizionamento del bordo della pagina rispetto al margine della pagina.
type: docs
weight: 4350
url: /it/net/aspose.words/pageborderdistancefrom/
---
## PageBorderDistanceFrom enumeration

Specifica il posizionamento del bordo della pagina rispetto al margine della pagina.

```csharp
public enum PageBorderDistanceFrom
```

### I valori

| Nome | Valore | Descrizione |
| --- | --- | --- |
| Text | `0` | La posizione del bordo viene misurata dal margine della pagina. |
| PageEdge | `1` | La posizione del bordo viene misurata dal bordo della pagina. |

### Esempi

Mostra come creare un ampio bordo a fascia blu nella parte superiore della prima pagina.

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

* class [PageSetup](../pagesetup/)
* property [BorderDistanceFrom](../pagesetup/borderdistancefrom/)
* spazio dei nomi [Aspose.Words](../../aspose.words/)
* assemblea [Aspose.Words](../../)


