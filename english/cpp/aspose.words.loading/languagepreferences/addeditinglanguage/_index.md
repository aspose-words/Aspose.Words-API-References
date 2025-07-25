---
title: Aspose::Words::Loading::LanguagePreferences::AddEditingLanguage method
linktitle: AddEditingLanguage
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Loading::LanguagePreferences::AddEditingLanguage method. Adds additional editing language in C++.'
type: docs
weight: 3000
url: /cpp/aspose.words.loading/languagepreferences/addeditinglanguage/
---
## LanguagePreferences::AddEditingLanguage method


Adds additional editing language.

```cpp
void Aspose::Words::Loading::LanguagePreferences::AddEditingLanguage(Aspose::Words::Loading::EditingLanguage language)
```


## Examples



Shows how to apply language preferences when loading a document. 
```cpp
auto loadOptions = System::MakeObject<Aspose::Words::Loading::LoadOptions>();
loadOptions->get_LanguagePreferences()->AddEditingLanguage(Aspose::Words::Loading::EditingLanguage::Japanese);

auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"No default editing language.docx", loadOptions);

int32_t localeIdFarEast = doc->get_Styles()->get_DefaultFont()->get_LocaleIdFarEast();
std::cout << (localeIdFarEast == (int32_t)Aspose::Words::Loading::EditingLanguage::Japanese ? System::String(u"The document either has no any FarEast language set in defaults or it was set to Japanese originally.") : System::String(u"The document default FarEast language was set to another than Japanese language originally, so it is not overridden.")) << std::endl;
```

## See Also

* Enum [EditingLanguage](../../editinglanguage/)
* Class [LanguagePreferences](../)
* Namespace [Aspose::Words::Loading](../../)
* Library [Aspose.Words for C++](../../../)
