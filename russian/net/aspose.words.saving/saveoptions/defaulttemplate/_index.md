---
title: DefaultTemplate
second_title: Справочник по API Aspose.Words для .NET
description: Получает или задает путь к шаблону по умолчанию включая имя файла. Значение по умолчанию для этого свойства пустой строки Empty .
type: docs
weight: 40
url: /ru/net/aspose.words.saving/saveoptions/defaulttemplate/
---
## SaveOptions.DefaultTemplate property

Получает или задает путь к шаблону по умолчанию (включая имя файла). Значение по умолчанию для этого свойства: **пустой строки** (Empty ).

```csharp
public string DefaultTemplate { get; set; }
```

### Примечания

Если указано, этот путь используется для загрузки шаблона, когда[`AutomaticallyUpdateStyles`](../../../aspose.words/document/automaticallyupdatestyles) верно, но[`AttachedTemplate`](../../../aspose.words/document/attachedtemplate) пустой.

### Примеры

Показывает, как задать шаблон по умолчанию для документов, к которым нет прикрепленных шаблонов.

```csharp
Document doc = new Document();

// Включить автоматическое обновление стиля, но не прикреплять шаблонный документ.
doc.AutomaticallyUpdateStyles = true;

Assert.AreEqual(string.Empty, doc.AttachedTemplate);

// Так как документа-шаблона нет, в документе негде было отслеживать изменения стилей.
// Используйте объект SaveOptions для автоматической установки шаблона
// если документа, который мы сохраняем, нет.
SaveOptions options = SaveOptions.CreateSaveOptions("Document.DefaultTemplate.docx");
options.DefaultTemplate = MyDir + "Business brochure.dotx";

doc.Save(ArtifactsDir + "Document.DefaultTemplate.docx", options);
```

### Смотрите также

* class [SaveOptions](../../saveoptions)
* пространство имен [Aspose.Words.Saving](../../saveoptions)
* сборка [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
