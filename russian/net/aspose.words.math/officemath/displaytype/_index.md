---
title: OfficeMath.DisplayType
second_title: Справочник по API Aspose.Words для .NET
description: OfficeMath свойство. Получает/задает тип формата отображения Office Math который указывает отображается ли уравнение вместе с текстом или отображается на отдельной строке.
type: docs
weight: 10
url: /ru/net/aspose.words.math/officemath/displaytype/
---
## OfficeMath.DisplayType property

Получает/задает тип формата отображения Office Math, который указывает, отображается ли уравнение вместе с текстом или отображается на отдельной строке.

```csharp
public OfficeMathDisplayType DisplayType { get; set; }
```

### Примечания

Тип формата отображения действует только для Office Math верхнего уровня.

Тип возвращаемого формата отображения всегдаInline для вложенных Office Math.

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

* enum [OfficeMathDisplayType](../../officemathdisplaytype/)
* class [OfficeMath](../)
* пространство имен [Aspose.Words.Math](../../officemath/)
* сборка [Aspose.Words](../../../)


