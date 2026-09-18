---
title: "Aspose::Words::WarningInfo Klasse"
linktitle: "WarningInfo"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::WarningInfo Klasse. Enthält Informationen über eine Warnung, die Aspose.Words beim Laden oder Speichern eines Dokuments ausgegeben hat. Weitere Informationen finden Sie im Dokumentationsartikel für C++."
type: docs
weight: 74000
url: /de/cpp/aspose.words/warninginfo/
---
## WarningInfo class


Enthält Informationen über eine Warnung, die Aspose.Words beim Laden oder Speichern eines Dokuments ausgegeben hat. Weitere Informationen finden Sie im Dokumentationsartikel [Programming with Documents](https://docs.aspose.com/words/cpp/programming-with-documents/).

```cpp
class WarningInfo : public System::Object
```

## Methoden

| Methode | Beschreibung |
| --- | --- |
| [get_Description](./get_description/)() const | Gibt die Beschreibung der Warnung zurück. |
| [get_Source](./get_source/)() const | Gibt die Quelle der Warnung zurück. |
| [get_WarningType](./get_warningtype/)() const | Gibt den Typ der Warnung zurück. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| static [Type](./type/)() |  |
## Hinweise


Sie erstellen keine Instanzen dieser Klasse. Objekte dieser Klasse werden von Aspose.Words erstellt und an die Methode [Warning()](../iwarningcallback/warning/) übergeben.

## Beispiele



Zeigt, wie die Eigenschaft eingestellt wird, um die nächstbeste Übereinstimmung für eine fehlende Schriftart aus den verfügbaren Schriftquellen zu finden.
```cpp
// Öffnen Sie ein Dokument, das Text enthält, der mit einer Schriftart formatiert ist, die in keiner unserer Schriftquellen existiert.
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Missing font.docx");

// Weisen Sie einen Callback zu, um Warnungen zur Schriftart-Substitution zu behandeln.
auto warningCollector = System::MakeObject<Aspose::Words::WarningInfoCollection>();
doc->set_WarningCallback(warningCollector);

// Legen Sie einen Standard-Schriftartnamen fest und aktivieren Sie die Schriftart-Substitution.
auto fontSettings = System::MakeObject<Aspose::Words::Fonts::FontSettings>();
fontSettings->get_SubstitutionSettings()->get_DefaultFontSubstitution()->set_DefaultFontName(u"Arial");
fontSettings->get_SubstitutionSettings()->get_FontInfoSubstitution()->set_Enabled(true);

// Ursprüngliche Schriftmetriken sollten nach der Schriftart-Substitution verwendet werden.
doc->get_LayoutOptions()->set_KeepOriginalFontMetrics(true);

// Wir erhalten eine Schriftart-Substitutionswarnung, wenn wir ein Dokument mit einer fehlenden Schriftart speichern.
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

## Siehe auch

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
