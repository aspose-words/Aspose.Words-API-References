---
title: get_DefaultEditingLanguage
second_title: Aspose.Words for C++ API Reference
description: Gets or sets default editing language. The default value is EnglishUS.
type: docs
weight: 53
url: /cpp/aspose.words.loading/languagepreferences/get_defaulteditinglanguage/
---
## LanguagePreferences::get_DefaultEditingLanguage method


Gets or sets default editing language. The default value is [EnglishUS](../../editinglanguage/).

```cpp
Aspose::Words::Loading::EditingLanguage Aspose::Words::Loading::LanguagePreferences::get_DefaultEditingLanguage() const
```


## Examples



Shows how set a default language when loading a document. 
```cpp
auto loadOptions = MakeObject<LoadOptions>();
loadOptions->get_LanguagePreferences()->set_DefaultEditingLanguage(EditingLanguage::Russian);

auto doc = MakeObject<Document>(MyDir + u"No default editing language.docx", loadOptions);

int localeId = doc->get_Styles()->get_DefaultFont()->get_LocaleId();
std::cout << (localeId == (int)EditingLanguage::Russian
                  ? String(u"The document either has no any language set in defaults or it was set to Russian originally.")
                  : String(u"The document default language was set to another than Russian language originally, so it is not overridden."))
          << std::endl;
```

## See Also

* Enum [EditingLanguage](../../editinglanguage/)
* Class [LanguagePreferences](../)
* Namespace [Aspose::Words::Loading](../../)
* Library [Aspose.Words](../../../)
