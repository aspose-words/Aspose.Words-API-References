---
title: OfficeMathDisplayType Enum
linktitle: OfficeMathDisplayType
articleTitle: OfficeMathDisplayType
second_title: Aspose.Words для .NET
description: Откройте для себя перечисление Aspose.Words.Math.OfficeMathDisplayType, чтобы легко настраивать форматы отображения уравнений для повышения ясности и наглядности документа.
type: docs
weight: 4820
url: /ru/net/aspose.words.math/officemathdisplaytype/
---
## OfficeMathDisplayType enumeration

Указывает тип формата отображения уравнения.

```csharp
public enum OfficeMathDisplayType
```

### Ценности

| Имя | Ценность | Описание |
| --- | --- | --- |
| Display | `0` | Office Math отображается в отдельной строке. |
| Inline | `1` | Office Math отображается в строке с текстом. |

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

* пространство имен [Aspose.Words.Math](../../aspose.words.math/)
* сборка [Aspose.Words](../../)
