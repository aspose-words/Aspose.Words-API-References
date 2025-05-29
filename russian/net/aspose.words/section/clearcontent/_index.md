---
title: Section.ClearContent
linktitle: ClearContent
articleTitle: ClearContent
second_title: Aspose.Words для .NET
description: Легко очищайте разделы с помощью метода ClearContent. Улучшите свой рабочий процесс и повысьте эффективность управления контентом уже сегодня!
type: docs
weight: 110
url: /ru/net/aspose.words/section/clearcontent/
---
## Section.ClearContent method

Очищает раздел.

```csharp
public void ClearContent()
```

## Примечания

Текст[`Body`](../body/) очищается, остается только один пустой абзац, представляющий собой разрыв раздела.

Текст всех верхних и нижних колонтитулов очищается, но[`HeaderFooter`](../../headerfooter/) Сами объекты не удаляются.

## Примеры

Показывает, как очистить содержимое раздела.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Hello world!");

Assert.AreEqual("Hello world!", doc.GetText().Trim());
Assert.AreEqual(1, doc.FirstSection.Body.Paragraphs.Count);

// Запуск метода "ClearContent" удалит все содержимое раздела
// но оставьте пустой абзац, чтобы снова добавить содержимое.
doc.FirstSection.ClearContent();

Assert.AreEqual(string.Empty, doc.GetText().Trim());
Assert.AreEqual(1, doc.FirstSection.Body.Paragraphs.Count);
```

### Смотрите также

* class [Section](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
