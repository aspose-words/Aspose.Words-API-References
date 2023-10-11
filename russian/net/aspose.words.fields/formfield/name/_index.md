---
title: FormField.Name
second_title: Справочник по API Aspose.Words для .NET
description: FormField свойство. Получает или задает имя поля формы.
type: docs
weight: 130
url: /ru/net/aspose.words.fields/formfield/name/
---
## FormField.Name property

Получает или задает имя поля формы.

```csharp
public string Name { get; set; }
```

### Примечания

Microsoft Word допускает строки длиной не более 20 символов.

### Примеры

Показывает, как вставить поле со списком.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Please select a fruit: ");

// Вставляем поле со списком, которое позволит пользователю выбрать вариант из коллекции строк.
FormField comboBox = builder.InsertComboBox("MyComboBox", new[] { "Apple", "Banana", "Cherry" }, 0);

Assert.AreEqual("MyComboBox", comboBox.Name);
Assert.AreEqual(FieldType.FieldFormDropDown, comboBox.Type);
Assert.AreEqual("Apple", comboBox.Result);

// Поле формы появится в виде html-тега select.
doc.Save(ArtifactsDir + "FormFields.Create.html");
```

### Смотрите также

* class [FormField](../)
* пространство имен [Aspose.Words.Fields](../../formfield/)
* сборка [Aspose.Words](../../../)


