---
title: ListLevel.GetEffectiveValue
linktitle: GetEffectiveValue
articleTitle: GetEffectiveValue
second_title: Aspose.Words для .NET
description: ListLevel GetEffectiveValue метод. Сообщает строковое представлениеListLevelобъект для указанного index элемента списка. Параметры определяютNumberStyle и необязательный формат string  используемый когдаCustom указано на С#.
type: docs
weight: 190
url: /ru/net/aspose.words.lists/listlevel/geteffectivevalue/
---
## ListLevel.GetEffectiveValue method

Сообщает строковое представление[`ListLevel`](../)объект для указанного index элемента списка. Параметры определяют[`NumberStyle`](../../../aspose.words/numberstyle/) и необязательный формат string , используемый, когдаCustom указано.

```csharp
public static string GetEffectiveValue(int index, NumberStyle numberStyle, 
    string customNumberStyleFormat)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| index | Int32 | Индекс элемента списка (должен быть в диапазоне от 1 до 32767). |
| numberStyle | NumberStyle | [`NumberStyle`](../../../aspose.words/numberstyle/) принадлежащий[`ListLevel`](../) объект. |
| customNumberStyleFormat | String | Необязательная строка формата, используемая, когдаCustom указан (например, "a, ç, ĝ, ..."). В остальных случаях этот параметр должен быть`нулевой` или пусто. |

### Возвращаемое значение

Строковое представление[`ListLevel`](../) объект, описанный*numberStyle* параметр and *customNumberStyleFormat* параметр, в элементе списка в позиции, определяемой*index* параметр.

### Исключения

| исключение | условие |
| --- | --- |
| ArgumentException | *customNumberStyleFormat* является`нулевой` или пусто, когда*numberStyle* является пользовательским.-или- *customNumberStyleFormat* не является`нулевой` или пусто, когда*numberStyle* не является пользовательским.-или- *customNumberStyleFormat* неверно. |
| ArgumentOutOfRangeException | индекс выходит за пределы допустимого диапазона. |

## Примеры

Показывает, как получить формат списка с пользовательским числовым стилем.

```csharp
Document doc = new Document(MyDir + "List with leading zero.docx");

ListLevel listLevel = doc.FirstSection.Body.Paragraphs[0].ListFormat.ListLevel;

string customNumberStyleFormat = string.Empty;

if (listLevel.NumberStyle == NumberStyle.Custom)
    customNumberStyleFormat = listLevel.CustomNumberStyleFormat;

Assert.AreEqual("001, 002, 003, ...", customNumberStyleFormat);

// Мы можем получить значение по указанному индексу элемента списка.
Assert.AreEqual("iv", ListLevel.GetEffectiveValue(4, NumberStyle.LowercaseRoman, null));
Assert.AreEqual("005", ListLevel.GetEffectiveValue(5, NumberStyle.Custom, customNumberStyleFormat));
```

### Смотрите также

* enum [NumberStyle](../../../aspose.words/numberstyle/)
* class [ListLevel](../)
* пространство имен [Aspose.Words.Lists](../../../aspose.words.lists/)
* сборка [Aspose.Words](../../../)
