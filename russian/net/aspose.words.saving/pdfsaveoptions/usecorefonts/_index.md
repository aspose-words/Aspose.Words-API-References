---
title: PdfSaveOptions.UseCoreFonts
linktitle: UseCoreFonts
articleTitle: UseCoreFonts
second_title: Aspose.Words для .NET
description: PdfSaveOptions UseCoreFonts свойство. Получает или задает значение определяющее следует ли заменять шрифты TrueType Arial Times New Roman Courier New и символ базовыми шрифтами PDF Type 1 на С#.
type: docs
weight: 310
url: /ru/net/aspose.words.saving/pdfsaveoptions/usecorefonts/
---
## PdfSaveOptions.UseCoreFonts property

Получает или задает значение, определяющее, следует ли заменять шрифты TrueType Arial, Times New Roman, Courier New и символ базовыми шрифтами PDF Type 1.

```csharp
public bool UseCoreFonts { get; set; }
```

## Примечания

Значение по умолчанию:`ЛОЖЬ` . Когда это значение установлено на`истинный` Шрифты Arial, Times New Roman, Courier New и Symbol заменяются в PDF-документе соответствующим базовым шрифтом Type 1.

Базовые шрифты PDF или их параметры шрифта и подходящие замещающие шрифты должны быть доступны любому приложению просмотра PDF.

Этот параметр работает только для текста в кодировке ANSI (Windows-1252). Текст, отличный от ANSI, будет написан со встроенным шрифтом TrueType независимо от этой настройки.

Для соответствия PDF/A и PDF/UA необходимо встроить все шрифты.`ЛОЖЬ` значение будет использовано автоматически при сохранении в PDF/A и PDF/UA.

Базовые шрифты не поддерживаются при сохранении в формате PDF 2.0.`ЛОЖЬ` значение будет использовано автоматически при сохранении в PDF 2.0.

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

// Создаем объект «PdfSaveOptions», который мы можем передать методу «Save» документа.
// чтобы изменить способ преобразования этого метода в .PDF.
PdfSaveOptions options = new PdfSaveOptions();

// Установите для свойства UseCoreFonts значение «true», чтобы заменить некоторые шрифты,
// включая два шрифта в нашем документе и их эквиваленты PDF Type 1.
// Установите для свойства UseCoreFonts значение «false», чтобы не применять шрифты PDF Type 1.
options.UseCoreFonts = useCoreFonts;

doc.Save(ArtifactsDir + "PdfSaveOptions.EmbedCoreFonts.pdf", options);

if (useCoreFonts)
    Assert.That(3000, Is.AtLeast(new FileInfo(ArtifactsDir + "PdfSaveOptions.EmbedCoreFonts.pdf").Length));
else
    Assert.That(30000, Is.LessThan(new FileInfo(ArtifactsDir + "PdfSaveOptions.EmbedCoreFonts.pdf").Length));
```

### Смотрите также

* class [PdfSaveOptions](../)
* пространство имен [Aspose.Words.Saving](../../../aspose.words.saving/)
* сборка [Aspose.Words](../../../)
