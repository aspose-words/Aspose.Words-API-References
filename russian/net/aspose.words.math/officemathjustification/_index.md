---
title: OfficeMathJustification Enum
linktitle: OfficeMathJustification
articleTitle: OfficeMathJustification
second_title: Aspose.Words для .NET
description: Aspose.Words.Math.OfficeMathJustification перечисление. Указывает выравнивание уравнения на С#.
type: docs
weight: 4140
url: /ru/net/aspose.words.math/officemathjustification/
---
## OfficeMathJustification enumeration

Указывает выравнивание уравнения.

```csharp
public enum OfficeMathJustification
```

### Ценности

| Имя | Ценность | Описание |
| --- | --- | --- |
| CenterGroup | `1` | Выравнивает экземпляры математического текста слева относительно друг друга и центрирует группу математического текста (математический абзац) относительно страницы. |
| Center | `2` | Центрирует каждый экземпляр математического текста индивидуально относительно полей. |
| Left | `3` | Выравнивание математического абзаца по левому краю. |
| Right | `4` | Правое обоснование математического абзаца. |
| Inline | `7` | Встроенная позиция Math. |
| Default | `1` | Значение по умолчаниюCenterGroup . |

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
