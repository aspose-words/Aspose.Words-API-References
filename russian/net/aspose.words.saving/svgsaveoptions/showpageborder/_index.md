---
title: SvgSaveOptions.ShowPageBorder
linktitle: ShowPageBorder
articleTitle: ShowPageBorder
second_title: Aspose.Words для .NET
description: Откройте для себя свойство SvgSaveOptions ShowPageBorder, чтобы настроить контур страницы. Управляйте границами без усилий — настройка по умолчанию — true для простоты использования!
type: docs
weight: 110
url: /ru/net/aspose.words.saving/svgsaveoptions/showpageborder/
---
## SvgSaveOptions.ShowPageBorder property

Управляет добавлением границы к контуру страницы. Значение по умолчанию:`истинный` .

```csharp
public bool ShowPageBorder { get; set; }
```

## Примеры

Показывает, как имитировать свойства изображений при конвертации документа .docx в .svg.

```csharp
Document doc = new Document(MyDir + "Document.docx");

// Настройте объект SvgSaveOptions для сохранения без границ страницы или выбираемого текста.
SvgSaveOptions options = new SvgSaveOptions
{
    FitToViewPort = true,
    ShowPageBorder = false,
    TextOutputMode = SvgTextOutputMode.UsePlacedGlyphs
};

doc.Save(ArtifactsDir + "SvgSaveOptions.SaveLikeImage.svg", options);
```

### Смотрите также

* class [SvgSaveOptions](../)
* пространство имен [Aspose.Words.Saving](../../../aspose.words.saving/)
* сборка [Aspose.Words](../../../)
