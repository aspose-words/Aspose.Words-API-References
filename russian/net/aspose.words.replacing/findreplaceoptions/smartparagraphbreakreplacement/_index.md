---
title: FindReplaceOptions.SmartParagraphBreakReplacement
linktitle: SmartParagraphBreakReplacement
articleTitle: SmartParagraphBreakReplacement
second_title: Aspose.Words для .NET
description: Откройте для себя свойство SmartParagraphBreakReplacement в FindReplaceOptions. Легко управляйте разрывами абзацев для бесшовного форматирования текста.
type: docs
weight: 170
url: /ru/net/aspose.words.replacing/findreplaceoptions/smartparagraphbreakreplacement/
---
## FindReplaceOptions.SmartParagraphBreakReplacement property

Возвращает или задает логическое значение, указывающее, разрешено ли заменять абзац break , если нет следующего родственного абзаца.

Значение по умолчанию:`ЛОЖЬ`.

```csharp
public bool SmartParagraphBreakReplacement { get; set; }
```

## Примечания

Эта опция позволяет заменить разрыв абзаца, когда нет следующего родственного абзаца, в который можно переместить все дочерние узлы, путем поиска любого (не обязательно родственного) следующего абзаца после заменяемого абзаца.

## Примеры

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
// Если для следующего параметра установлено значение «true», Aspose.Words удалит текст абзаца
// полностью с его знаком абзаца. В противном случае Aspose.Words будет имитировать Word и удалять
// только текст абзаца и оставляет знак абзаца нетронутым (когда таблица следует за текстом).
options.SmartParagraphBreakReplacement = isSmartParagraphBreakReplacement;
doc.Range.Replace(new Regex(@"TEXT1&p"), "", options);

doc.Save(ArtifactsDir + "Table.RemoveParagraphTextAndMark.docx");
```

### Смотрите также

* class [FindReplaceOptions](../)
* пространство имен [Aspose.Words.Replacing](../../../aspose.words.replacing/)
* сборка [Aspose.Words](../../../)
