---
title: SaveOptions.DefaultTemplate
linktitle: DefaultTemplate
articleTitle: DefaultTemplate
second_title: Aspose.Words для .NET
description: Управляйте своими SaveOptions с легкостью! Установите или получите путь шаблона и имя файла по умолчанию для упрощенной обработки документов. Оптимизируйте свой рабочий процесс сегодня!
type: docs
weight: 40
url: /ru/net/aspose.words.saving/saveoptions/defaulttemplate/
---
## SaveOptions.DefaultTemplate property

Возвращает или задает путь к шаблону по умолчанию (включая имя файла). Значение по умолчанию для этого свойства:**пустая строка** (Empty ).

```csharp
public string DefaultTemplate { get; set; }
```

## Примечания

Если указан, этот путь используется для загрузки шаблона, когда[`AutomaticallyUpdateStyles`](../../../aspose.words/document/automaticallyupdatestyles/) является`истинный` , но[`AttachedTemplate`](../../../aspose.words/document/attachedtemplate/) пусто.

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

* class [SaveOptions](../)
* пространство имен [Aspose.Words.Saving](../../../aspose.words.saving/)
* сборка [Aspose.Words](../../../)
