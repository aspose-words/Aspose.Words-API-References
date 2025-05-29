---
title: PdfSaveOptions.UseCoreFonts
linktitle: UseCoreFonts
articleTitle: UseCoreFonts
second_title: Aspose.Words для .NET
description: Оптимизируйте свои PDF-файлы с помощью PdfSaveOptions! Управляйте заменой шрифтов TrueType, таких как Arial и Times New Roman, чтобы улучшить качество документа.
type: docs
weight: 330
url: /ru/net/aspose.words.saving/pdfsaveoptions/usecorefonts/
---
## PdfSaveOptions.UseCoreFonts property

Возвращает или задает значение, определяющее, следует ли заменять шрифты TrueType Arial, Times New Roman, Courier New и Symbol основными шрифтами PDF Type 1.

```csharp
public bool UseCoreFonts { get; set; }
```

## Примечания

Значение по умолчанию:`ЛОЖЬ` . Когда это значение установлено на`истинный` Шрифты Arial, Times New Roman, Courier New и Symbol заменены в документе PDF соответствующим основным шрифтом Type 1.

Основные шрифты PDF или их метрики и подходящие заменяющие шрифты должны быть доступны для любого приложения просмотра PDF-файлов .

Эта настройка работает только для текста в кодировке ANSI (Windows-1252). Текст, не являющийся ANSI, будет записан со встроенным шрифтом TrueType независимо от этой настройки.

Для соответствия стандартам PDF/A и PDF/UA необходимо, чтобы все шрифты были встроены.`ЛОЖЬ` значение будет использовано автоматически при сохранении в PDF/A и PDF/UA.

Основные шрифты не поддерживаются при сохранении в формате PDF 2.0.`ЛОЖЬ` значение будет использовано автоматически при сохранении в PDF 2.0.

Эта опция имеет более высокий приоритет, чем[`FontEmbeddingMode`](../fontembeddingmode/) вариант.

## Примеры

Показывает, как включить/отключить замену шрифта PDF Type 1.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Name = "Arial";
builder.Writeln("Hello world!");
builder.Font.Name = "Courier New";
builder.Writeln("The quick brown fox jumps over the lazy dog.");

// Создаем объект "PdfSaveOptions", который можно передать методу "Save" документа
// чтобы изменить способ преобразования этим методом документа в .PDF.
PdfSaveOptions options = new PdfSaveOptions();
// Установите свойство «UseCoreFonts» в значение «true», чтобы заменить некоторые шрифты,
// включая два шрифта в наш документ с их эквивалентами PDF Type 1.
// Установите свойство «UseCoreFonts» в значение «false», чтобы не применять шрифты PDF Type 1.
options.UseCoreFonts = useCoreFonts;

doc.Save(ArtifactsDir + "PdfSaveOptions.EmbedCoreFonts.pdf", options);
```

### Смотрите также

* class [PdfSaveOptions](../)
* пространство имен [Aspose.Words.Saving](../../../aspose.words.saving/)
* сборка [Aspose.Words](../../../)
