---
title: PresetTexture Enum
linktitle: PresetTexture
articleTitle: PresetTexture
second_title: Aspose.Words para .NET
description: Descubra la enumeración Aspose.Words.Drawing.PresetTexture para mejorar sus formas con texturas personalizables para diseños de documentos impresionantes.
type: docs
weight: 1560
url: /es/net/aspose.words.drawing/presettexture/
---
## PresetTexture enumeration

Especifica la textura que se utilizará para rellenar una forma.

```csharp
public enum PresetTexture
```

### Valores

| Nombre | Valor | Descripción |
| --- | --- | --- |
| None | `-1` | Sin textura. |
| BlueTissuePaper | `1` | Textura de papel de seda azul. |
| Bouquet | `2` | Textura de ramo. |
| BrownMarble | `3` | Textura de mármol marrón. |
| Canvas | `4` | Textura de lienzo. |
| Cork | `5` | Textura de corcho. |
| Denim | `6` | Textura de mezclilla. |
| FishFossil | `7` | Textura de fósil de pez. |
| Granite | `8` | Textura de granito. |
| GreenMarble | `9` | Textura de mármol verde. |
| MediumWood | `10` | Textura de madera media. |
| Newsprint | `11` | Textura de papel de periódico. |
| Oak | `12` | Textura de roble. |
| PaperBag | `13` | Textura de bolsa de papel. |
| Papyrus | `14` | Textura de papiro. |
| Parchment | `15` | Textura de pergamino. |
| PinkTissuePaper | `16` | Textura de papel de seda rosa. |
| PurpleMesh | `17` | Textura de malla morada. |
| RecycledPaper | `18` | Textura de papel reciclado. |
| Sand | `19` | Textura de arena. |
| Stationery | `20` | Textura de papelería. |
| Walnut | `21` | Textura de nuez. |
| WaterDroplets | `22` | Textura de gotas de agua. |
| WhiteMarble | `23` | Textura de mármol blanco. |
| WovenMat | `24` | Textura de estera tejida. |

## Ejemplos

Muestra cómo establecer el formato del marcador.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Scatter, 432, 252);
Chart chart = shape.Chart;

//Eliminar serie generada por defecto.
chart.Series.Clear();
ChartSeries series = chart.Series.Add("AW Series 1", new[] { 0.7, 1.8, 2.6, 3.9 },
    new[] { 2.7, 3.2, 0.8, 1.7 });

// Establecer el formato del marcador.
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

### Ver también

* espacio de nombres [Aspose.Words.Drawing](../../aspose.words.drawing/)
* asamblea [Aspose.Words](../../)
