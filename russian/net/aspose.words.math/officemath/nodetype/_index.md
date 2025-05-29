---
title: OfficeMath.NodeType
linktitle: NodeType
articleTitle: NodeType
second_title: Aspose.Words для .NET
description: Откройте для себя свойство OfficeMath NodeType, которое эффективно возвращает элементы OfficeMath, расширяя математические возможности вашего документа.
type: docs
weight: 40
url: /ru/net/aspose.words.math/officemath/nodetype/
---
## OfficeMath.NodeType property

ВозвратOfficeMath .

```csharp
public override NodeType NodeType { get; }
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

* enum [NodeType](../../../aspose.words/nodetype/)
* class [OfficeMath](../)
* пространство имен [Aspose.Words.Math](../../../aspose.words.math/)
* сборка [Aspose.Words](../../../)
