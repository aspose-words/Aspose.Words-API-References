---
title: OfficeMath.ParentParagraph
second_title: Справочник по API Aspose.Words для .NET
description: OfficeMath свойство. Получает родительский элементParagraph этого узла.
type: docs
weight: 50
url: /ru/net/aspose.words.math/officemath/parentparagraph/
---
## OfficeMath.ParentParagraph property

Получает родительский элемент[`Paragraph`](../../../aspose.words/paragraph/) этого узла.

```csharp
public Paragraph ParentParagraph { get; }
```

### Примеры

Показывает, как настроить форматирование отображения математических функций Office.

```csharp
Document doc = new Document(MyDir + "Office math.docx");

OfficeMath officeMath = (OfficeMath) doc.GetChild(NodeType.OfficeMath, 0, true);

// Узлы OfficeMath, являющиеся дочерними по отношению к другим узлам OfficeMath, всегда являются встроенными.
// Узел, с которым мы работаем, является базовым узлом для изменения его местоположения и типа отображения.
Assert.AreEqual(MathObjectType.OMathPara, officeMath.MathObjectType);
Assert.AreEqual(NodeType.OfficeMath, officeMath.NodeType);
Assert.AreEqual(officeMath.ParentNode, officeMath.ParentParagraph);

// Изменяем расположение и тип отображения узла OfficeMath.
officeMath.DisplayType = OfficeMathDisplayType.Display;
officeMath.Justification = OfficeMathJustification.Left;

doc.Save(ArtifactsDir + "Shape.OfficeMath.docx");
```

### Смотрите также

* class [Paragraph](../../../aspose.words/paragraph/)
* class [OfficeMath](../)
* пространство имен [Aspose.Words.Math](../../officemath/)
* сборка [Aspose.Words](../../../)


