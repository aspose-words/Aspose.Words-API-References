---
title: PresetTexture Enum
linktitle: PresetTexture
articleTitle: PresetTexture
second_title: Aspose.Words для .NET
description: Откройте для себя перечисление Aspose.Words.Drawing.PresetTexture, чтобы улучшить свои фигуры с помощью настраиваемых текстур для создания потрясающих дизайнов документов.
type: docs
weight: 1560
url: /ru/net/aspose.words.drawing/presettexture/
---
## PresetTexture enumeration

Указывает текстуру, которая будет использоваться для заполнения формы.

```csharp
public enum PresetTexture
```

### Ценности

| Имя | Ценность | Описание |
| --- | --- | --- |
| None | `-1` | Нет текстуры. |
| BlueTissuePaper | `1` | Текстура синей папиросной бумаги. |
| Bouquet | `2` | Текстура букета. |
| BrownMarble | `3` | Текстура коричневого мрамора. |
| Canvas | `4` | Текстура холста. |
| Cork | `5` | Текстура пробки. |
| Denim | `6` | Текстура денима. |
| FishFossil | `7` | Текстура окаменелости рыбы. |
| Granite | `8` | Текстура гранита. |
| GreenMarble | `9` | Текстура зеленого мрамора. |
| MediumWood | `10` | Средняя текстура дерева. |
| Newsprint | `11` | Текстура газетной бумаги. |
| Oak | `12` | Текстура дуба. |
| PaperBag | `13` | Текстура бумажного пакета. |
| Papyrus | `14` | Текстура папируса. |
| Parchment | `15` | Текстура пергамента. |
| PinkTissuePaper | `16` | Текстура розовой папиросной бумаги. |
| PurpleMesh | `17` | Фиолетовая сетчатая текстура. |
| RecycledPaper | `18` | Текстура переработанной бумаги. |
| Sand | `19` | Текстура песка. |
| Stationery | `20` | Текстура канцелярских товаров. |
| Walnut | `21` | Текстура грецкого ореха. |
| WaterDroplets | `22` | Текстура капель воды. |
| WhiteMarble | `23` | Текстура белого мрамора. |
| WovenMat | `24` | Текстура плетеного коврика. |

## Примеры

Покажите, как настроить форматирование маркера.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Scatter, 432, 252);
Chart chart = shape.Chart;

// Удалить сгенерированную по умолчанию серию.
chart.Series.Clear();
ChartSeries series = chart.Series.Add("AW Series 1", new[] { 0.7, 1.8, 2.6, 3.9 },
    new[] { 2.7, 3.2, 0.8, 1.7 });

// Установить форматирование маркера.
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

### Смотрите также

* пространство имен [Aspose.Words.Drawing](../../aspose.words.drawing/)
* сборка [Aspose.Words](../../)
