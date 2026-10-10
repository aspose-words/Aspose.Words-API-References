---
title: "Aspose::Words::Layout::LayoutOptions::get_KeepOriginalFontMetrics Methode"
linktitle: "get_KeepOriginalFontMetrics"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Layout::LayoutOptions::get_KeepOriginalFontMetrics Methode. Ruft eine Angabe ab oder legt sie fest, ob die ursprünglichen Schriftmetriken nach einer Schriftartsubstitution verwendet werden sollen. Der Standardwert ist true in C++."
type: docs
weight: 6500
url: /de/cpp/aspose.words.layout/layoutoptions/get_keeporiginalfontmetrics/
---
## LayoutOptions::get_KeepOriginalFontMetrics method


Liest oder schreibt die Angabe, ob nach einer Schriftart‑Ersetzung die ursprünglichen Schriftmetriken verwendet werden sollen. Der Standardwert ist **true**.

```cpp
bool Aspose::Words::Layout::LayoutOptions::get_KeepOriginalFontMetrics() const
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

* Class [LayoutOptions](../)
* Namespace [Aspose::Words::Layout](../../)
* Library [Aspose.Words for C++](../../../)
