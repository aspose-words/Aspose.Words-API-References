---
title: FormField.RemoveField
second_title: Справочник по API Aspose.Words для .NET
description: FormField метод. Удаляет все поле формы а не только специальный символ поля формы.
type: docs
weight: 240
url: /ru/net/aspose.words.fields/formfield/removefield/
---
## FormField.RemoveField method

Удаляет все поле формы, а не только специальный символ поля формы.

```csharp
public void RemoveField()
```

### Примечания

Если есть закладка, связанная с полем формы, закладка не удаляется.

### Примеры

Показывает, как удалить поле формы.

```csharp
Document doc = new Document(MyDir + "Form fields.docx");

FormField formField = doc.Range.FormFields[3];
formField.RemoveField();
```

### Смотрите также

* class [FormField](../)
* пространство имен [Aspose.Words.Fields](../../formfield/)
* сборка [Aspose.Words](../../../)


