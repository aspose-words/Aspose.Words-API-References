---
title: Section.ProtectedForForms
second_title: Справочник по API Aspose.Words для .NET
description: Section свойство. True если раздел защищен для форм. Если раздел защищен для форм пользователи могут выбирать и изменять текст только в полях формы в Microsoft Word.
type: docs
weight: 60
url: /ru/net/aspose.words/section/protectedforforms/
---
## Section.ProtectedForForms property

True, если раздел защищен для форм. Если раздел защищен для форм, пользователи могут выбирать и изменять текст только в полях формы в Microsoft Word.

```csharp
public bool ProtectedForForms { get; set; }
```

### Примеры

Показывает, как отключить защиту раздела.

```csharp
Document doc = new Document();

DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Section 1. Hello world!");
builder.InsertBreak(BreakType.SectionBreakNewPage);

builder.Writeln("Section 2. Hello again!");
builder.Write("Please enter text here: ");
builder.InsertTextInput("TextInput1", TextFormFieldType.Regular, "", "Placeholder text", 0);

// Применяем защиту от записи к каждому разделу документа.
doc.Protect(ProtectionType.AllowOnlyFormFields);

// Отключаем защиту от записи для первого раздела.
doc.Sections[0].ProtectedForForms = false;

// В этом выходном документе мы сможем свободно редактировать первый раздел,
// и мы сможем редактировать содержимое поля формы только во втором разделе.
doc.Save(ArtifactsDir + "Section.Protect.docx");
```

### Смотрите также

* class [Section](../)
* пространство имен [Aspose.Words](../../section/)
* сборка [Aspose.Words](../../../)


