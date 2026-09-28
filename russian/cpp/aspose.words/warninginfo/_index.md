---
title: "Класс Aspose::Words::WarningInfo"
linktitle: "WarningInfo"
second_title: "Справочник API Aspose.Words для C++"
description: "Класс Aspose::Words::WarningInfo. Содержит информацию о предупреждении, выданном Aspose.Words во время загрузки или сохранения документа. Чтобы узнать больше, посетите статью документации на C++."
type: docs
weight: 74000
url: /ru/cpp/aspose.words/warninginfo/
---
## WarningInfo class


Содержит информацию о предупреждении, выданном Aspose.Words во время загрузки или сохранения документа. Чтобы узнать больше, посетите статью документации [Programming with Documents](https://docs.aspose.com/words/cpp/programming-with-documents/).

```cpp
class WarningInfo : public System::Object
```

## Методы

| Метод | Описание |
| --- | --- |
| [get_Description](./get_description/)() const | Возвращает описание предупреждения. |
| [get_Source](./get_source/)() const | Возвращает источник предупреждения. |
| [get_WarningType](./get_warningtype/)() const | Возвращает тип предупреждения. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| static [Type](./type/)() |  |
## Примечания


Вы не создаёте экземпляры этого класса. Объекты этого класса создаются и передаются Aspose.Words в метод [Warning()](../iwarningcallback/warning/).

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
