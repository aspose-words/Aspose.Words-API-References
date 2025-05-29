---
title: OdtSaveOptions.MeasureUnit
linktitle: MeasureUnit
articleTitle: MeasureUnit
second_title: Aspose.Words для .NET
description: Настройте MeasureUnit вашего документа с помощью OdtSaveOptions. Выберите предпочитаемые единицы измерения для точности — по умолчанию это сантиметры.
type: docs
weight: 40
url: /ru/net/aspose.words.saving/odtsaveoptions/measureunit/
---
## OdtSaveOptions.MeasureUnit property

Позволяет указать единицы измерения, применяемые к содержимому документа. Значение по умолчанию:Centimeters

```csharp
public OdtSaveMeasureUnit MeasureUnit { get; set; }
```

## Примечания

Open Office использует сантиметры при указании длины, ширины и других измеряемых форматов и свойств содержимого в документах, тогда как MS Office использует дюймы.

## Примеры

Показывает, как использовать различные единицы измерения для определения параметров стиля сохраненного документа ODT.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

// При экспорте документа в формат .odt мы можем использовать объект OdtSaveOptions, чтобы изменить способ сохранения документа.
// Мы можем установить свойство "MeasureUnit" на "OdtSaveMeasureUnit.Centimeters"
 // для определения содержимого, такого как параметры стиля, с использованием метрической системы, используемой Open Office.
// Мы можем установить свойство "MeasureUnit" на "OdtSaveMeasureUnit.Inches"
// для определения содержимого, такого как параметры стиля, с использованием имперской системы, используемой в Microsoft Word.
OdtSaveOptions saveOptions = new OdtSaveOptions
{
    MeasureUnit = odtSaveMeasureUnit
};

doc.Save(ArtifactsDir + "OdtSaveOptions.Odt11Schema.odt", saveOptions);
```

### Смотрите также

* enum [OdtSaveMeasureUnit](../../odtsavemeasureunit/)
* class [OdtSaveOptions](../)
* пространство имен [Aspose.Words.Saving](../../../aspose.words.saving/)
* сборка [Aspose.Words](../../../)
