---
title: MeasurementUnits Enum
linktitle: MeasurementUnits
articleTitle: MeasurementUnits
second_title: Aspose.Words для .NET
description: Откройте для себя перечисление Aspose.Words.MeasurementUnits для точного выбора единиц измерения при обработке документов. Улучшите свой рабочий процесс с помощью точных параметров измерения!
type: docs
weight: 4840
url: /ru/net/aspose.words/measurementunits/
---
## MeasurementUnits enumeration

Указывает единицу измерения.

```csharp
public enum MeasurementUnits
```

### Ценности

| Имя | Ценность | Описание |
| --- | --- | --- |
| Inches | `0` | Дюймы. |
| Centimeters | `1` | Сантиметры. |
| Millimeters | `2` | Миллиметры. |
| Points | `3` | Очки. |
| Picas | `4` | Пика (обычно используется в традиционных интервалах шрифтов пишущих машинок). |

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

* пространство имен [Aspose.Words](../../aspose.words/)
* сборка [Aspose.Words](../../)
