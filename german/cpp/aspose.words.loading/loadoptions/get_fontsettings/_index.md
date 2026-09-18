---
title: "Aspose::Words::Loading::LoadOptions::get_FontSettings Methode"
linktitle: "get_FontSettings"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Loading::LoadOptions::get_FontSettings Methode. Ermöglicht das Festlegen von Dokument‑Schrifteinstellungen in C++."
type: docs
weight: 7000
url: /de/cpp/aspose.words.loading/loadoptions/get_fontsettings/
---
## LoadOptions::get_FontSettings method


Ermöglicht das Angeben von Dokument-Schrifteinstellungen.

```cpp
System::SharedPtr<Aspose::Words::Fonts::FontSettings> Aspose::Words::Loading::LoadOptions::get_FontSettings() const
```

## Hinweise


Beim Laden einiger Formate kann Aspose.Words die Auflösung von Schriftarten erfordern. Zum Beispiel kann beim Laden von HTML‑Dokumenten [Aspose.Words](../../../aspose.words/) die Schriftartenauflösung durchgeführt werden, um einen Schriftart‑Fallback zu ermöglichen.

Wenn auf **null** gesetzt, werden die standardmäßigen statischen Schrifteinstellungen [DefaultInstance](../../../aspose.words.fonts/fontsettings/get_defaultinstance/) verwendet.

Der Standardwert ist **null**.

## Beispiele



Zeigt, wie man beim Laden Schriftart‑Ersatz festlegt.
```cpp
auto loadOptions = System::MakeObject<Aspose::Words::Loading::LoadOptions>();
loadOptions->set_FontSettings(System::MakeObject<Aspose::Words::Fonts::FontSettings>());

// Legen Sie eine Schriftart‑Ersatzregel für ein LoadOptions‑Objekt fest.
// Wenn das Dokument, das wir laden, eine Schriftart verwendet, die wir nicht besitzen,
// Diese Regel ersetzt die nicht verfügbare Schriftart durch eine, die existiert.
// In diesem Fall werden alle Verwendungen von "MissingFont" zu "Comic Sans MS" konvertiert.
System::SharedPtr<Aspose::Words::Fonts::TableSubstitutionRule> substitutionRule = loadOptions->get_FontSettings()->get_SubstitutionSettings()->get_TableSubstitution();
substitutionRule->AddSubstitutes(u"MissingFont", System::MakeArray<System::String>({u"Comic Sans MS"}));

auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Missing font.html", loadOptions);

// An diesem Punkt bleibt solcher Text weiterhin in "MissingFont".
// Die Schriftart-Ersetzung erfolgt, wenn wir das Dokument rendern.
ASSERT_EQ(u"MissingFont", doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_Runs()->idx_get(0)->get_Font()->get_Name());

doc->Save(get_ArtifactsDir() + u"FontSettings.ResolveFontsBeforeLoadingDocument.pdf");
```


Zeigt, wie man Schriftart-Ersetzungseinstellungen beim Laden eines Dokuments anwendet.
```cpp
// Erstellen Sie ein FontSettings-Objekt, das die Schriftart "Times New Roman" ersetzt
// mit der Schriftart "Arvo" aus unserem "MyFonts"-Ordner.
auto fontSettings = System::MakeObject<Aspose::Words::Fonts::FontSettings>();
fontSettings->SetFontsFolder(get_FontsDir(), false);
fontSettings->get_SubstitutionSettings()->get_TableSubstitution()->AddSubstitutes(u"Times New Roman", System::MakeArray<System::String>({u"Arvo"}));

// Setzen Sie dieses FontSettings-Objekt als Eigenschaft eines neu erstellten LoadOptions-Objekts.
auto loadOptions = System::MakeObject<Aspose::Words::Loading::LoadOptions>();
loadOptions->set_FontSettings(fontSettings);

// Laden Sie das Dokument und rendern Sie es anschließend als PDF mit der Schriftart-Ersetzung.
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document.docx", loadOptions);

doc->Save(get_ArtifactsDir() + u"LoadOptions.FontSettings.pdf");
```

## Siehe auch

* Class [FontSettings](../../../aspose.words.fonts/fontsettings/)
* Class [LoadOptions](../)
* Namespace [Aspose::Words::Loading](../../)
* Library [Aspose.Words for C++](../../../)
