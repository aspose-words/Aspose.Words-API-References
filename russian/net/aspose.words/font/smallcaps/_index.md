---
title: Font.SmallCaps
linktitle: SmallCaps
articleTitle: SmallCaps
second_title: Aspose.Words для .NET
description: Откройте для себя свойство Font SmallCaps. Легко форматируйте текст маленькими заглавными буквами для улучшения читаемости и стильного вида ваших дизайнов.
type: docs
weight: 370
url: /ru/net/aspose.words/font/smallcaps/
---
## Font.SmallCaps property

True, если шрифт отформатирован как маленькие заглавные буквы.

```csharp
public bool SmallCaps { get; set; }
```

## Примеры

Показывает, как отформатировать запуск, чтобы его содержимое отображалось заглавными буквами.

```csharp
Document doc = new Document();
Paragraph para = (Paragraph)doc.GetChild(NodeType.Paragraph, 0, true);

// Есть два способа заставить run отображать строчный текст заглавным, не меняя содержимое.
// 1 - Установите флаг AllCaps, чтобы отображать все символы обычными заглавными буквами:
Run run = new Run(doc, "all capitals");
run.Font.AllCaps = true;
para.AppendChild(run);

para = (Paragraph)para.ParentNode.AppendChild(new Paragraph(doc));

// 2 - Установите флаг SmallCaps, чтобы отображать все символы заглавными буквами:
// Если символ строчный, он будет отображаться в верхнем регистре
// но будет иметь ту же высоту, что и строчные буквы (x-высота шрифта).
// Символы, которые изначально были в верхнем регистре, будут выглядеть так же.
run = new Run(doc, "Small Capitals");
run.Font.SmallCaps = true;
para.AppendChild(run);

doc.Save(ArtifactsDir + "Font.Caps.docx");
```

### Смотрите также

* class [Font](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
