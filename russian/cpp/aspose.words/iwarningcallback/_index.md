---
title: "Aspose::Words::IWarningCallback interface"
linktitle: "IWarningCallback"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::IWarningCallback interface. Реализуйте этот интерфейс, если хотите иметь собственный метод, вызываемый для захвата предупреждений о потере точности, которые могут возникнуть при загрузке или сохранении документа в C++."
type: docs
weight: 80000
url: /ru/cpp/aspose.words/iwarningcallback/
---
## IWarningCallback interface


Реализуйте этот интерфейс, если вы хотите иметь собственный пользовательский метод, вызываемый для захвата предупреждений о потере точности, которые могут возникать при загрузке или сохранении документа.

```cpp
class IWarningCallback : public virtual System::Object
```

## Методы

| Метод | Описание |
| --- | --- |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| static [Type](./type/)() |  |
| virtual [Warning](./warning/)(System::SharedPtr\<Aspose::Words::WarningInfo\>) | Aspose.Words вызывает этот метод, когда сталкивается с проблемой при загрузке или сохранении документа, которая может привести к потере форматирования или точности данных. |

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
