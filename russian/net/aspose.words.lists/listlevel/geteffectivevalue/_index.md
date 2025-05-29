---
title: ListLevel.GetEffectiveValue
linktitle: GetEffectiveValue
articleTitle: GetEffectiveValue
second_title: Aspose.Words для .NET
description: Откройте для себя метод ListLevel GetEffectiveValue для простого получения строковых представлений элементов списка. Настройте с помощью NumberStyle и параметров формата!
type: docs
weight: 190
url: /ru/net/aspose.words.lists/listlevel/geteffectivevalue/
---
## ListLevel.GetEffectiveValue method

Сообщает строковое представление[`ListLevel`](../)объект для указанного index элемента списка. Параметры указывают[`NumberStyle`](../../../aspose.words/numberstyle/) и необязательный формат string , используемый, когдаCustom указано.

```csharp
public static string GetEffectiveValue(int index, NumberStyle numberStyle, 
    string customNumberStyleFormat)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| index | Int32 | Индекс элемента списка (должен быть в диапазоне от 1 до 32767). |
| numberStyle | NumberStyle | [`NumberStyle`](../../../aspose.words/numberstyle/) принадлежащий[`ListLevel`](../) объект. |
| customNumberStyleFormat | String | Необязательная строка формата, используемая приCustom указан (например, "a, ç, ĝ, ..."). В других случаях этот параметр должен быть`нулевой` или пусто. |

### Возвращаемое значение

Строковое представление[`ListLevel`](../) объект, описанный*numberStyle* параметр and *customNumberStyleFormat* параметр, в элементе списка в позиции, определяемой*index* параметр.

### Исключения

| исключение | условие |
| --- | --- |
| ArgumentException | *customNumberStyleFormat* является`нулевой` или пустым, когда*numberStyle* это индивидуальный заказ.-или- *customNumberStyleFormat* не`нулевой` или пустым, когда*numberStyle* не является пользовательским.-или- *customNumberStyleFormat* недействителен. |
| ArgumentOutOfRangeException | индекс находится вне диапазона. |

## Примеры

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

* enum [NumberStyle](../../../aspose.words/numberstyle/)
* class [ListLevel](../)
* пространство имен [Aspose.Words.Lists](../../../aspose.words.lists/)
* сборка [Aspose.Words](../../../)
