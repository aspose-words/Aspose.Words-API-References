---
title: ParagraphFormat.SpaceAfterAuto
second_title: Справочник по API Aspose.Words для .NET
description: ParagraphFormat свойство. True если интервал после абзаца устанавливается автоматически.
type: docs
weight: 310
url: /ru/net/aspose.words/paragraphformat/spaceafterauto/
---
## ParagraphFormat.SpaceAfterAuto property

True, если интервал после абзаца устанавливается автоматически.

```csharp
public bool SpaceAfterAuto { get; set; }
```

### Примечания

Если установлено значение`истинный` , переопределяет эффект[`SpaceAfter`](../spaceafter/).

Если для абзаца «Отступ до» и «Отступ после» установлено значение «Авто», Microsoft Word автоматически добавляет 14 пунктов между абзацами в соответствии со следующими правилами:

* Обычно интервал добавляется после всех абзацев.
* В маркированном или нумерованном списке интервал добавляется только после последнего элемента списка. Интервал между элементами списка не добавляется.
* Во вложенных маркированных или нумерованных списках интервалы не добавляются.
* Обычно после таблицы добавляется пробел.
* Пробел не добавляется после таблицы, если это последний блок в ячейке таблицы.
* Интервал не добавляется после последнего абзаца в ячейке таблицы.

### Примеры

Показывает, как установить автоматический интервал между абзацами.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Примените большой интервал до и после абзацев, которые создаст этот конструктор.
builder.ParagraphFormat.SpaceBefore = 24;
builder.ParagraphFormat.SpaceAfter = 24;

// Установите для этих флагов значение «true», чтобы применить автоматический интервал,
// эффективно игнорируем интервал в свойствах, которые мы установили выше.
// Оставьте их значение «false», и будет применен наш собственный интервал между абзацами.
builder.ParagraphFormat.SpaceAfterAuto = autoSpacing;
builder.ParagraphFormat.SpaceBeforeAuto = autoSpacing;

// Вставьте два абзаца с интервалом выше и ниже и сохраните документ.
builder.Writeln("Paragraph 1.");
builder.Writeln("Paragraph 2.");

doc.Save(ArtifactsDir + "ParagraphFormat.ParagraphSpacingAuto.docx");
```

### Смотрите также

* class [ParagraphFormat](../)
* пространство имен [Aspose.Words](../../paragraphformat/)
* сборка [Aspose.Words](../../../)


