---
title: OfficeMath.DisplayType
linktitle: DisplayType
articleTitle: DisplayType
second_title: Aspose.Words для .NET
description: OfficeMath DisplayType свойство. Получает/задает тип формата отображения Office Math который определяет отображается ли уравнение в строке с текстом text или отображается в отдельной строке на С#.
type: docs
weight: 10
url: /ru/net/aspose.words.math/officemath/displaytype/
---
## OfficeMath.DisplayType property

Получает/задает тип формата отображения Office Math, который определяет, отображается ли уравнение в строке с текстом text или отображается в отдельной строке.

```csharp
public OfficeMathDisplayType DisplayType { get; set; }
```

## Примечания

Тип формата отображения действует только для Office Math верхнего уровня.

Тип возвращаемого формата отображения всегдаInline для вложенной Office Math.

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

* enum [OfficeMathDisplayType](../../officemathdisplaytype/)
* class [OfficeMath](../)
* пространство имен [Aspose.Words.Math](../../../aspose.words.math/)
* сборка [Aspose.Words](../../../)
