---
title: Document.AutomaticallyUpdateStyles
linktitle: AutomaticallyUpdateStyles
articleTitle: AutomaticallyUpdateStyles
second_title: Aspose.Words для .NET
description: Узнайте, как свойство AutomaticallyUpdateStyles в MS Word обеспечивает синхронизацию стилей документа с шаблоном каждый раз при его открытии, повышая согласованность.
type: docs
weight: 30
url: /ru/net/aspose.words/document/automaticallyupdatestyles/
---
## Document.AutomaticallyUpdateStyles property

Возвращает или задает флаг, указывающий, обновляются ли стили в документе в соответствии со стилями в прикрепленном шаблоне каждый раз при открытии документа в MS Word.

```csharp
public bool AutomaticallyUpdateStyles { get; set; }
```

## Примеры

Показывает, как прикрепить шаблон к документу.

```csharp
Document doc = new Document();

// Документы Microsoft Word по умолчанию поставляются с прикрепленным шаблоном под названием «Normal.dotm».
// Для пустых документов Aspose.Words шаблона по умолчанию нет.
Assert.AreEqual(string.Empty, doc.AttachedTemplate);

// Прикрепите шаблон, затем установите флаг для применения изменений стиля
// внутри шаблона для стилей в нашем документе.
doc.AttachedTemplate = MyDir + "Business brochure.dotx";
doc.AutomaticallyUpdateStyles = true;

doc.Save(ArtifactsDir + "Document.AutomaticallyUpdateStyles.docx");
```

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
