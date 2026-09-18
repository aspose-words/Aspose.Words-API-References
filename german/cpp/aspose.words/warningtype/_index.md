---
title: "Aspose::Words::WarningType Enum"
linktitle: "WarningType"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::WarningType Enum. Gibt den Typ einer Warnung an, die von Aspose.Words beim Laden oder Speichern eines Dokuments in C++ ausgegeben wird."
type: docs
weight: 129000
url: /de/cpp/aspose.words/warningtype/
---
## WarningType enum


Gibt den Typ einer Warnung an, die von Aspose.Words beim Laden oder Speichern eines Dokuments ausgegeben wird.

```cpp
enum class WarningType
```

### Werte

| Name | Wert | Beschreibung |
| --- | --- | --- |
| DataLossCategory | 255 | Einige Texte/Zeichen/Bilder oder andere Daten fehlen entweder im Dokumentbaum nach dem Laden oder im erstellten Dokument nach dem Speichern. |
| DataLoss | 1 | Allgemeiner Datenverlust, kein spezifischer Code. |
| MajorFormattingLossCategory | 65280 | Das resultierende Dokument oder ein bestimmter Abschnitt darin kann im Vergleich zum Originaldokument erheblich anders aussehen. |
| MajorFormattingLoss | 256 | Allgemeiner erheblicher Formatierungsverlust, kein spezifischer Code. |
| MinorFormattingLossCategory | 16711680 | Das resultierende Dokument oder ein bestimmter Ort darin könnte im Vergleich zum Originaldokument etwas anders aussehen. |
| MinorFormattingLoss | 65536 | Allgemeiner kleiner Formatierungsverlust, kein spezifischer Code. |
| FontSubstitution | 131072 | [Font](../font/) wurde ersetzt. |
| FontEmbedding | 262144 | Verlust von eingebetteten Schriftartinformationen beim Speichern des Dokuments. |
| UnexpectedContentCategory | 251658240 | Einige Inhalte im Quelldokument konnten nicht erkannt werden (d. h. werden nicht unterstützt); dies kann Probleme verursachen oder zu Daten‑/Formatierungsverlust führen. |
| UnexpectedContent | 16777216 | Allgemeiner unerwarteter Inhalt, kein spezifischer Code. |
| Hint | 268435456 | Weist auf ein potenzielles Problem hin oder schlägt eine Verbesserung vor. |


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
