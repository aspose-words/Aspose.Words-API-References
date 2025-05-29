---
title: DocumentBuilder.InsertComboBox
linktitle: InsertComboBox
articleTitle: InsertComboBox
second_title: Aspose.Words для .NET
description: Улучшите свои документы с помощью метода DocumentBuilder InsertComboBox. Легко добавляйте интерактивные поля формы со списком для улучшения пользовательского опыта.
type: docs
weight: 300
url: /ru/net/aspose.words/documentbuilder/insertcombobox/
---
## DocumentBuilder.InsertComboBox method

Вставляет поле формы со списком в текущую позицию.

```csharp
public FormField InsertComboBox(string name, string[] items, int selectedIndex)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| name | String | Имя поля формы. Может быть пустой строкой. Значение длиннее 20 символов будет усечено. |
| items | String[] | Элементы ComboBox. Максимум 25 элементов. |
| selectedIndex | Int32 | Индекс выбранного элемента в ComboBox. |

### Возвращаемое значение

Узел поля формы, который был только что вставлен.

## Примечания

Если указать имя поля формы, то автоматически будет создана закладка с таким же именем.

## Примеры

Показывает, как вставить поле формы со списком в документ.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Вставьте форму, предлагающую пользователю выбрать один из пунктов меню.
builder.Write("Pick a fruit: ");
string[] items = { "Apple", "Banana", "Cherry" };
builder.InsertComboBox("DropDown", items, 0);

doc.Save(ArtifactsDir + "DocumentBuilder.InsertComboBox.docx");
```

Показывает, как создавать поля формы.

```csharp
DocumentBuilder builder = new DocumentBuilder();

// Поля формы — это объекты в документе, с которыми пользователь может взаимодействовать, получая запросы на ввод значений.
// Мы можем создать их с помощью конструктора документов, и ниже приведены два способа сделать это.
// 1 - Основной ввод текста:
builder.InsertTextInput("My text input", TextFormFieldType.Regular, 
    "", "Enter your name here", 30);

// 2 — Поле со списком с текстом подсказки и диапазоном возможных значений:
string[] items =
{
    "-- Select your favorite footwear --", "Sneakers", "Oxfords", "Flip-flops", "Other"
};

builder.InsertParagraph();
builder.InsertComboBox("My combo box", items, 0);

builder.Document.Save(ArtifactsDir + "DocumentBuilder.CreateForm.docx");
```

### Смотрите также

* class [FormField](../../../aspose.words.fields/formfield/)
* class [DocumentBuilder](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
