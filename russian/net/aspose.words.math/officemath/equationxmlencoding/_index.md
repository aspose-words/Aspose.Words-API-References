---
title: OfficeMath.EquationXmlEncoding
second_title: Справочник по API Aspose.Words для .NET
description: OfficeMath свойство. Получает/задает кодировку которая использовалась для кодирования XMLуравнения если этот офисный математический объект считывается из XMLуравнения. Мы используем кодировку при сохранении документа для записи в той же кодировке в которой он был прочитан.
type: docs
weight: 20
url: /ru/net/aspose.words.math/officemath/equationxmlencoding/
---
## OfficeMath.EquationXmlEncoding property

Получает/задает кодировку, которая использовалась для кодирования XML-уравнения, если этот офисный математический объект считывается из XML-уравнения. Мы используем кодировку при сохранении документа для записи в той же кодировке, в которой он был прочитан.

```csharp
public Encoding EquationXmlEncoding { get; set; }
```

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

* class [OfficeMath](../)
* пространство имен [Aspose.Words.Math](../../officemath/)
* сборка [Aspose.Words](../../../)


