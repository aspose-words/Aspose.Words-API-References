---
title: OfficeMathJustification Enum
linktitle: OfficeMathJustification
articleTitle: OfficeMathJustification
second_title: Aspose.Words для .NET
description: Откройте для себя перечисление Aspose.Words.Math.OfficeMathJustification для точного выравнивания уравнений. Улучшите ясность вашего документа с помощью оптимальных вариантов выравнивания.
type: docs
weight: 4830
url: /ru/net/aspose.words.math/officemathjustification/
---
## OfficeMathJustification enumeration

Указывает обоснование уравнения.

```csharp
public enum OfficeMathJustification
```

### Ценности

| Имя | Ценность | Описание |
| --- | --- | --- |
| CenterGroup | `1` | Выравнивает экземпляры математического текста по левому краю относительно друг друга и центрирует группу математического текста (Математический абзац) относительно страницы. |
| Center | `2` | Центрирует каждый экземпляр математического текста индивидуально относительно полей. |
| Left | `3` | Выравнивание математического абзаца влево. |
| Right | `4` | Правое выравнивание математического абзаца. |
| Inline | `7` | Встроенная позиция Math. |
| Default | `1` | Значение по умолчаниюCenterGroup . |

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
