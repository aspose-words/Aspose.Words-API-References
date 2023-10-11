---
title: SaveOptions.DefaultTemplate
second_title: Справочник по API Aspose.Words для .NET
description: SaveOptions свойство. Получает или задает путь к шаблону по умолчанию включая имя файла. Значение по умолчанию для этого свойства пустая строка Empty.
type: docs
weight: 40
url: /ru/net/aspose.words.saving/saveoptions/defaulttemplate/
---
## SaveOptions.DefaultTemplate property

Получает или задает путь к шаблону по умолчанию (включая имя файла). Значение по умолчанию для этого свойства: **пустая строка** (Empty).

```csharp
public string DefaultTemplate { get; set; }
```

### Примечания

Если указано, этот путь используется для загрузки шаблона при[`AutomaticallyUpdateStyles`](../../../aspose.words/document/automaticallyupdatestyles/) является`истинный` , но[`AttachedTemplate`](../../../aspose.words/document/attachedtemplate/) пусто.

### Примеры

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

* class [SaveOptions](../)
* пространство имен [Aspose.Words.Saving](../../saveoptions/)
* сборка [Aspose.Words](../../../)


