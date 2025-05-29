---
title: OdtSaveOptions.IsStrictSchema11
linktitle: IsStrictSchema11
articleTitle: IsStrictSchema11
second_title: Aspose.Words для .NET
description: Оптимизируйте экспорт ODT с помощью свойства IsStrictSchema11. Обеспечьте строгое соответствие ODT 1.1 или включите совместимость с 1.2 для достижения наилучших результатов.
type: docs
weight: 30
url: /ru/net/aspose.words.saving/odtsaveoptions/isstrictschema11/
---
## OdtSaveOptions.IsStrictSchema11 property

Указывает, должен ли экспорт строго соответствовать спецификации ODT 1.1. OOo 3.0 корректно отображает файлы, содержащие элементы и атрибуты ODT 1.2. Для этой цели используйте «false» или «true» для строгого соответствия спецификации 1.1. Значение по умолчанию:`ЛОЖЬ` .

```csharp
public bool IsStrictSchema11 { get; set; }
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

* class [OdtSaveOptions](../)
* пространство имен [Aspose.Words.Saving](../../../aspose.words.saving/)
* сборка [Aspose.Words](../../../)
