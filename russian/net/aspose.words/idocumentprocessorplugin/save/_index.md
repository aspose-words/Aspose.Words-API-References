---
title: IDocumentProcessorPlugin.Save
linktitle: Save
articleTitle: Save
second_title: Aspose.Words для .NET
description: С легкостью сохраняйте документы с помощью метода сохранения IDocumentProcessorPlugin, гарантируя оптимальный вывод и настраиваемые параметры сохранения в соответствии с вашими потребностями.
type: docs
weight: 30
url: /ru/net/aspose.words/idocumentprocessorplugin/save/
---
## IDocumentProcessorPlugin.Save method

Сохраните документ, загруженный[`Load`](../load/) метод в выходной поток с использованием указанных параметров сохранения.

```csharp
public void Save(Stream outputStream, SaveOptions saveOptions)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| outputStream | Stream | Выходной поток. |
| saveOptions | SaveOptions | Параметры сохранения. |

## Примечания

Если указан формат вывода — изображение, в выходной поток сохраняется только изображение первой страницы. Если указанный формат сохранения изначально не поддерживается плагином (требуется загрузка в[`Document`](../../document/)), метод выдает исключение.

### Смотрите также

* class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* interface [IDocumentProcessorPlugin](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
