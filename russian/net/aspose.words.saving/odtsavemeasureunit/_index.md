---
title: OdtSaveMeasureUnit Enum
linktitle: OdtSaveMeasureUnit
articleTitle: OdtSaveMeasureUnit
second_title: Aspose.Words для .NET
description: Откройте для себя перечисление Aspose.Words.OdtSaveMeasureUnit для точного контроля над измерениями документа. Улучшите форматирование документа с легкостью!
type: docs
weight: 6100
url: /ru/net/aspose.words.saving/odtsavemeasureunit/
---
## OdtSaveMeasureUnit enumeration

Указанные единицы измерения, применяемые к измеряемому содержимому документа, такому как форма, ширина и т. д. во время сохранения.

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

* пространство имен [Aspose.Words.Saving](../../aspose.words.saving/)
* сборка [Aspose.Words](../../)
