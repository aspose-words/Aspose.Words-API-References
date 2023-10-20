---
title: ProtectionType Enum
linktitle: ProtectionType
articleTitle: ProtectionType
second_title: Aspose.Words для .NET
description: Aspose.Words.ProtectionType перечисление. Тип защиты документа на С#.
type: docs
weight: 4510
url: /ru/net/aspose.words/protectiontype/
---
## ProtectionType enumeration

Тип защиты документа.

```csharp
public enum ProtectionType
```

### Ценности

| Имя | Ценность | Описание |
| --- | --- | --- |
| AllowOnlyComments | `1` | Пользователь может изменять только комментарии в документе. |
| AllowOnlyFormFields | `2` | Пользователь может вводить данные только в поля формы документа. |
| AllowOnlyRevisions | `0` | Пользователь может добавлять к документу только отметки редакции. |
| ReadOnly | `3` | В документ нельзя вносить изменения. Доступно начиная с Microsoft Word 2003. . |
| NoProtection | `-1` | Документ не защищен. |

## Примеры

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

* пространство имен [Aspose.Words](../../aspose.words/)
* сборка [Aspose.Words](../../)
