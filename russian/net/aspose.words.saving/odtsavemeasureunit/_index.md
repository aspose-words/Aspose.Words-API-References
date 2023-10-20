---
title: OdtSaveMeasureUnit Enum
linktitle: OdtSaveMeasureUnit
articleTitle: OdtSaveMeasureUnit
second_title: Aspose.Words для .NET
description: Aspose.Words.Saving.OdtSaveMeasureUnit перечисление. Указанные единицы измерения применяемые к измеряемому содержимому документа например форме ширине и т. д. во время сохранения на С#.
type: docs
weight: 5320
url: /ru/net/aspose.words.saving/odtsavemeasureunit/
---
## OdtSaveMeasureUnit enumeration

Указанные единицы измерения, применяемые к измеряемому содержимому документа, например форме, ширине и т. д. во время сохранения.

```csharp
public enum OdtSaveMeasureUnit
```

### Ценности

| Имя | Ценность | Описание |
| --- | --- | --- |
| Centimeters | `0` | Указывает, что содержимое документа сохраняется в сантиметрах. |
| Inches | `1` | Указывает, что содержимое документа сохраняется в дюймах. |

## Примеры

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

* пространство имен [Aspose.Words.Saving](../../aspose.words.saving/)
* сборка [Aspose.Words](../../)
