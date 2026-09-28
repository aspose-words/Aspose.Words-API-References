---
title: "Aspose::Words::WarningType enum"
linktitle: "WarningType"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::WarningType enum. Указывает тип предупреждения, выдаваемого Aspose.Words при загрузке или сохранении документа в C++."
type: docs
weight: 129000
url: /ru/cpp/aspose.words/warningtype/
---
## WarningType enum


Указывает тип предупреждения, выдаваемого Aspose.Words при загрузке или сохранении документа.

```cpp
enum class WarningType
```

### Значения

| Имя | Значение | Описание |
| --- | --- | --- |
| DataLossCategory | 255 | Некоторые текстовые/символьные/изображения или другие данные будут отсутствовать либо в дереве документа после загрузки, либо в созданном документе после сохранения. |
| DataLoss | 1 | Общая потеря данных, без конкретного кода. |
| MajorFormattingLossCategory | 65280 | Полученный документ или конкретное место в нём может выглядеть существенно иначе по сравнению с оригинальным документом. |
| MajorFormattingLoss | 256 | Общая крупная потеря форматирования, без конкретного кода. |
| MinorFormattingLossCategory | 16711680 | Полученный документ или конкретное место в нём может выглядеть несколько иначе по сравнению с оригинальным документом. |
| MinorFormattingLoss | 65536 | Общее небольшое ухудшение форматирования, без конкретного кода. |
| FontSubstitution | 131072 | [Font](../font/) был заменён. |
| FontEmbedding | 262144 | Потеря встроенной информации о шрифте при сохранении документа. |
| UnexpectedContentCategory | 251658240 | Некоторое содержимое исходного документа не удалось распознать (т.е. оно не поддерживается), это может вызвать проблемы или привести к потере данных/форматирования. |
| UnexpectedContent | 16777216 | Общее непредвиденное содержимое, без конкретного кода. |
| Hint | 268435456 | Сообщает о потенциальной проблеме или предлагает улучшение. |


## Примеры



Показывает, как установить свойство для поиска наиболее подходящего шрифта при отсутствии нужного шрифта среди доступных источников шрифтов.
```cpp
// Откройте документ, содержащий текст, отформатированный шрифтом, которого нет ни в одном из наших источников шрифтов.
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Missing font.docx");

// Назначьте обратный вызов для обработки предупреждений о замене шрифтов.
auto warningCollector = System::MakeObject<Aspose::Words::WarningInfoCollection>();
doc->set_WarningCallback(warningCollector);

// Установите имя шрифта по умолчанию и включите замену шрифтов.
auto fontSettings = System::MakeObject<Aspose::Words::Fonts::FontSettings>();
fontSettings->get_SubstitutionSettings()->get_DefaultFontSubstitution()->set_DefaultFontName(u"Arial");
fontSettings->get_SubstitutionSettings()->get_FontInfoSubstitution()->set_Enabled(true);

// После замены шрифтов следует использовать исходные метрики шрифта.
doc->get_LayoutOptions()->set_KeepOriginalFontMetrics(true);

// Мы получим предупреждение о замене шрифта, если сохраним документ с отсутствующим шрифтом.
doc->set_FontSettings(fontSettings);
doc->Save(get_ArtifactsDir() + u"FontSettings.EnableFontSubstitution.pdf");

for (auto&& info : warningCollector)
{
    if (info->get_WarningType() == Aspose::Words::WarningType::FontSubstitution)
    {
        std::cout << info->get_Description() << std::endl;
    }
}
```

## См. также

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
