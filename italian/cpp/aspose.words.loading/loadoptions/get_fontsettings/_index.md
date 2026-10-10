---
title: "Metodo Aspose::Words::Loading::LoadOptions::get_FontSettings"
linktitle: "get_FontSettings"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::Loading::LoadOptions::get_FontSettings. Consente di specificare le impostazioni dei font del documento in C++."
type: docs
weight: 7000
url: /it/cpp/aspose.words.loading/loadoptions/get_fontsettings/
---
## LoadOptions::get_FontSettings method


Consente di specificare le impostazioni del carattere del documento.

```cpp
System::SharedPtr<Aspose::Words::Fonts::FontSettings> Aspose::Words::Loading::LoadOptions::get_FontSettings() const
```

## Note


Durante il caricamento di alcuni formati, Aspose.Words potrebbe dover risolvere i font. Ad esempio, durante il caricamento di documenti HTML [Aspose.Words](../../../aspose.words/) può risolvere i font per eseguire il fallback dei font.

Se impostato a **null**, verranno utilizzate le impostazioni statiche dei font predefinite [DefaultInstance](../../../aspose.words.fonts/fontsettings/get_defaultinstance/).

Il valore predefinito è **null**.

## Esempi



Mostra come designare i sostituti dei font durante il caricamento.
```cpp
auto loadOptions = System::MakeObject<Aspose::Words::Loading::LoadOptions>();
loadOptions->set_FontSettings(System::MakeObject<Aspose::Words::Fonts::FontSettings>());

// Imposta una regola di sostituzione dei font per un oggetto LoadOptions.
// Se il documento che stiamo caricando utilizza un font che non possediamo,
// questa regola sostituirà il font non disponibile con uno che esiste.
// In questo caso, tutte le occorrenze di "MissingFont" verranno convertite in "Comic Sans MS".
System::SharedPtr<Aspose::Words::Fonts::TableSubstitutionRule> substitutionRule = loadOptions->get_FontSettings()->get_SubstitutionSettings()->get_TableSubstitution();
substitutionRule->AddSubstitutes(u"MissingFont", System::MakeArray<System::String>({u"Comic Sans MS"}));

auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Missing font.html", loadOptions);

// A questo punto tale testo sarà ancora in "MissingFont".
// La sostituzione dei caratteri avverrà quando renderizziamo il documento.
ASSERT_EQ(u"MissingFont", doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_Runs()->idx_get(0)->get_Font()->get_Name());

doc->Save(get_ArtifactsDir() + u"FontSettings.ResolveFontsBeforeLoadingDocument.pdf");
```


Mostra come applicare le impostazioni di sostituzione dei caratteri durante il caricamento di un documento.
```cpp
// Crea un oggetto FontSettings che sostituirà il carattere "Times New Roman"
// con il carattere "Arvo" dalla nostra cartella "MyFonts".
auto fontSettings = System::MakeObject<Aspose::Words::Fonts::FontSettings>();
fontSettings->SetFontsFolder(get_FontsDir(), false);
fontSettings->get_SubstitutionSettings()->get_TableSubstitution()->AddSubstitutes(u"Times New Roman", System::MakeArray<System::String>({u"Arvo"}));

// Imposta quell'oggetto FontSettings come proprietà di un nuovo oggetto LoadOptions.
auto loadOptions = System::MakeObject<Aspose::Words::Loading::LoadOptions>();
loadOptions->set_FontSettings(fontSettings);

// Carica il documento, quindi renderizzalo come PDF con la sostituzione dei caratteri.
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document.docx", loadOptions);

doc->Save(get_ArtifactsDir() + u"LoadOptions.FontSettings.pdf");
```

## Vedi anche

* Class [FontSettings](../../../aspose.words.fonts/fontsettings/)
* Class [LoadOptions](../)
* Namespace [Aspose::Words::Loading](../../)
* Library [Aspose.Words for C++](../../../)
