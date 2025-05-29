---
title: TextWatermarkOptions.IsSemitrasparent
linktitle: IsSemitrasparent
articleTitle: IsSemitrasparent
second_title: Aspose.Words для .NET
description: Откройте для себя свойство TextWatermarkOptions IsSemitransparent — легко контролируйте непрозрачность водяного знака. Улучшите свои проекты с помощью настраиваемых параметров прозрачности!
type: docs
weight: 50
url: /ru/net/aspose.words/textwatermarkoptions/issemitrasparent/
---
## TextWatermarkOptions.IsSemitrasparent property

Возвращает или задает логическое значение, которое отвечает за непрозрачность водяного знака. Значение по умолчанию:`истинный` .

```csharp
public bool IsSemitrasparent { get; set; }
```

## Примеры

Показывает, как создать текстовый водяной знак.

```csharp
Document doc = new Document();

// Добавить простой текстовый водяной знак.
doc.Watermark.SetText("Aspose Watermark");

// Если мы хотим изменить форматирование текста, используя его как водяной знак,
// мы можем сделать это, передав объект TextWatermarkOptions при создании водяного знака.
TextWatermarkOptions textWatermarkOptions = new TextWatermarkOptions();
textWatermarkOptions.FontFamily = "Arial";
textWatermarkOptions.FontSize = 36;
textWatermarkOptions.Color = Color.Black;
textWatermarkOptions.Layout = WatermarkLayout.Diagonal;
textWatermarkOptions.IsSemitrasparent = false;

doc.Watermark.SetText("Aspose Watermark", textWatermarkOptions);

doc.Save(ArtifactsDir + "Document.TextWatermark.docx");

// Мы можем удалить водяной знак из документа следующим образом.
if (doc.Watermark.Type == WatermarkType.Text)
    doc.Watermark.Remove();
```

### Смотрите также

* class [TextWatermarkOptions](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
