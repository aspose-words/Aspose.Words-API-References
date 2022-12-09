---
title: Hyphenation
second_title: Aspose.Words for C++ API Reference
description: Provides methods for working with hyphenation dictionaries. These dictionaries prescribe where words of a specific language can be hyphenated. To learn more, visit the  documentation article.
type: docs
weight: 417
url: /cpp/aspose.words/hyphenation/
---
## Hyphenation class


Provides methods for working with hyphenation dictionaries. These dictionaries prescribe where words of a specific language can be hyphenated. To learn more, visit the [Working with Hyphenation](https://docs.aspose.com/words/cpp/working-with-hyphenation/) documentation article.

```cpp
class Hyphenation
```

## Methods

| Method | Description |
| --- | --- |
| static [get_Callback](./get_callback/)() | Gets or sets callback interface used to request dictionaries when page layout of the document is built. This allows delay loading of dictionaries which may be useful when processing documents in many languages. |
| static [get_WarningCallback](./get_warningcallback/)() | Called during a load hyphenation patterns, when an issue is detected that might result in formatting fidelity loss. |
| [Hyphenation](./hyphenation/)() |  |
| static [IsDictionaryRegistered](./isdictionaryregistered/)(const System::String\&) | Returns **false** if for the specified language there is no dictionary registered or if registered is Null dictionary, **true** otherwise. |
| static [RegisterDictionary](./registerdictionary/)(const System::String\&, const System::SharedPtr\<System::IO::Stream\>\&) | Registers and loads a hyphenation dictionary for the specified language from a stream. Throws if dictionary cannot be read or has invalid format. |
| static [RegisterDictionary](./registerdictionary/)(const System::String\&, const System::String\&) | Registers and loads a hyphenation dictionary for the specified language from file. Throws if dictionary cannot be read or has invalid format. This method can also be used to register Null dictionary to prevent [Callback](./get_callback/) from being called repeatedly for the same language. |
| static [RegisterDictionary](./registerdictionary/)(System::String, std::basic_istream\<CharType, Traits\>\&) |  |
| static [set_Callback](./set_callback/)(const System::SharedPtr\<Aspose::Words::IHyphenationCallback\>\&) | Setter for [Aspose::Words::Hyphenation::get_Callback](./get_callback/). |
| static [set_WarningCallback](./set_warningcallback/)(const System::SharedPtr\<Aspose::Words::IWarningCallback\>\&) | Setter for [Aspose::Words::Hyphenation::get_WarningCallback](./get_warningcallback/). |
| static [UnregisterDictionary](./unregisterdictionary/)(const System::String\&) | Unregisters a hyphenation dictionary for the specified language. This is different from registering Null dictionary. Unregistering a dictionary enables callback for the specified language. |

## Examples



Shows how to open and register a dictionary from a file. 
```cpp
void RegisterDictionary()
{
    // Set up a callback that tracks warnings that occur during hyphenation dictionary registration.
    auto warningInfoCollection = MakeObject<WarningInfoCollection>();
    Hyphenation::set_WarningCallback(warningInfoCollection);

    // Register an English (US) hyphenation dictionary by stream.
    SharedPtr<System::IO::Stream> dictionaryStream = MakeObject<System::IO::FileStream>(MyDir + u"hyph_en_US.dic", System::IO::FileMode::Open);
    Hyphenation::RegisterDictionary(u"en-US", dictionaryStream);

    ASSERT_EQ(0, warningInfoCollection->get_Count());

    // Open a document with a locale that Microsoft Word may not hyphenate on an English machine, such as German.
    auto doc = MakeObject<Document>(MyDir + u"German text.docx");

    // To hyphenate that document upon saving, we need a hyphenation dictionary for the "de-CH" language code.
    // This callback will handle the automatic request for that dictionary.
    Hyphenation::set_Callback(MakeObject<ExHyphenation::CustomHyphenationDictionaryRegister>());

    // When we save the document, German hyphenation will take effect.
    doc->Save(ArtifactsDir + u"Hyphenation.RegisterDictionary.pdf");

    // This dictionary contains two identical patterns, which will trigger a warning.
    ASSERT_EQ(1, warningInfoCollection->get_Count());
    ASSERT_EQ(WarningType::MinorFormattingLoss, warningInfoCollection->idx_get(0)->get_WarningType());
    ASSERT_EQ(WarningSource::Layout, warningInfoCollection->idx_get(0)->get_Source());
    ASSERT_EQ(String(u"Hyphenation dictionary contains duplicate patterns. The only first found pattern will be used. ") +
                  u"Content can be wrapped differently.",
              warningInfoCollection->idx_get(0)->get_Description());
}

class CustomHyphenationDictionaryRegister : public IHyphenationCallback
{
public:
    CustomHyphenationDictionaryRegister()
    {
        mHyphenationDictionaryFiles = MakeObject<System::Collections::Generic::Dictionary<String, String>>();
        mHyphenationDictionaryFiles->Add(u"en-US", MyDir + u"hyph_en_US.dic");
        mHyphenationDictionaryFiles->Add(u"de-CH", MyDir + u"hyph_de_CH.dic");
    }

    void RequestDictionary(String language) override
    {
        std::cout << (String(u"Hyphenation dictionary requested: ") + language);

        if (Hyphenation::IsDictionaryRegistered(language))
        {
            std::cout << ", is already registered." << std::endl;
            return;
        }

        if (mHyphenationDictionaryFiles->ContainsKey(language))
        {
            Hyphenation::RegisterDictionary(language, mHyphenationDictionaryFiles->idx_get(language));
            std::cout << ", successfully registered." << std::endl;
            return;
        }

        std::cout << ", no respective dictionary file known by this Callback." << std::endl;
    }

private:
    SharedPtr<System::Collections::Generic::Dictionary<String, String>> mHyphenationDictionaryFiles;
};
```

## See Also

* Namespace [Aspose::Words](../)
* Library [Aspose.Words](../../)
