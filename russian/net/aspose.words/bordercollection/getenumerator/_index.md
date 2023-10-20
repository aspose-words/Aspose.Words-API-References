---
title: BorderCollection.GetEnumerator
linktitle: GetEnumerator
articleTitle: GetEnumerator
second_title: Aspose.Words для .NET
description: BorderCollection GetEnumerator метод. Возвращает объект перечислителя который можно использовать для обхода всех границ коллекции на С#.
type: docs
weight: 160
url: /ru/net/aspose.words/bordercollection/getenumerator/
---
## BorderCollection.GetEnumerator method

Возвращает объект перечислителя, который можно использовать для обхода всех границ коллекции.

```csharp
public IEnumerator<Border> GetEnumerator()
```

## Примеры

Показывает, как перебирать и редактировать все границы объекта формата абзаца.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Настройте параметры формата абзаца в конструкторе, чтобы создать зеленую волнистую рамку со всех сторон.
BorderCollection borders = builder.ParagraphFormat.Borders;

using (IEnumerator<Border> enumerator = borders.GetEnumerator())
{
    while (enumerator.MoveNext())
    {
        Border border = enumerator.Current;
        border.Color = Color.Green;
        border.LineStyle = LineStyle.Wave;
        border.LineWidth = 3;
    }
}

// Вставляем абзац. Наши настройки границы будут определять внешний вид границы.
builder.Writeln("Hello world!");

doc.Save(ArtifactsDir + "BorderCollection.GetBordersEnumerator.docx");
```

### Смотрите также

* class [Border](../../border/)
* class [BorderCollection](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
