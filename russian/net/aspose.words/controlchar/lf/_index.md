---
title: ControlChar.Lf
linktitle: Lf
articleTitle: Lf
second_title: Aspose.Words для .NET
description: Откройте для себя ControlChar Lf, основной символ перевода строки (x000a) для бесшовного форматирования текста. Повысьте эффективность кодирования сегодня!
type: docs
weight: 110
url: /ru/net/aspose.words/controlchar/lf/
---
## ControlChar.Lf field

Символ перевода строки: "\x000a" или "\n". То же, что и[`LineFeed`](../linefeed/) .

```csharp
public static readonly string Lf;
```

## Примеры

Показывает, как добавлять в документ различные управляющие символы.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Добавьте обычный пробел.
builder.Write("Before space." + ControlChar.SpaceChar + "After space.");

// Добавьте NBSP, который является неразрывным пробелом.
// В отличие от обычного пробела, этот пробел не может иметь автоматический перенос строки в своей позиции.
builder.Write("Before space." + ControlChar.NonBreakingSpace + "After space.");

// Добавьте символ табуляции.
builder.Write("Before tab." + ControlChar.Tab + "After tab.");

// Добавить перенос строки.
builder.Write("Before line break." + ControlChar.LineBreak + "After line break.");

// Добавить новую строку и начать новый абзац.
Assert.AreEqual(1, doc.FirstSection.Body.GetChildNodes(NodeType.Paragraph, true).Count);
builder.Write("Before line feed." + ControlChar.LineFeed + "After line feed.");
Assert.AreEqual(2, doc.FirstSection.Body.GetChildNodes(NodeType.Paragraph, true).Count);

// Символ перевода строки имеет две версии.
Assert.AreEqual(ControlChar.LineFeed, ControlChar.Lf);

// Возврат каретки и перевод строки могут быть представлены вместе одним символом.
Assert.AreEqual(ControlChar.CrLf, ControlChar.Cr + ControlChar.Lf);

// Добавить разрыв абзаца, который начнет новый абзац.
builder.Write("Before paragraph break." + ControlChar.ParagraphBreak + "After paragraph break.");
Assert.AreEqual(3, doc.FirstSection.Body.GetChildNodes(NodeType.Paragraph, true).Count);

// Добавить разрыв раздела. Это не создает новый раздел или абзац.
Assert.AreEqual(1, doc.Sections.Count);
builder.Write("Before section break." + ControlChar.SectionBreak + "After section break.");
Assert.AreEqual(1, doc.Sections.Count);

// Добавить разрыв страницы.
builder.Write("Before page break." + ControlChar.PageBreak + "After page break.");

// Разрыв страницы имеет то же значение, что и разрыв раздела.
Assert.AreEqual(ControlChar.PageBreak, ControlChar.SectionBreak);

// Вставьте новый раздел, а затем установите количество столбцов равным двум.
doc.AppendChild(new Section(doc));
builder.MoveToSection(1);
builder.CurrentSection.PageSetup.TextColumns.SetCount(2);

// Мы можем использовать управляющий символ, чтобы отметить точку, в которой текст переходит в следующий столбец.
builder.Write("Text at end of column 1." + ControlChar.ColumnBreak + "Text at beginning of column 2.");

doc.Save(ArtifactsDir + "ControlChar.InsertControlChars.docx");

// Для большинства символов существуют символьные и строковые аналоги.
Assert.AreEqual(Convert.ToChar(ControlChar.Cell), ControlChar.CellChar);
Assert.AreEqual(Convert.ToChar(ControlChar.NonBreakingSpace), ControlChar.NonBreakingSpaceChar);
Assert.AreEqual(Convert.ToChar(ControlChar.Tab), ControlChar.TabChar);
Assert.AreEqual(Convert.ToChar(ControlChar.LineBreak), ControlChar.LineBreakChar);
Assert.AreEqual(Convert.ToChar(ControlChar.LineFeed), ControlChar.LineFeedChar);
Assert.AreEqual(Convert.ToChar(ControlChar.ParagraphBreak), ControlChar.ParagraphBreakChar);
Assert.AreEqual(Convert.ToChar(ControlChar.SectionBreak), ControlChar.SectionBreakChar);
Assert.AreEqual(Convert.ToChar(ControlChar.PageBreak), ControlChar.SectionBreakChar);
Assert.AreEqual(Convert.ToChar(ControlChar.ColumnBreak), ControlChar.ColumnBreakChar);
```

### Смотрите также

* class [ControlChar](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
