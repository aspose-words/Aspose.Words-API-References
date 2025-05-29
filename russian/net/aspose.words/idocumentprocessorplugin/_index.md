---
title: IDocumentProcessorPlugin Interface
linktitle: IDocumentProcessorPlugin
articleTitle: IDocumentProcessorPlugin
second_title: Aspose.Words для .NET
description: Откройте для себя интерфейс Aspose.Words IDocumentProcessorPlugin, который улучшит обработку документов с помощью мощных внешних плагинов для бесшовной интеграции.
type: docs
weight: 3610
url: /ru/net/aspose.words/idocumentprocessorplugin/
---
## IDocumentProcessorPlugin interface

Определяет интерфейс для внешнего плагина процессора документов.

```csharp
public interface IDocumentProcessorPlugin
```

## Методы

| Имя | Описание |
| --- | --- |
| [Append](../../aspose.words/idocumentprocessorplugin/append/)(*Stream, [LoadOptions](../../aspose.words.loading/loadoptions/)*) | Добавить документ, загрузив его с указанными параметрами загрузки. |
| [Load](../../aspose.words/idocumentprocessorplugin/load/)(*Stream, [LoadOptions](../../aspose.words.loading/loadoptions/)*) | Загрузите документ, используя указанные параметры загрузки. |
| [Save](../../aspose.words/idocumentprocessorplugin/save/)(*Stream, [SaveOptions](../../aspose.words.saving/saveoptions/)*) | Сохраните документ, загруженный[`Load`](./load/) метод в выходной поток с использованием указанных параметров сохранения. |
| [SetImageWatermark](../../aspose.words/idocumentprocessorplugin/setimagewatermark/)(*Stream, [ImageWatermarkOptions](../imagewatermarkoptions/)*) | Добавляет водяной знак на каждую страницу документа, загруженного[`Load`](./load/) метод. |
| [SetTextWatermark](../../aspose.words/idocumentprocessorplugin/settextwatermark/)(*string, [TextWatermarkOptions](../textwatermarkoptions/)*) | Добавляет текстовый водяной знак на каждую страницу документа, загруженного[`Load`](./load/) метод. |
| [ToDocument](../../aspose.words/idocumentprocessorplugin/todocument/)() | Анализирует документ, загруженный[`Load`](./load/) метод в[`Document`](../document/) объект. |
| [ToPages](../../aspose.words/idocumentprocessorplugin/topages/)(*[FixedPageSaveOptions](../../aspose.words.saving/fixedpagesaveoptions/)*) | Сохраняет каждую страницу документа, загруженного[`Load`](./load/) метод с использованием указанных фиксированных параметров сохранения страницы. |

### Смотрите также

* пространство имен [Aspose.Words](../../aspose.words/)
* сборка [Aspose.Words](../../)
