---
title: BorderCollection.GetEnumerator
linktitle: GetEnumerator
articleTitle: GetEnumerator
second_title: Aspose.Words для .NET
description: Откройте для себя метод BorderCollection GetEnumerator, который позволяет легко перебирать все границы, повышая эффективность кодирования и управления коллекциями.
type: docs
weight: 160
url: /ru/net/aspose.words/bordercollection/getenumerator/
---
## BorderCollection.GetEnumerator method

Возвращает объект-перечислитель, который можно использовать для перебора всех границ в коллекции.

```csharp
public IEnumerator<Border> GetEnumerator()
```

## Примеры

Показывает, как перебрать и отредактировать все границы в объекте формата абзаца.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Настройте параметры формата абзаца конструктора, чтобы создать зеленую волнистую границу со всех сторон.
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

// Вставьте абзац. Наши настройки границ будут определять внешний вид его границ.
builder.Writeln("Hello world!");

doc.Save(ArtifactsDir + "BorderCollection.GetBordersEnumerator.docx");
```

### Смотрите также

* class [Border](../../border/)
* class [BorderCollection](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
