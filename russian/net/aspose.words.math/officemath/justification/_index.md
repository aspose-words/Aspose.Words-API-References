---
title: OfficeMath.Justification
linktitle: Justification
articleTitle: Justification
second_title: Aspose.Words для .NET
description: Откройте для себя свойство OfficeMath Justification, чтобы легко настроить и установить выравнивание Office Math. Улучшите представление вашего документа без усилий!
type: docs
weight: 20
url: /ru/net/aspose.words.math/officemath/justification/
---
## OfficeMath.Justification property

Возвращает/устанавливает выравнивание Office Math.

```csharp
public OfficeMathJustification Justification { get; set; }
```

## Примечания

Выравнивание не может быть установлено в Office Math с типом формата отображенияInline.

Встроенное выравнивание не может быть установлено в Office Math с типом формата отображенияDisplay.

Соответствующий[`DisplayType`](../displaytype/) необходимо настроить до настройки выравнивания Office Math.

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

* enum [OfficeMathJustification](../../officemathjustification/)
* class [OfficeMath](../)
* пространство имен [Aspose.Words.Math](../../../aspose.words.math/)
* сборка [Aspose.Words](../../../)
