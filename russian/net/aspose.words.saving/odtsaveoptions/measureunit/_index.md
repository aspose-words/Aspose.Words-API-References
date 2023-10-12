---
title: OdtSaveOptions.MeasureUnit
second_title: Справочник по API Aspose.Words для .NET
description: OdtSaveOptions свойство. Позволяет указать единицы измерения применяемые к содержимому документа. Значение по умолчаниюCentimeters
type: docs
weight: 30
url: /ru/net/aspose.words.saving/odtsaveoptions/measureunit/
---
## OdtSaveOptions.MeasureUnit property

Позволяет указать единицы измерения, применяемые к содержимому документа. Значение по умолчанию:Centimeters

```csharp
public OdtSaveMeasureUnit MeasureUnit { get; set; }
```

### Примечания

Open Office использует сантиметры при указании длины, ширины и других измеряемых свойств форматирования и свойств содержимого в документах, тогда как MS Office использует дюймы.

### Примеры

Показывает, как использовать различные единицы измерения для определения параметров стиля сохраненного документа ODT.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

// Когда мы экспортируем документ в .odt, мы можем использовать объект OdtSaveOptions, чтобы изменить способ сохранения документа.
// Мы можем установить для свойства "MeasureUnit" значение "OdtSaveMeasureUnit.Centimeters"
 // для определения содержимого, такого как параметры стиля, с использованием метрической системы, которую использует Open Office.
// Мы можем установить для свойства "MeasureUnit" значение "OdtSaveMeasureUnit.Inches"
// для определения содержимого, такого как параметры стиля, с использованием британской системы мер, которую использует Microsoft Word.
OdtSaveOptions saveOptions = new OdtSaveOptions
{
    MeasureUnit = odtSaveMeasureUnit
};

doc.Save(ArtifactsDir + "OdtSaveOptions.Odt11Schema.odt", saveOptions);
```

### Смотрите также

* enum [OdtSaveMeasureUnit](../../odtsavemeasureunit/)
* class [OdtSaveOptions](../)
* пространство имен [Aspose.Words.Saving](../../odtsaveoptions/)
* сборка [Aspose.Words](../../../)


