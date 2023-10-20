---
title: OfficeMathDisplayType Enum
linktitle: OfficeMathDisplayType
articleTitle: OfficeMathDisplayType
second_title: Aspose.Words для .NET
description: Aspose.Words.Math.OfficeMathDisplayType перечисление. Указывает тип формата отображения уравнения на С#.
type: docs
weight: 4130
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
| Display | `0` | Математическая часть Office отображается в отдельной строке. |
| Inline | `1` | Математическая часть Office отображается вместе с текстом. |

## Примеры

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

* пространство имен [Aspose.Words.Math](../../aspose.words.math/)
* сборка [Aspose.Words](../../)
