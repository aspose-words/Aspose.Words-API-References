---
title: DocumentBase.Document
linktitle: Document
articleTitle: Document
second_title: Aspose.Words для .NET
description: Изучите свойства DocumentBase для эффективного управления документами. Разблокируйте бесперебойный доступ и улучшите свой рабочий процесс сегодня!
type: docs
weight: 20
url: /ru/net/aspose.words/documentbase/document/
---
## DocumentBase.Document property

Получает этот экземпляр.

```csharp
public override DocumentBase Document { get; }
```

## Примеры

Показывает, как создать простой документ.

```csharp
Document doc = new Document();

// Новые объекты документа по умолчанию имеют минимальный набор узлов
// требуется для начала добавления контента, такого как текст и фигуры: Раздел, Тело и Абзац.
doc.AppendChild(new Section(doc))
    .AppendChild(new Body(doc))
    .AppendChild(new Paragraph(doc))
    .AppendChild(new Run(doc, "Hello world!"));
```

### Смотрите также

* class [DocumentBase](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
