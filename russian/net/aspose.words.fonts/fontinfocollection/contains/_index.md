---
title: FontInfoCollection.Contains
linktitle: Contains
articleTitle: Contains
second_title: Aspose.Words для .NET
description: FontInfoCollection Contains метод. Определяет содержит ли коллекция шрифт с данным именем на С#.
type: docs
weight: 60
url: /ru/net/aspose.words.fonts/fontinfocollection/contains/
---
## FontInfoCollection.Contains method

Определяет, содержит ли коллекция шрифт с данным именем.

```csharp
public bool Contains(string name)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| name | String | Имя шрифта, который необходимо найти, без учета регистра. |

### Возвращаемое значение

`истинный` если предмет найден в коллекции; в противном случае,`ЛОЖЬ`.

## Примеры

Показывает информацию о шрифтах, присутствующих в пустом документе.

```csharp
Document doc = new Document();

// Пустой документ содержит 3 шрифта по умолчанию. Каждый шрифт в документе
// будет иметь соответствующий объект FontInfo, содержащий сведения об этом шрифте.
Assert.AreEqual(3, doc.FontInfos.Count);

Assert.True(doc.FontInfos.Contains("Times New Roman"));
Assert.AreEqual(204, doc.FontInfos["Times New Roman"].Charset);

Assert.True(doc.FontInfos.Contains("Symbol"));
Assert.True(doc.FontInfos.Contains("Arial"));
```

### Смотрите также

* class [FontInfoCollection](../)
* пространство имен [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* сборка [Aspose.Words](../../../)
