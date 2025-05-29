---
title: ListLevel.CustomNumberStyleFormat
linktitle: CustomNumberStyleFormat
articleTitle: CustomNumberStyleFormat
second_title: Aspose.Words для .NET
description: Настройте уровни списка с помощью свойства ListLevel CustomNumberStyleFormat. Легко устанавливайте уникальные форматы чисел для улучшенного оформления документа.
type: docs
weight: 20
url: /ru/net/aspose.words.lists/listlevel/customnumberstyleformat/
---
## ListLevel.CustomNumberStyleFormat property

Получает или задает пользовательский формат стиля чисел для этого уровня списка. Например: "a, ç, ĝ, ...".

```csharp
public string CustomNumberStyleFormat { get; set; }
```

## Примеры

Показывает, как задать формат стиля номера клиента.

```csharp
Document doc = new Document(MyDir + "List with leading zero.docx");

doc.UpdateListLabels();

ParagraphCollection paras = doc.FirstSection.Body.Paragraphs;
Assert.AreEqual("001.", paras[0].ListLabel.LabelString);
Assert.AreEqual("0001.", paras[1].ListLabel.LabelString);
Assert.AreEqual("0002.", paras[2].ListLabel.LabelString);

paras[1].ListFormat.ListLevel.CustomNumberStyleFormat = "001, 002, 003, ...";

doc.UpdateListLabels();

Assert.AreEqual("001.", paras[0].ListLabel.LabelString);
Assert.AreEqual("001.", paras[1].ListLabel.LabelString);
Assert.AreEqual("002.", paras[2].ListLabel.LabelString);
```

Показывает, как получить формат списка с пользовательским стилем чисел.

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
* пространство имен [Aspose.Words.Lists](../../../aspose.words.lists/)
* сборка [Aspose.Words](../../../)
