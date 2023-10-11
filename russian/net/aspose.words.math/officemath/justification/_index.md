---
title: OfficeMath.Justification
second_title: Справочник по API Aspose.Words для .NET
description: OfficeMath свойство. Получает/устанавливает выравнивание Office Math.
type: docs
weight: 20
url: /ru/net/aspose.words.math/officemath/justification/
---
## OfficeMath.Justification property

Получает/устанавливает выравнивание Office Math.

```csharp
public OfficeMathJustification Justification { get; set; }
```

### Примечания

Для выравнивания нельзя установить Office Math с типом формата отображения.Inline.

Встроенное выравнивание не может быть установлено для Office Math с типом формата отображения.Display.

Соответствующий[`DisplayType`](../displaytype/) необходимо установить перед настройкой выравнивания Office Math.

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

* enum [OfficeMathJustification](../../officemathjustification/)
* class [OfficeMath](../)
* пространство имен [Aspose.Words.Math](../../officemath/)
* сборка [Aspose.Words](../../../)


