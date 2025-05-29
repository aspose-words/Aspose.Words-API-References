---
title: FindReplaceOptions.IgnoreFields
linktitle: IgnoreFields
articleTitle: IgnoreFields
second_title: Aspose.Words для .NET
description: Откройте для себя свойство FindReplaceOptions IgnoreFields для легкого управления текстом в полях. Контролируйте, когда игнорировать контент для эффективного поиска!
type: docs
weight: 80
url: /ru/net/aspose.words.replacing/findreplaceoptions/ignorefields/
---
## FindReplaceOptions.IgnoreFields property

Возвращает или задает логическое значение, указывающее, следует ли игнорировать текст внутри полей. Значение по умолчанию:`ЛОЖЬ` .

```csharp
public bool IgnoreFields { get; set; }
```

## Примечания

Эта опция влияет на все поле (все узлы между FieldStart иFieldEnd).

Чтобы игнорировать только коды полей, используйте соответствующую опцию.[`IgnoreFieldCodes`](../ignorefieldcodes/).

## Примеры

Показывает, как игнорировать текст внутри полей.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Hello world!");
builder.InsertField("QUOTE", "Hello again!");

// Мы можем использовать объект «FindReplaceOptions» для изменения процесса поиска и замены.
FindReplaceOptions options = new FindReplaceOptions();

// Установите флаг "IgnoreFields" на "true", чтобы получить функцию поиска и замены
// операция игнорирования текста внутри полей.
// Установите флаг "IgnoreFields" на "false", чтобы получить функцию поиска и замены
// операция также для поиска текста внутри полей.
options.IgnoreFields = ignoreTextInsideFields;

doc.Range.Replace("Hello", "Greetings", options);

Assert.AreEqual(
    ignoreTextInsideFields
        ? "Greetings world!\r\u0013QUOTE\u0014Hello again!\u0015"
        : "Greetings world!\r\u0013QUOTE\u0014Greetings again!\u0015", doc.GetText().Trim());
```

### Смотрите также

* class [FindReplaceOptions](../)
* пространство имен [Aspose.Words.Replacing](../../../aspose.words.replacing/)
* сборка [Aspose.Words](../../../)
