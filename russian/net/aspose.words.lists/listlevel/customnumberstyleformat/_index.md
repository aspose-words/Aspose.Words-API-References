---
title: ListLevel.CustomNumberStyleFormat
second_title: Справочник по API Aspose.Words для .NET
description: ListLevel свойство. Получает пользовательский формат числового стиля для этого уровня списка. Например a ç ĝ ....
type: docs
weight: 20
url: /ru/net/aspose.words.lists/listlevel/customnumberstyleformat/
---
## ListLevel.CustomNumberStyleFormat property

Получает пользовательский формат числового стиля для этого уровня списка. Например: "a, ç, ĝ, ...".

```csharp
public string CustomNumberStyleFormat { get; }
```

### Примеры

Показывает, как получить формат для списка с пользовательским стилем чисел.

```csharp
Document doc = new Document(MyDir + "List with leading zero.docx");

ListLevel listLevel = doc.FirstSection.Body.Paragraphs[0].ListFormat.ListLevel;

string customNumberStyleFormat = string.Empty;

if (listLevel.NumberStyle == NumberStyle.Custom)
    customNumberStyleFormat = listLevel.CustomNumberStyleFormat;

Assert.AreEqual("001, 002, 003, ...", customNumberStyleFormat);

// Мы можем получить значение для указанного индекса элемента списка.
Assert.AreEqual("iv", ListLevel.GetEffectiveValue(4, NumberStyle.LowercaseRoman, null));
Assert.AreEqual("005", ListLevel.GetEffectiveValue(5, NumberStyle.Custom, customNumberStyleFormat));
```

### Смотрите также

* class [ListLevel](../)
* пространство имен [Aspose.Words.Lists](../../listlevel/)
* сборка [Aspose.Words](../../../)


