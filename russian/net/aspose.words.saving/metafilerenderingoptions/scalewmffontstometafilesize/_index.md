---
title: MetafileRenderingOptions.ScaleWmfFontsToMetafileSize
second_title: Справочник по API Aspose.Words для .NET
description: MetafileRenderingOptions свойство. Получает или задает значение определяющее следует ли масштабировать шрифты в метафайле WMF в соответствии с размером метафайла на странице.
type: docs
weight: 50
url: /ru/net/aspose.words.saving/metafilerenderingoptions/scalewmffontstometafilesize/
---
## MetafileRenderingOptions.ScaleWmfFontsToMetafileSize property

Получает или задает значение, определяющее, следует ли масштабировать шрифты в метафайле WMF в соответствии с размером метафайла на странице.

```csharp
public bool ScaleWmfFontsToMetafileSize { get; set; }
```

### Примечания

Когда метафайлы WMF отображаются в MS Word, шрифты могут масштабироваться в соответствии с фактическим размером метафайла на странице.

Когда это значение установлено на`истинный`, Aspose.Words эмулирует масштабирование шрифта в соответствии с размером метафайла на странице.

Когда это значение установлено на`ЛОЖЬ`, Aspose.Words отображает шрифты, поскольку метафайл отображается в размере по умолчанию.

Этот параметр используется только тогда, когда метафайл визуализируется как векторная графика.

Значение по умолчанию`истинный`.

### Примеры

Показывает, как масштабировать шрифты WMF в соответствии с размером метафайла на странице.

```csharp
Document doc = new Document(MyDir + "WMF with text.docx");

// Создаем объект "PdfSaveOptions", который мы можем передать в метод "Сохранить" документа
// для изменения того, как этот метод преобразует документ в .PDF.
PdfSaveOptions saveOptions = new PdfSaveOptions();

// Установите для свойства "ScaleWmfFontsToMetafileSize" значение "true", чтобы масштабировать шрифты
// которые форматируют текст в изображениях WMF в соответствии с размером метафайла на странице.
// Установите для свойства "ScaleWmfFontsToMetafileSize" значение "false", чтобы
// сохранить масштаб этих шрифтов по умолчанию.
saveOptions.MetafileRenderingOptions.ScaleWmfFontsToMetafileSize = scaleWmfFonts;

doc.Save(ArtifactsDir + "PdfSaveOptions.FontsScaledToMetafileSize.pdf", saveOptions);
```

### Смотрите также

* class [MetafileRenderingOptions](../)
* пространство имен [Aspose.Words.Saving](../../metafilerenderingoptions/)
* сборка [Aspose.Words](../../../)


