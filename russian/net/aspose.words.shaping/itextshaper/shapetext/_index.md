---
title: ITextShaper.ShapeText
linktitle: ShapeText
articleTitle: ShapeText
second_title: Aspose.Words для .NET
description: Откройте для себя метод ShapeText iTextShaper, который эффективно генерирует объекты Cluster из текстовых фрагментов, обеспечивая точное форматирование и выравнивание текста.
type: docs
weight: 10
url: /ru/net/aspose.words.shaping/itextshaper/shapetext/
---
## ITextShaper.ShapeText method

Возврат[`Cluster`](../../cluster/)объекты, сгенерированные из последовательности текстовых фрагментов. Длина возвращаемого массива равна длине*runs* . Если запуск по индексу имеет соответствующие кластеры, то результат по тому же индексу будет содержать их запись.

```csharp
public Cluster[][] ShapeText(string[] runs, Direction direction, UnicodeScript script, 
    FontFeature[] enabledFontFeatures, VariationAxisCoordinate[] variations)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| runs | String[] | Последовательность фрагментов текста |
| direction | Direction | Направление текста |
| script | UnicodeScript | Сценарий |
| enabledFontFeatures | FontFeature[] | Набор явно включенных функций OpenType, которые следует учитывать |
| variations | VariationAxisCoordinate[] | Значения оси вариации шрифта |

### Смотрите также

* class [Cluster](../../cluster/)
* enum [Direction](../../direction/)
* enum [UnicodeScript](../../unicodescript/)
* enum [FontFeature](../../fontfeature/)
* class [VariationAxisCoordinate](../../variationaxiscoordinate/)
* interface [ITextShaper](../)
* пространство имен [Aspose.Words.Shaping](../../../aspose.words.shaping/)
* сборка [Aspose.Words](../../../)
