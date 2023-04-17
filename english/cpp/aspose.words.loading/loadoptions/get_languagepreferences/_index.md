---
title: Aspose::Words::Loading::LoadOptions::get_LanguagePreferences method
linktitle: get_LanguagePreferences
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Loading::LoadOptions::get_LanguagePreferences method. Gets language preferences that will be used when document is loading in C++.'
type: docs
weight: 9000
url: /cpp/aspose.words.loading/loadoptions/get_languagepreferences/
---
## LoadOptions::get_LanguagePreferences method


Gets language preferences that will be used when document is loading.

```cpp
System::SharedPtr<Aspose::Words::Loading::LanguagePreferences> Aspose::Words::Loading::LoadOptions::get_LanguagePreferences() const
```


## Examples



Shows how to apply language preferences when loading a document. 
```cpp
auto loadOptions = MakeObject<LoadOptions>();
loadOptions->get_LanguagePreferences()->AddEditingLanguage(EditingLanguage::Japanese);

auto doc = MakeObject<Document>(MyDir + u"No default editing language.docx", loadOptions);

int localeIdFarEast = doc->get_Styles()->get_DefaultFont()->get_LocaleIdFarEast();
std::cout << (localeIdFarEast == (int)EditingLanguage::Japanese
                  ? String(u"The document either has no any FarEast language set in defaults or it was set to Japanese originally.")
                  : String(u"The document default FarEast language was set to another than Japanese language originally, so it is not overridden."))
          << std::endl;
```

## See Also

* Class [LanguagePreferences](../../languagepreferences/)
* Class [LoadOptions](../)
* Namespace [Aspose::Words::Loading](../../)
* Library [Aspose.Words for C++](../../../)
