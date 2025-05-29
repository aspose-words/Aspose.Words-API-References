---
title: ParagraphFormat.SpaceBeforeAuto
linktitle: SpaceBeforeAuto
articleTitle: SpaceBeforeAuto
second_title: Aspose.Words для .NET
description: Откройте для себя свойство ParagraphFormat SpaceBeforeAuto. Автоматически настраивайте интервалы между абзацами для придания документам изысканного и профессионального вида.
type: docs
weight: 340
url: /ru/net/aspose.words/paragraphformat/spacebeforeauto/
---
## ParagraphFormat.SpaceBeforeAuto property

True, если величина интервала перед абзацем устанавливается автоматически.

```csharp
public bool SpaceBeforeAuto { get; set; }
```

## Примечания

При установке на`истинный` , отменяет эффект[`SpaceBefore`](../spacebefore/).

При установке для параметров «Отступ до абзаца» и «Отступ после абзаца» значения «Авто», Microsoft Word автоматически добавляет интервал в 14 пунктов между абзацами в соответствии со следующими правилами:

* Обычно интервал добавляется после всех абзацев.
* В маркированном или нумерованном списке интервал добавляется только после последнего элемента списка. Между элементами списка интервал не добавляется.
* Во вложенном маркированном или нумерованном списке интервал не добавляется.
* После таблицы обычно добавляется пробел.
* Интервал после таблицы не добавляется, если это последний блок в ячейке таблицы.
* После последнего абзаца в ячейке таблицы интервал не добавляется.

## Примеры

Показывает, как установить автоматический интервал между абзацами.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Применить большой интервал до и после абзацев, которые создаст этот конструктор.
builder.ParagraphFormat.SpaceBefore = 24;
builder.ParagraphFormat.SpaceAfter = 24;

// Установите эти флаги на «true», чтобы применить автоматический интервал,
// фактически игнорируя интервал в свойствах, которые мы установили выше.
// Если оставить значение "false", будет применен наш пользовательский интервал между абзацами.
builder.ParagraphFormat.SpaceAfterAuto = autoSpacing;
builder.ParagraphFormat.SpaceBeforeAuto = autoSpacing;

// Вставьте два абзаца с интервалами сверху и снизу и сохраните документ.
builder.Writeln("Paragraph 1.");
builder.Writeln("Paragraph 2.");

doc.Save(ArtifactsDir + "ParagraphFormat.ParagraphSpacingAuto.docx");
```

### Смотрите также

* class [ParagraphFormat](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
