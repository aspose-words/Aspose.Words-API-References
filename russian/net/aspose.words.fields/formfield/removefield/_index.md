---
title: FormField.RemoveField
linktitle: RemoveField
articleTitle: RemoveField
second_title: Aspose.Words для .NET
description: С легкостью удаляйте целые поля форм с помощью метода FormField RemoveField, повышая ясность и организованность вашего документа.
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

Если с полем формы связана закладка, то закладка не удаляется.

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
