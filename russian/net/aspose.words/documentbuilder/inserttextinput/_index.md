---
title: DocumentBuilder.InsertTextInput
linktitle: InsertTextInput
articleTitle: InsertTextInput
second_title: Aspose.Words для .NET
description: DocumentBuilder InsertTextInput метод. Вставляет поле текстовой формы в текущую позицию на С#.
type: docs
weight: 470
url: /ru/net/aspose.words/documentbuilder/inserttextinput/
---
## DocumentBuilder.InsertTextInput method

Вставляет поле текстовой формы в текущую позицию.

```csharp
public FormField InsertTextInput(string name, TextFormFieldType type, string format, 
    string fieldValue, int maxLength)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| name | String | Имя поля формы. Может быть пустой строкой. |
| type | TextFormFieldType | Указывает тип поля текстовой формы. |
| format | String | Строка формата, используемая для форматирования значения поля формы. |
| fieldValue | String | Текст, который будет отображаться в поле. |
| maxLength | Int32 | Максимальная длина, которую пользователь может ввести в поле формы. Установите ноль для неограниченной длины. |

### Возвращаемое значение

Узел поля формы, который был только что вставлен.

## Примечания

Если вы укажете имя для поля формы, то автоматически создастся закладка с таким же именем.

## Примеры

Показывает, как вставить поле формы ввода текста в документ.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Вставляем форму, предлагающую пользователю ввести текст.
builder.InsertTextInput("TextInput", TextFormFieldType.Regular, "", "Enter your text here", 0);

doc.Save(ArtifactsDir + "DocumentBuilder.InsertTextInput.docx");
```

Показывает, как вставить поле формы ввода текста.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Please enter text here: ");

// Вставляем поле ввода текста, которое позволит пользователю щелкнуть его и ввести текст.
// Назначаем некоторый текст-заполнитель, который пользователь может перезаписать и передать
// максимальная длина текста равна 0, чтобы не налагать ограничений на содержимое поля формы.
builder.InsertTextInput("TextInput1", TextFormFieldType.Regular, "", "Placeholder text", 0);

// Поле формы появится в виде «входного» html-тега с типом «текст».
doc.Save(ArtifactsDir + "FormFields.TextInput.html");
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
* enum [TextFormFieldType](../../../aspose.words.fields/textformfieldtype/)
* class [DocumentBuilder](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
