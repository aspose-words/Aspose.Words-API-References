---
title: FormField.RemoveField
linktitle: RemoveField
articleTitle: RemoveField
second_title: Aspose.Words для .NET
description: FormField RemoveField метод. Удаляет все поле формы а не только специальный символ поля формы на С#.
type: docs
weight: 240
url: /ru/net/aspose.words.fields/formfield/removefield/
---
## FormField.RemoveField method

Удаляет все поле формы, а не только специальный символ поля формы.

```csharp
public void RemoveField()
```

## Примечания

Если с полем формы связана закладка, она не удаляется.

## Примеры

Показывает, как удалить поле формы.

```csharp
Document doc = new Document(MyDir + "Form fields.docx");

FormField formField = doc.Range.FormFields[3];
formField.RemoveField();
```

### Смотрите также

* class [FormField](../)
* пространство имен [Aspose.Words.Fields](../../../aspose.words.fields/)
* сборка [Aspose.Words](../../../)
