---
title: PresetTexture Enum
linktitle: PresetTexture
articleTitle: PresetTexture
second_title: Aspose.Words pour .NET
description: Découvrez l'énumération Aspose.Words.Drawing.PresetTexture pour améliorer vos formes avec des textures personnalisables pour des conceptions de documents époustouflantes.
type: docs
weight: 1560
url: /fr/net/aspose.words.drawing/presettexture/
---
## PresetTexture enumeration

Spécifie la texture à utiliser pour remplir une forme.

```csharp
public enum PresetTexture
```

### Valeurs

| Nom | Évaluer | La description |
| --- | --- | --- |
| None | `-1` | Aucune texture. |
| BlueTissuePaper | `1` | Texture de papier de soie bleu. |
| Bouquet | `2` | Texture du bouquet. |
| BrownMarble | `3` | Texture de marbre brun. |
| Canvas | `4` | Texture de la toile. |
| Cork | `5` | Texture liège. |
| Denim | `6` | Texture denim. |
| FishFossil | `7` | Texture de fossile de poisson. |
| Granite | `8` | Texture de granit. |
| GreenMarble | `9` | Texture de marbre vert. |
| MediumWood | `10` | Texture bois moyenne. |
| Newsprint | `11` | Texture de papier journal. |
| Oak | `12` | Texture chêne. |
| PaperBag | `13` | Texture de sac en papier. |
| Papyrus | `14` | Texture de papyrus. |
| Parchment | `15` | Texture de parchemin. |
| PinkTissuePaper | `16` | Texture de papier de soie rose. |
| PurpleMesh | `17` | Texture de maille violette. |
| RecycledPaper | `18` | Texture de papier recyclé. |
| Sand | `19` | Texture de sable. |
| Stationery | `20` | Texture de papeterie. |
| Walnut | `21` | Texture de noix. |
| WaterDroplets | `22` | Texture de gouttes d'eau. |
| WhiteMarble | `23` | Texture de marbre blanc. |
| WovenMat | `24` | Texture de tapis tissé. |

## Exemples

Montrez comment définir la mise en forme des marqueurs.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Scatter, 432, 252);
Chart chart = shape.Chart;

// Supprimer la série générée par défaut.
chart.Series.Clear();
ChartSeries series = chart.Series.Add("AW Series 1", new[] { 0.7, 1.8, 2.6, 3.9 },
    new[] { 2.7, 3.2, 0.8, 1.7 });

// Définir le formatage du marqueur.
series.Marker.Size = 40;
series.Marker.Symbol = MarkerSymbol.Square;
ChartDataPointCollection dataPoints = series.DataPoints;
dataPoints[0].Marker.Format.Fill.PresetTextured(PresetTexture.Denim);
dataPoints[0].Marker.Format.Stroke.ForeColor = Color.Yellow;
dataPoints[0].Marker.Format.Stroke.BackColor = Color.Red;
dataPoints[1].Marker.Format.Fill.PresetTextured(PresetTexture.WaterDroplets);
dataPoints[1].Marker.Format.Stroke.ForeColor = Color.Yellow;
dataPoints[1].Marker.Format.Stroke.Visible = false;
dataPoints[2].Marker.Format.Fill.PresetTextured(PresetTexture.GreenMarble);
dataPoints[2].Marker.Format.Stroke.ForeColor = Color.Yellow;
dataPoints[3].Marker.Format.Fill.PresetTextured(PresetTexture.Oak);
dataPoints[3].Marker.Format.Stroke.ForeColor = Color.Yellow;
dataPoints[3].Marker.Format.Stroke.Transparency = 0.5;

doc.Save(ArtifactsDir + "Charts.MarkerFormatting.docx");
```

### Voir également

* espace de noms [Aspose.Words.Drawing](../../aspose.words.drawing/)
* Assemblée [Aspose.Words](../../)
