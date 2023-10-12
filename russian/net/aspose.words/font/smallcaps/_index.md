---
title: Font.SmallCaps
second_title: Справочник по API Aspose.Words для .NET
description: Font свойство. True если шрифт отформатирован как маленькие заглавные буквы.
type: docs
weight: 360
url: /ru/net/aspose.words/font/smallcaps/
---
## Font.SmallCaps property

True, если шрифт отформатирован как маленькие заглавные буквы.

```csharp
public bool SmallCaps { get; set; }
```

### Примеры

Показывает, как отформатировать прогон для отображения его содержимого заглавными буквами.

```csharp
Document doc = new Document();
Paragraph para = (Paragraph)doc.GetChild(NodeType.Paragraph, 0, true);

// Есть два способа заставить прогон отображать строчный текст в верхнем регистре без изменения содержимого.
// 1 — установите флаг AllCaps для отображения всех символов обычными заглавными буквами:
Run run = new Run(doc, "all capitals");
run.Font.AllCaps = true;
para.AppendChild(run);

para = (Paragraph)para.ParentNode.AppendChild(new Paragraph(doc));

// 2 - Установите флаг SmallCaps для отображения всех символов маленькими заглавными буквами:
// Если символ в нижнем регистре, он появится в верхнем регистре
// но будет иметь ту же высоту, что и строчные буквы (высота шрифта по оси x).
// Символы, которые изначально были в верхнем регистре, будут выглядеть так же.
run = new Run(doc, "Small Capitals");
run.Font.SmallCaps = true;
para.AppendChild(run);

doc.Save(ArtifactsDir + "Font.Caps.docx");
```

### Смотрите также

* class [Font](../)
* пространство имен [Aspose.Words](../../font/)
* сборка [Aspose.Words](../../../)


