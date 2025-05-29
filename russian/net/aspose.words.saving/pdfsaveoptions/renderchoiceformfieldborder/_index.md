---
title: PdfSaveOptions.RenderChoiceFormFieldBorder
linktitle: RenderChoiceFormFieldBorder
articleTitle: RenderChoiceFormFieldBorder
second_title: Aspose.Words для .NET
description: Узнайте, как свойство PdfSaveOptions RenderChoiceFormFieldBorder улучшает дизайн PDF-формы, управляя границами полей выбора для лучшего взаимодействия с пользователем.
type: docs
weight: 290
url: /ru/net/aspose.words.saving/pdfsaveoptions/renderchoiceformfieldborder/
---
## PdfSaveOptions.RenderChoiceFormFieldBorder property

Указывает, отображать ли границу поля формы выбора PDF.

```csharp
public bool RenderChoiceFormFieldBorder { get; set; }
```

## Примечания

Поля формы выбора PDF используются для экспорта элемента управления содержимым поля со списком SDT, элемента управления раскрывающимся списком SDT Content и устаревшего поля раскрывающегося списка формы, когда[`PreserveFormFields`](../preserveformfields/) опция включена.

Значение по умолчанию:`истинный`.

## Примеры

Показывает, как визуализировать границу поля формы выбора PDF.

```csharp
Document doc = new Document(MyDir + "Legacy drop-down.docx");

PdfSaveOptions saveOptions = new PdfSaveOptions();
saveOptions.PreserveFormFields = true;
saveOptions.RenderChoiceFormFieldBorder = true;

doc.Save(ArtifactsDir + "PdfSaveOptions.RenderChoiceFormFieldBorder.pdf", saveOptions);
```

### Смотрите также

* class [PdfSaveOptions](../)
* пространство имен [Aspose.Words.Saving](../../../aspose.words.saving/)
* сборка [Aspose.Words](../../../)
