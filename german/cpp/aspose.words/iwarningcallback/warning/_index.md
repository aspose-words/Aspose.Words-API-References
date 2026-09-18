---
title: "Aspose::Words::IWarningCallback::Warning Methode"
linktitle: "Warnung"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::IWarningCallback::Warning Methode. Aspose.Words ruft diese Methode auf, wenn ein Problem beim Laden oder Speichern eines Dokuments auftritt, das zu einem Verlust von Formatierung oder Datenintegrität in C++ führen könnte."
type: docs
weight: 4000
url: /de/cpp/aspose.words/iwarningcallback/warning/
---
## IWarningCallback::Warning method


Aspose.Words ruft diese Methode auf, wenn es ein Problem beim Laden oder Speichern von Dokumenten erkennt, das zu einem Verlust von Formatierung oder Daten-Genauigkeit führen könnte.

```cpp
virtual void Aspose::Words::IWarningCallback::Warning(System::SharedPtr<Aspose::Words::WarningInfo> info)=0
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

* Class [WarningInfo](../../warninginfo/)
* Interface [IWarningCallback](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
