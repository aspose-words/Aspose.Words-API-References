---
title: Font.AutoColor
linktitle: AutoColor
articleTitle: AutoColor
second_title: Aspose.Words для .NET
description: Откройте для себя свойство Font AutoColor, получите текущий цвет текста (черный или белый) для автоматической настройки цвета. Оптимизируйте свой дизайн без усилий!
type: docs
weight: 20
url: /ru/net/aspose.words/font/autocolor/
---
## Font.AutoColor property

Возвращает текущий вычисленный цвет текста (черный или белый), который будет использоваться для «автоматического цвета». Если цвет не равен «автоматическому», то возвращается[`Color`](../color/) .

```csharp
public Color AutoColor { get; }
```

## Примечания

Когда текст имеет «автоматический цвет», фактический цвет текста вычисляется автоматически так, чтобы он был читаемым на фоне цвета. При изменении цвета фона цвет текста автоматически изменится на черный или белый в MS Word, чтобы максимизировать читаемость.

## Примеры

Показывает, как улучшить читаемость, автоматически выбирая цвет текста в зависимости от яркости его фона.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Если объект Font не указывает цвет текста, он будет автоматически
// выберите черный или белый цвет в зависимости от цвета фона.
Assert.AreEqual(Color.Empty.ToArgb(), builder.Font.Color.ToArgb());

// Цвет текста по умолчанию — черный. Если цвет фона темный, черный текст будет трудно увидеть.
// Чтобы решить эту проблему, свойство AutoColor отобразит этот текст белым цветом.
builder.Font.Shading.BackgroundPatternColor = Color.DarkBlue;

builder.Writeln("The text color automatically chosen for this run is white.");

Assert.AreEqual(Color.White.ToArgb(), doc.FirstSection.Body.Paragraphs[0].Runs[0].Font.AutoColor.ToArgb());

// Если мы изменим фон на светлый цвет, черный будет более
// подходящий цвет текста, отличный от белого, чтобы автоматический цвет отображал его черным.
builder.Font.Shading.BackgroundPatternColor = Color.LightBlue;

builder.Writeln("The text color automatically chosen for this run is black.");

Assert.AreEqual(Color.Black.ToArgb(), doc.FirstSection.Body.Paragraphs[1].Runs[0].Font.AutoColor.ToArgb());

doc.Save(ArtifactsDir + "Font.SetFontAutoColor.docx");
```

### Смотрите также

* class [Font](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
