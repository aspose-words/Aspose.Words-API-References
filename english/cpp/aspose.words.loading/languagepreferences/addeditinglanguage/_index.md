---
title: AddEditingLanguage
second_title: Aspose.Words for C++ API Reference
description: Adds additional editing language.
type: docs
weight: 27
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

* Enum [EditingLanguage](../../editinglanguage/)
* Class [LanguagePreferences](../)
* Namespace [Aspose::Words::Loading](../../)
* Library [Aspose.Words](../../../)
