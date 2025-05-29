---
title: ProtectionType Enum
linktitle: ProtectionType
articleTitle: ProtectionType
second_title: Aspose.Words для .NET
description: Откройте для себя перечисление Aspose.Words.ProtectionType для надежной защиты документов. Улучшите свои документы с помощью настраиваемых параметров защиты сегодня!
type: docs
weight: 5240
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
| AllowOnlyFormFields | `2` | Пользователь может вводить данные только в поля формы в документе. |
| AllowOnlyRevisions | `0` | Пользователь может только добавлять отметки о правках в документ. |
| ReadOnly | `3` | Внесение изменений в документ запрещено. Доступно с Microsoft Word 2003. |
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

// Применить защиту от записи к каждому разделу документа.
doc.Protect(ProtectionType.AllowOnlyFormFields);

// Отключаем защиту от записи для первого раздела.
doc.Sections[0].ProtectedForForms = false;

// В этом выходном документе мы сможем свободно редактировать первый раздел,
// и мы сможем редактировать только содержимое поля формы во втором разделе.
doc.Save(ArtifactsDir + "Section.Protect.docx");
```

### Смотрите также

* пространство имен [Aspose.Words](../../aspose.words/)
* сборка [Aspose.Words](../../)
