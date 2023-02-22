---
title: SvgSaveOptions.ShowPageBorder
second_title: Справочник по API Aspose.Words для .NET
description: SvgSaveOptions свойство. Управляет добавлением рамки к контуру страницы. Значение по умолчаниюистинный .
type: docs
weight: 80
url: /ru/net/aspose.words.saving/svgsaveoptions/showpageborder/
---
## SvgSaveOptions.ShowPageBorder property

Управляет добавлением рамки к контуру страницы. Значение по умолчанию:`истинный` .

```csharp
public bool ShowPageBorder { get; set; }
```

### Примеры

Показывает, как имитировать свойства изображений при преобразовании документа .docx в .svg.

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
* пространство имен [Aspose.Words.Saving](../../svgsaveoptions/)
* сборка [Aspose.Words](../../../)


