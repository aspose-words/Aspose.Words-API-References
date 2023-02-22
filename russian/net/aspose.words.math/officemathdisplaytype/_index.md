---
title: Enum OfficeMathDisplayType
second_title: Справочник по API Aspose.Words для .NET
description: Aspose.Words.Math.OfficeMathDisplayType перечисление. Указывает тип формата отображения уравнения.
type: docs
weight: 3890
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
| Inline | `1` | Office Math отображается вместе с текстом. |

### Примеры

Показывает, как настроить формат отображения математических данных в офисе.

```csharp
Document doc = new Document(MyDir + "Office math.docx");

OfficeMath officeMath = (OfficeMath) doc.GetChild(NodeType.OfficeMath, 0, true);

// Узлы OfficeMath, являющиеся потомками других узлов OfficeMath, всегда являются встроенными.
// Узел, с которым мы работаем, является базовым узлом для изменения его местоположения и типа отображения.
Assert.AreEqual(MathObjectType.OMathPara, officeMath.MathObjectType);
Assert.AreEqual(NodeType.OfficeMath, officeMath.NodeType);
Assert.AreEqual(officeMath.ParentNode, officeMath.ParentParagraph);

// Форматы OOXML и WML используют свойство "EquationXmlEncoding".
Assert.IsNull(officeMath.EquationXmlEncoding);

// Измените расположение и тип отображения узла OfficeMath.
officeMath.DisplayType = OfficeMathDisplayType.Display;
officeMath.Justification = OfficeMathJustification.Left;

doc.Save(ArtifactsDir + "Shape.OfficeMath.docx");
```

### Смотрите также

* пространство имен [Aspose.Words.Math](../../aspose.words.math/)
* сборка [Aspose.Words](../../)


