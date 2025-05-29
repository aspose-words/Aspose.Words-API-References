---
title: FormField.Name
linktitle: Name
articleTitle: Name
second_title: Aspose.Words для .NET
description: Узнайте, как легко управлять свойством FormField Name, чтобы настраивать и оптимизировать формы для лучшего взаимодействия с пользователями и сбора данных.
type: docs
weight: 130
url: /ru/net/aspose.words.fields/formfield/name/
---
## FormField.Name property

Получает или задает имя поля формы.

```csharp
public string Name { get; set; }
```

## Примечания

Microsoft Word допускает строки длиной не более 20 символов.

## Примеры

Показывает, как вставить поле со списком.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Please select a fruit: ");

// Вставьте поле со списком, которое позволит пользователю выбрать вариант из набора строк.
FormField comboBox = builder.InsertComboBox("MyComboBox", new[] { "Apple", "Banana", "Cherry" }, 0);

Assert.AreEqual("MyComboBox", comboBox.Name);
Assert.AreEqual(FieldType.FieldFormDropDown, comboBox.Type);
Assert.AreEqual("Apple", comboBox.Result);

// Поле формы будет отображаться в виде HTML-тега «select».
doc.Save(ArtifactsDir + "FormFields.Create.html");
```

### Смотрите также

* class [FormField](../)
* пространство имен [Aspose.Words.Fields](../../../aspose.words.fields/)
* сборка [Aspose.Words](../../../)
