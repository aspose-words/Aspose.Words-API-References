---
title: Font.AutoColor
linktitle: AutoColor
articleTitle: AutoColor
second_title: Aspose.Words для .NET
description: Font AutoColor свойство. Возвращает текущий рассчитанный цвет текста черный или белый который будет использоваться для автоматического цвета. Если цвет не авто то возвращаетсяColor  на С#.
type: docs
weight: 20
url: /ru/net/aspose.words/font/autocolor/
---
## Font.AutoColor property

Возвращает текущий рассчитанный цвет текста (черный или белый), который будет использоваться для «автоматического цвета». Если цвет не «авто», то возвращается[`Color`](../color/) .

```csharp
public Color AutoColor { get; }
```

## Примечания

Когда текст имеет «автоматический цвет», фактический цвет текста рассчитывается автоматически , чтобы его можно было прочитать на фоне цвета фона. Когда вы меняете цвет фона, , цвет текста в MS Word автоматически переключается на черный или белый, чтобы обеспечить максимальную разборчивость.

## Примеры

Показывает, как улучшить читаемость за счет автоматического выбора цвета текста в зависимости от яркости его фона.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Если объект Font выполнения не определяет цвет текста, он будет автоматически
// выбираем черный или белый цвет в зависимости от цвета фона.
Assert.AreEqual(Color.Empty.ToArgb(), builder.Font.Color.ToArgb());

// Цвет текста по умолчанию — черный. Если цвет фона темный, черный текст будет плохо видно.
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
