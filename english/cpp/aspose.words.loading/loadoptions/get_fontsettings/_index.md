---
title: get_FontSettings
second_title: Aspose.Words for C++ API Reference
description: Allows to specify document font settings.
type: docs
weight: 79
url: /cpp/aspose.words.loading/loadoptions/get_fontsettings/
---
## LoadOptions::get_FontSettings method


Allows to specify document font settings.

```cpp
System::SharedPtr<Aspose::Words::Fonts::FontSettings> Aspose::Words::Loading::LoadOptions::get_FontSettings() const
```

## Remarks


When loading some formats, Aspose.Words may require to resolve the fonts. For example, when loading HTML documents [Aspose.Words](../../../aspose.words/) may resolve the fonts to perform font fallback.

If set to **null**, default static font settings [DefaultInstance](../../../aspose.words.fonts/fontsettings/get_defaultinstance/) will be used.

The default value is **null**.

## Examples



Shows how to designate font substitutes during loading. 
```cpp
auto loadOptions = MakeObject<LoadOptions>();
loadOptions->set_FontSettings(MakeObject<FontSettings>());

// Set a font substitution rule for a LoadOptions object.
// If the document we are loading uses a font which we do not have,
// this rule will substitute the unavailable font with one that does exist.
// In this case, all uses of the "MissingFont" will convert to "Comic Sans MS".
SharedPtr<TableSubstitutionRule> substitutionRule = loadOptions->get_FontSettings()->get_SubstitutionSettings()->get_TableSubstitution();
substitutionRule->AddSubstitutes(u"MissingFont", MakeArray<String>({u"Comic Sans MS"}));

auto doc = MakeObject<Document>(MyDir + u"Missing font.html", loadOptions);

// At this point such text will still be in "MissingFont".
// Font substitution will take place when we render the document.
ASSERT_EQ(u"MissingFont", doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_Runs()->idx_get(0)->get_Font()->get_Name());

doc->Save(ArtifactsDir + u"FontSettings.ResolveFontsBeforeLoadingDocument.pdf");
```


Shows how to apply font substitution settings while loading a document. 
```cpp
// Create a FontSettings object that will substitute the "Times New Roman" font
// with the font "Arvo" from our "MyFonts" folder.
auto fontSettings = MakeObject<FontSettings>();
fontSettings->SetFontsFolder(FontsDir, false);
fontSettings->get_SubstitutionSettings()->get_TableSubstitution()->AddSubstitutes(u"Times New Roman", MakeArray<String>({u"Arvo"}));

// Set that FontSettings object as a property of a newly created LoadOptions object.
auto loadOptions = MakeObject<LoadOptions>();
loadOptions->set_FontSettings(fontSettings);

// Load the document, then render it as a PDF with the font substitution.
auto doc = MakeObject<Document>(MyDir + u"Document.docx", loadOptions);

doc->Save(ArtifactsDir + u"LoadOptions.FontSettings.pdf");
```

## See Also

* Class [FontSettings](../../../aspose.words.fonts/fontsettings/)
* Class [LoadOptions](../)
* Namespace [Aspose::Words::Loading](../../)
* Library [Aspose.Words](../../../)
