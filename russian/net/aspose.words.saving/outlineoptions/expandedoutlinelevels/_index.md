---
title: OutlineOptions.ExpandedOutlineLevels
linktitle: ExpandedOutlineLevels
articleTitle: ExpandedOutlineLevels
second_title: Aspose.Words для .NET
description: Откройте для себя свойство ExpandedOutlineLevels в OutlineOptions, позволяющее настраивать видимость структуры документа для улучшения навигации и удобства пользователя.
type: docs
weight: 60
url: /ru/net/aspose.words.saving/outlineoptions/expandedoutlinelevels/
---
## OutlineOptions.ExpandedOutlineLevels property

Указывает, сколько уровней в структуре документа будет отображаться развернутым при просмотре файла.

```csharp
public int ExpandedOutlineLevels { get; set; }
```

## Примечания

Обратите внимание, что эти параметры не будут работать при сохранении в формате XPS.

Укажите 0, и структура документа будет свернута; укажите 1, и элементы первого уровня items в структуре будут развернуты и т. д.

По умолчанию — 0. Допустимый диапазон — от 0 до 9.

## Примеры

Показывает, как преобразовать весь документ в PDF с тремя уровнями в структуре документа.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Вставьте заголовки уровней с 1 по 5.
builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading1;

Assert.True(builder.ParagraphFormat.IsHeading);

builder.Writeln("Heading 1");

builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading2;

builder.Writeln("Heading 1.1");
builder.Writeln("Heading 1.2");

builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading3;

builder.Writeln("Heading 1.2.1");
builder.Writeln("Heading 1.2.2");

builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading4;

builder.Writeln("Heading 1.2.2.1");
builder.Writeln("Heading 1.2.2.2");

builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading5;

builder.Writeln("Heading 1.2.2.2.1");
builder.Writeln("Heading 1.2.2.2.2");

// Создаем объект "PdfSaveOptions", который можно передать методу "Save" документа
// чтобы изменить способ преобразования этим методом документа в .PDF.
PdfSaveOptions options = new PdfSaveOptions();

// Выходной PDF-документ будет содержать структуру, представляющую собой оглавление, в котором перечислены заголовки в тексте документа.
// Нажатие на запись в этой схеме перенесет нас к местоположению соответствующего заголовка.
// Установите свойство "HeadingsOutlineLevels" на "4", чтобы исключить из структуры все заголовки, уровни которых выше 4.
options.OutlineOptions.HeadingsOutlineLevels = 4;

// Если запись структуры имеет последующие записи более высокого уровня между собой и следующей записью того же или более низкого уровня,
// слева от записи появится стрелка. Эта запись является «владельцем» нескольких таких «подзаписей».
// В нашем документе записи структуры из 5-го уровня заголовка являются подзаписями второй записи структуры 4-го уровня,
// записи 4-го и 5-го уровня заголовка являются подзаголовками второй записи 3-го уровня и т. д.
// В схеме мы можем щелкнуть стрелку записи «владелец», чтобы свернуть/развернуть все ее подзаписи.
// Установите свойство "ExpandedOutlineLevels" на "2", чтобы автоматически развернуть все заголовки уровня 2 и более низких записей структуры
// и сворачиваем все записи уровня 3 и выше при открытии документа.
options.OutlineOptions.ExpandedOutlineLevels = 2;

doc.Save(ArtifactsDir + "PdfSaveOptions.ExpandedOutlineLevels.pdf", options);
```

### Смотрите также

* class [OutlineOptions](../)
* пространство имен [Aspose.Words.Saving](../../../aspose.words.saving/)
* сборка [Aspose.Words](../../../)
