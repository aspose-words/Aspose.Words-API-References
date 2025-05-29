---
title: TextFormFieldType Enum
linktitle: TextFormFieldType
articleTitle: TextFormFieldType
second_title: Aspose.Words для .NET
description: Откройте для себя перечисление Aspose.Words.Fields.TextFormFieldType, определяющее различные типы полей текстовой формы для улучшенной автоматизации и настройки документов.
type: docs
weight: 3180
url: /ru/net/aspose.words.fields/textformfieldtype/
---
## TextFormFieldType enumeration

Указывает тип поля текстовой формы.

```csharp
public enum TextFormFieldType
```

### Ценности

| Имя | Ценность | Описание |
| --- | --- | --- |
| Regular | `0` | Поле текстовой формы может содержать любой текст. |
| Number | `1` | Поле текстовой формы может содержать только цифры. |
| Date | `2` | Поле текстовой формы может содержать только допустимое значение даты. |
| CurrentDate | `3` | Значение поля текстовой формы — это текущая дата обновления поля. |
| CurrentTime | `4` | Значение поля текстовой формы — это текущее время обновления поля. |
| Calculated | `5` | Значение поля текстовой формы вычисляется из выражения, указанного в [`TextInputDefault`](../formfield/textinputdefault/) свойство. |

## Примеры

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

* пространство имен [Aspose.Words.Fields](../../aspose.words.fields/)
* сборка [Aspose.Words](../../)
