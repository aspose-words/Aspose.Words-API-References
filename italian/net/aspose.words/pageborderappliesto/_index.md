---
title: PageBorderAppliesTo Enum
linktitle: PageBorderAppliesTo
articleTitle: PageBorderAppliesTo
second_title: Aspose.Words per .NET
description: Aspose.Words.PageBorderAppliesTo enum. Specifica su quali pagine viene stampato il bordo della pagina in C#.
type: docs
weight: 4340
url: /it/net/aspose.words/pageborderappliesto/
---
## PageBorderAppliesTo enumeration

Specifica su quali pagine viene stampato il bordo della pagina.

```csharp
public enum PageBorderAppliesTo
```

### I valori

| Nome | Valore | Descrizione |
| --- | --- | --- |
| AllPages | `0` | Il bordo della pagina viene mostrato su tutte le pagine della sezione. |
| FirstPage | `1` | Il bordo della pagina viene mostrato solo sulla prima pagina della sezione. |
| OtherPages | `2` | Il bordo della pagina viene visualizzato su tutte le pagine tranne la prima pagina della sezione. |

## Esempi

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
* property [BorderAppliesTo](../pagesetup/borderappliesto/)
* spazio dei nomi [Aspose.Words](../../aspose.words/)
* assemblea [Aspose.Words](../../)
