---
title: OfficeMath.ParentParagraph
linktitle: ParentParagraph
articleTitle: ParentParagraph
second_title: Aspose.Words для .NET
description: Откройте для себя свойство OfficeMath ParentParagraph, которое позволяет легко получить доступ к родительскому абзацу любого узла, улучшая форматирование и структуру документа.
type: docs
weight: 50
url: /ru/net/aspose.words.math/officemath/parentparagraph/
---
## OfficeMath.ParentParagraph property

Возвращает родителя[`Paragraph`](../../../aspose.words/paragraph/) этого узла.

```csharp
public Paragraph ParentParagraph { get; }
```

## Примеры

Показывает, как настроить форматирование отображения офисных математических данных.

```csharp
Document doc = new Document(MyDir + "Office math.docx");

OfficeMath officeMath = (OfficeMath)doc.GetChild(NodeType.OfficeMath, 0, true);

// Узлы OfficeMath, являющиеся дочерними узлами других узлов OfficeMath, всегда являются встроенными.
// Узел, с которым мы работаем, является базовым узлом для изменения его местоположения и типа отображения.
Assert.AreEqual(MathObjectType.OMathPara, officeMath.MathObjectType);
Assert.AreEqual(NodeType.OfficeMath, officeMath.NodeType);
Assert.AreEqual(officeMath.ParentNode, officeMath.ParentParagraph);

// Измените местоположение и тип отображения узла OfficeMath.
officeMath.DisplayType = OfficeMathDisplayType.Display;
officeMath.Justification = OfficeMathJustification.Left;

doc.Save(ArtifactsDir + "Shape.OfficeMath.docx");
```

### Смотрите также

* class [Paragraph](../../../aspose.words/paragraph/)
* class [OfficeMath](../)
* пространство имен [Aspose.Words.Math](../../../aspose.words.math/)
* сборка [Aspose.Words](../../../)
