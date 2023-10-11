---
title: LoadOptions.ConvertShapeToOfficeMath
second_title: Справочник по API Aspose.Words для .NET
description: LoadOptions свойство. Получает или задает необходимость преобразования фигур с помощью EquationXML в объекты Office Math.
type: docs
weight: 40
url: /ru/net/aspose.words.loading/loadoptions/convertshapetoofficemath/
---
## LoadOptions.ConvertShapeToOfficeMath property

Получает или задает необходимость преобразования фигур с помощью EquationXML в объекты Office Math.

```csharp
public bool ConvertShapeToOfficeMath { get; set; }
```

### Примеры

Показывает, как преобразовать фигуры EquationXML в объекты Office Math.

```csharp
LoadOptions loadOptions = new LoadOptions();

// Используйте этот флаг, чтобы указать, следует ли преобразовывать фигуры с атрибутами EquationXML
// к объектам Office Math и затем загружаем документ.
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
* пространство имен [Aspose.Words.Loading](../../loadoptions/)
* сборка [Aspose.Words](../../../)


