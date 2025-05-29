---
title: PresetTexture Enum
linktitle: PresetTexture
articleTitle: PresetTexture
second_title: Aspose.Words per .NET
description: Scopri l'enum Aspose.Words.Drawing.PresetTexture per migliorare le tue forme con texture personalizzabili per creare documenti dalla progettazione straordinaria.
type: docs
weight: 1560
url: /it/net/aspose.words.drawing/presettexture/
---
## PresetTexture enumeration

Specifica la texture da utilizzare per riempire una forma.

```csharp
public enum PresetTexture
```

### I valori

| Nome | Valore | Descrizione |
| --- | --- | --- |
| None | `-1` | Nessuna trama. |
| BlueTissuePaper | `1` | Texture di carta velina blu. |
| Bouquet | `2` | Trama del bouquet. |
| BrownMarble | `3` | Texture marmo marrone. |
| Canvas | `4` | Trama della tela. |
| Cork | `5` | Texture di sughero. |
| Denim | `6` | Trama denim. |
| FishFossil | `7` | Texture di fossili di pesce. |
| Granite | `8` | Texture granito. |
| GreenMarble | `9` | Texture di marmo verde. |
| MediumWood | `10` | Texture di legno medio. |
| Newsprint | `11` | Texture di carta di giornale. |
| Oak | `12` | Texture rovere. |
| PaperBag | `13` | Texture di sacchetto di carta. |
| Papyrus | `14` | Trama di papiro. |
| Parchment | `15` | Texture pergamena. |
| PinkTissuePaper | `16` | Texture di carta velina rosa. |
| PurpleMesh | `17` | Trama a rete viola. |
| RecycledPaper | `18` | Texture di carta riciclata. |
| Sand | `19` | Texture sabbia. |
| Stationery | `20` | Texture di cancelleria. |
| Walnut | `21` | Texture noce. |
| WaterDroplets | `22` | Texture di gocce d'acqua. |
| WhiteMarble | `23` | Texture di marmo bianco. |
| WovenMat | `24` | Trama di stuoia intrecciata. |

## Esempi

Mostra come impostare la formattazione dei marcatori.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Scatter, 432, 252);
Chart chart = shape.Chart;

// Elimina la serie generata di default.
chart.Series.Clear();
ChartSeries series = chart.Series.Add("AW Series 1", new[] { 0.7, 1.8, 2.6, 3.9 },
    new[] { 2.7, 3.2, 0.8, 1.7 });

// Imposta la formattazione del marcatore.
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

### Guarda anche

* spazio dei nomi [Aspose.Words.Drawing](../../aspose.words.drawing/)
* assemblea [Aspose.Words](../../)
