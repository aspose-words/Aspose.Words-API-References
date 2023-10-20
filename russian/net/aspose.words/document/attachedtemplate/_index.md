---
title: Document.AttachedTemplate
linktitle: AttachedTemplate
articleTitle: AttachedTemplate
second_title: Aspose.Words для .NET
description: Document AttachedTemplate свойство. Получает или задает полный путь к шаблону прикрепленному к документу на С#.
type: docs
weight: 20
url: /ru/net/aspose.words/document/attachedtemplate/
---
## Document.AttachedTemplate property

Получает или задает полный путь к шаблону, прикрепленному к документу.

```csharp
public string AttachedTemplate { get; set; }
```

### Исключения

| исключение | условие |
| --- | --- |
| ArgumentNullException | Выдает, если вы пытаетесь установить`нулевой` ценить. |

## Примечания

Пустая строка означает, что документ прикреплен к обычному шаблону.

## Примеры

Показывает, как установить шаблон по умолчанию для документов, к которым не прикреплены шаблоны.

```csharp
Document doc = new Document();

// Включаем автоматическое обновление стилей, но не прикрепляем документ-шаблон.
doc.AutomaticallyUpdateStyles = true;

Assert.AreEqual(string.Empty, doc.AttachedTemplate);

// Поскольку документа-шаблона нет, в документе негде было отслеживать изменения стиля.
// Используйте объект SaveOptions для автоматической установки шаблона
// если в документе, который мы сохраняем, его нет.
SaveOptions options = SaveOptions.CreateSaveOptions("Document.DefaultTemplate.docx");
options.DefaultTemplate = MyDir + "Business brochure.dotx";

doc.Save(ArtifactsDir + "Document.DefaultTemplate.docx", options);
```

### Смотрите также

* class [Document](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
