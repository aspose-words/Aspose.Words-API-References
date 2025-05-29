---
title: LoadOptions.ConvertShapeToOfficeMath
linktitle: ConvertShapeToOfficeMath
articleTitle: ConvertShapeToOfficeMath
second_title: Aspose.Words для .NET
description: Преобразуйте фигуры с EquationXML в объекты Office Math без особых усилий, используя свойство ConvertShapeToOfficeMath в LoadOptions для повышения ясности документа.
type: docs
weight: 40
url: /ru/net/aspose.words.loading/loadoptions/convertshapetoofficemath/
---
## LoadOptions.ConvertShapeToOfficeMath property

Возвращает или задает, следует ли преобразовывать фигуры с EquationXML в объекты Office Math.

```csharp
public bool ConvertShapeToOfficeMath { get; set; }
```

## Примеры

Показывает, как преобразовывать фигуры EquationXML в объекты Office Math.

```csharp
LoadOptions loadOptions = new LoadOptions();

// Используйте этот флаг, чтобы указать, следует ли преобразовывать фигуры с атрибутами EquationXML
// в объекты Office Math, а затем загрузить документ.
loadOptions.ConvertShapeToOfficeMath = isConvertShapeToOfficeMath;

Document doc = new Document(MyDir + "Math shapes.docx", loadOptions);

if (isConvertShapeToOfficeMath)
{
    Assert.AreEqual(16, doc.GetChildNodes(NodeType.Shape, true).Count);
    Assert.AreEqual(34, doc.GetChildNodes(NodeType.OfficeMath, true).Count);
}
else
{
    Assert.AreEqual(24, doc.GetChildNodes(NodeType.Shape, true).Count);
    Assert.AreEqual(0, doc.GetChildNodes(NodeType.OfficeMath, true).Count);
}
```

### Смотрите также

* class [LoadOptions](../)
* пространство имен [Aspose.Words.Loading](../../../aspose.words.loading/)
* сборка [Aspose.Words](../../../)
