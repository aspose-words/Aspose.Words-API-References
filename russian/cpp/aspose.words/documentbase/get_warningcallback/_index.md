---
title: "Aspose::Words::DocumentBase::get_WarningCallback метод"
linktitle: "get_WarningCallback"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::DocumentBase::get_WarningCallback метод. Вызывается во время различных процедур обработки документа, когда обнаруживается проблема, которая может привести к потере данных или точности форматирования в C++."
type: docs
weight: 10000
url: /ru/cpp/aspose.words/documentbase/get_warningcallback/
---
## DocumentBase::get_WarningCallback method


Вызывается во время различных процедур обработки документа, когда обнаруживается проблема, которая может привести к потере точности данных или форматирования.

```cpp
System::SharedPtr<Aspose::Words::IWarningCallback> Aspose::Words::DocumentBase::get_WarningCallback() const
```


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

* Interface [IWarningCallback](../../iwarningcallback/)
* Class [DocumentBase](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
