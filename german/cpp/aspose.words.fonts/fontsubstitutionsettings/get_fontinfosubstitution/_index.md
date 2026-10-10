---
title: "Aspose::Words::Fonts::FontSubstitutionSettings::get_FontInfoSubstitution Methode"
linktitle: "get_FontInfoSubstitution"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Fonts::FontSubstitutionSettings::get_FontInfoSubstitution Methode. Einstellungen, die mit der Schriftartinfo-Substitutionsregel in C++ zusammenhängen."
type: docs
weight: 4000
url: /de/cpp/aspose.words.fonts/fontsubstitutionsettings/get_fontinfosubstitution/
---
## FontSubstitutionSettings::get_FontInfoSubstitution method


[Settings](../../../aspose.words.settings/) related to font info substitution rule.

```cpp
const System::SharedPtr<Aspose::Words::Fonts::FontInfoSubstitutionRule> & Aspose::Words::Fonts::FontSubstitutionSettings::get_FontInfoSubstitution() const
```


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

* Class [FontInfoSubstitutionRule](../../fontinfosubstitutionrule/)
* Class [FontSubstitutionSettings](../)
* Namespace [Aspose::Words::Fonts](../../)
* Library [Aspose.Words for C++](../../../)
