---
title: RevisionOptions.MeasurementUnit
linktitle: MeasurementUnit
articleTitle: MeasurementUnit
second_title: Aspose.Words для .NET
description: Настройте комментарии к ревизии с помощью свойства RevisionOptions MeasurementUnit. Легко устанавливайте единицы измерения, по умолчанию используются сантиметры.
type: docs
weight: 80
url: /ru/net/aspose.words.layout/revisionoptions/measurementunit/
---
## RevisionOptions.MeasurementUnit property

Позволяет указать единицы измерения для комментариев к ревизии. Значение по умолчанию:Centimeters

```csharp
public MeasurementUnits MeasurementUnit { get; set; }
```

## Примеры

Показывает, как привести сохраненный документ в соответствие со старой схемой ODT.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

OdtSaveOptions saveOptions = new OdtSaveOptions
{
    MeasureUnit = OdtSaveMeasureUnit.Centimeters,
    IsStrictSchema11 = exportToOdt11Specs
};

doc.Save(ArtifactsDir + "OdtSaveOptions.Odt11Schema.odt", saveOptions);
```

### Смотрите также

* enum [MeasurementUnits](../../../aspose.words/measurementunits/)
* class [RevisionOptions](../)
* пространство имен [Aspose.Words.Layout](../../../aspose.words.layout/)
* сборка [Aspose.Words](../../../)
