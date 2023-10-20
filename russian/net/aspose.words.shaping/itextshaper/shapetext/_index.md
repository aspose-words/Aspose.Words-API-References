---
title: ITextShaper.ShapeText
linktitle: ShapeText
articleTitle: ShapeText
second_title: Aspose.Words для .NET
description: ITextShaper ShapeText метод. ВозвращаетClusterобъекты сгенерированные из последовательности текстовых фрагментов. Длина возвращаемого массива равна длинеruns . Если запуск по индексу имеет соответствующие кластеры то результат по тому же индексу будет записан на С#.
type: docs
weight: 10
url: /ru/net/aspose.words.shaping/itextshaper/shapetext/
---
## ITextShaper.ShapeText method

Возвращает[`Cluster`](../../cluster/)объекты, сгенерированные из последовательности текстовых фрагментов. Длина возвращаемого массива равна длине*runs* . Если запуск по индексу имеет соответствующие кластеры, то результат по тому же индексу будет записан.

```csharp
public Cluster[][] ShapeText(string[] runs, Direction direction, UnicodeScript script, 
    params FontFeature[] fontFeatures)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| runs | String[] | Последовательность текстовых фрагментов |
| direction | Direction | Направление текста |
| script | UnicodeScript | Скрипт |
| fontFeatures | FontFeature[] | Набор функций, которые следует учитывать |

### Смотрите также

* class [Cluster](../../cluster/)
* enum [Direction](../../direction/)
* enum [UnicodeScript](../../unicodescript/)
* enum [FontFeature](../../fontfeature/)
* interface [ITextShaper](../)
* пространство имен [Aspose.Words.Shaping](../../../aspose.words.shaping/)
* сборка [Aspose.Words](../../../)
