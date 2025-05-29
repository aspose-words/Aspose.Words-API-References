---
title: TableAlignment Enum
linktitle: TableAlignment
articleTitle: TableAlignment
second_title: Aspose.Words для .NET
description: Откройте для себя перечисление Aspose.Words.Tables.TableAlignment для оптимального выравнивания встроенных таблиц. Улучшите форматирование документов с точностью и легкостью.
type: docs
weight: 7200
url: /ru/net/aspose.words.tables/tablealignment/
---
## TableAlignment enumeration

Задает выравнивание для встроенной таблицы.

```csharp
public enum TableAlignment
```

### Ценности

| Имя | Ценность | Описание |
| --- | --- | --- |
| Left | `0` | Таблица выровнена по левому краю. |
| Center | `1` | Таблица отцентрирована. |
| Right | `2` | Таблица выровнена по правому краю. |

## Примеры

Показывает, как применить контурную рамку к таблице.

```csharp
Document doc = new Document(MyDir + "Tables.docx");
Table table = doc.FirstSection.Body.Tables[0];

// Выровняйте таблицу по центру страницы.
table.Alignment = TableAlignment.Center;

// Удалим все существующие границы и заливку из таблицы.
table.ClearBorders();
table.ClearShading();

// Добавляем зеленые границы к контуру таблицы.
table.SetBorder(BorderType.Left, LineStyle.Single, 1.5, Color.Green, true);
table.SetBorder(BorderType.Right, LineStyle.Single, 1.5, Color.Green, true);
table.SetBorder(BorderType.Top, LineStyle.Single, 1.5, Color.Green, true);
table.SetBorder(BorderType.Bottom, LineStyle.Single, 1.5, Color.Green, true);

// Заполните ячейки светло-зеленым сплошным цветом.
table.SetShading(TextureIndex.TextureSolid, Color.LightGreen, Color.Empty);

doc.Save(ArtifactsDir + "Table.SetOutlineBorders.docx");
```

### Смотрите также

* пространство имен [Aspose.Words.Tables](../../aspose.words.tables/)
* сборка [Aspose.Words](../../)
