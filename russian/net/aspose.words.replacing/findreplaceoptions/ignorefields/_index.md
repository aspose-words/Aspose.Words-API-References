---
title: FindReplaceOptions.IgnoreFields
second_title: Справочник по API Aspose.Words для .NET
description: FindReplaceOptions свойство. Получает или задает логическое значение указывающее следует ли игнорировать текст внутри полей. Значение по умолчаниюЛОЖЬ .
type: docs
weight: 80
url: /ru/net/aspose.words.replacing/findreplaceoptions/ignorefields/
---
## FindReplaceOptions.IgnoreFields property

Получает или задает логическое значение, указывающее, следует ли игнорировать текст внутри полей. Значение по умолчанию:`ЛОЖЬ` .

```csharp
public bool IgnoreFields { get; set; }
```

### Примечания

Эта опция влияет на все поле (все узлы между FieldStart а такжеFieldEnd).

Чтобы игнорировать только коды полей, используйте соответствующую опцию[`IgnoreFieldCodes`](../ignorefieldcodes/).

### Примеры

Показывает, как игнорировать текст внутри полей.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Hello world!");
builder.InsertField("QUOTE", "Hello again!");

// Мы можем использовать объект «FindReplaceOptions», чтобы изменить процесс поиска и замены.
FindReplaceOptions options = new FindReplaceOptions();

// Установите для флага «IgnoreFields» значение «true», чтобы получить функцию поиска и замены
// операция для игнорирования текста внутри полей.
// Установите флаг «IgnoreFields» в «false», чтобы получить функцию поиска и замены
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
* пространство имен [Aspose.Words.Replacing](../../findreplaceoptions/)
* сборка [Aspose.Words](../../../)


