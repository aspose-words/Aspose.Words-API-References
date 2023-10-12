---
title: DocumentBuilder.InsertComboBox
second_title: Справочник по API Aspose.Words для .NET
description: DocumentBuilder метод. Вставляет поле формы со списком в текущую позицию.
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
| name | String | Имя поля формы. Может быть пустой строкой. Значение длиной более 20 символов будет обрезано. |
| items | String[] | Элементы ComboBox. Максимум — 25 предметов. |
| selectedIndex | Int32 | Индекс выбранного элемента в ComboBox. |

### Возвращаемое значение

Узел поля формы, который был только что вставлен.

### Примечания

Если вы укажете имя для поля формы, то автоматически создастся закладка с таким же именем.

### Примеры

Показывает, как вставить поле формы со списком в документ.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Вставляем форму, предлагающую пользователю выбрать один из пунктов меню.
builder.Write("Pick a fruit: ");
string[] items = { "Apple", "Banana", "Cherry" };
builder.InsertComboBox("DropDown", items, 0);

doc.Save(ArtifactsDir + "DocumentBuilder.InsertComboBox.docx");
```

Показывает, как создавать поля формы.

```csharp
DocumentBuilder builder = new DocumentBuilder();

// Поля формы — это объекты в документе, с которыми пользователь может взаимодействовать, получая запрос на ввод значений.
// Мы можем создать их с помощью построителя документов, и ниже приведены два способа сделать это.
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
* пространство имен [Aspose.Words](../../documentbuilder/)
* сборка [Aspose.Words](../../../)


