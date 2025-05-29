---
title: Document.AttachedTemplate
linktitle: AttachedTemplate
articleTitle: AttachedTemplate
second_title: Aspose.Words для .NET
description: Узнайте, как эффективно управлять свойством Document AttachedTemplate. Легко задайте или получите полный путь к шаблону вашего документа для бесшовной интеграции.
type: docs
weight: 20
url: /ru/net/aspose.words/document/attachedtemplate/
---
## Document.AttachedTemplate property

Получает или задает полный путь шаблона, прикрепленного к документу.

```csharp
public string AttachedTemplate { get; set; }
```

### Исключения

| исключение | условие |
| --- | --- |
| ArgumentNullException | Выбрасывает, если вы пытаетесь установить`нулевой` ценить. |

## Примечания

Пустая строка означает, что документ прикреплен к шаблону Normal.

## Примеры

Показывает, как установить шаблон по умолчанию для документов, к которым не прикреплены шаблоны.

```csharp
Document doc = new Document();

// Включить автоматическое обновление стилей, но не прикреплять шаблон документа.
doc.AutomaticallyUpdateStyles = true;

Assert.AreEqual(string.Empty, doc.AttachedTemplate);

// Поскольку шаблон документа отсутствует, документу негде отслеживать изменения стиля.
// Используйте объект SaveOptions для автоматической установки шаблона
// если документ, который мы сохраняем, не имеет такового.
SaveOptions options = SaveOptions.CreateSaveOptions("Document.DefaultTemplate.docx");
options.DefaultTemplate = MyDir + "Business brochure.dotx";

doc.Save(ArtifactsDir + "Document.DefaultTemplate.docx", options);
```

### Смотрите также

* class [Document](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
