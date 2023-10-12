---
title: FindReplaceOptions.SmartParagraphBreakReplacement
second_title: Справочник по API Aspose.Words для .NET
description: FindReplaceOptions свойство. Получает или задает логическое значение указывающее разрешено ли заменять абзацbreak  если нет следующего одноуровневого абзаца.
type: docs
weight: 160
url: /ru/net/aspose.words.replacing/findreplaceoptions/smartparagraphbreakreplacement/
---
## FindReplaceOptions.SmartParagraphBreakReplacement property

Получает или задает логическое значение, указывающее, разрешено ли заменять абзацbreak , если нет следующего одноуровневого абзаца.

Значение по умолчанию:`ЛОЖЬ`.

```csharp
public bool SmartParagraphBreakReplacement { get; set; }
```

### Примечания

Эта опция позволяет заменить разрыв абзаца, когда нет следующего одноуровневого абзаца, в который можно переместить все дочерние узлы child , путем нахождения любого (не обязательно родственного) следующего абзаца после заменяемого абзаца.

### Примеры

Показывает, как удалить абзац из ячейки таблицы с вложенной таблицей.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Создать таблицу с абзацем и внутренней таблицей в первой ячейке.
builder.StartTable();
builder.InsertCell();
builder.Write("TEXT1");
builder.StartTable();
builder.InsertCell();
builder.EndTable();
builder.EndTable();
builder.Writeln();

FindReplaceOptions options = new FindReplaceOptions();
// Если для следующей опции установлено значение «true», Aspose.Words удалит текст абзаца
// полностью со знаком абзаца. В противном случае Aspose.Words будет имитировать Word и удалять
// только текст абзаца и оставляет знак абзаца нетронутым (когда за текстом следует таблица).
options.SmartParagraphBreakReplacement = isSmartParagraphBreakReplacement;
doc.Range.Replace(new Regex(@"TEXT1&p"), "", options);

doc.Save(ArtifactsDir + "Table.RemoveParagraphTextAndMark.docx");
```

### Смотрите также

* class [FindReplaceOptions](../)
* пространство имен [Aspose.Words.Replacing](../../findreplaceoptions/)
* сборка [Aspose.Words](../../../)


