---
title: RegisterDictionary
second_title: Aspose.Words for C++ API Reference
description: Registers and loads a hyphenation dictionary for the specified language from a stream. Throws if dictionary cannot be read or has invalid format.
type: docs
weight: 40
url: /cpp/aspose.words/hyphenation/registerdictionary/
---
## Hyphenation::RegisterDictionary(const System::String\&, const System::SharedPtr\<System::IO::Stream\>\&) method


Registers and loads a hyphenation dictionary for the specified language from a stream. Throws if dictionary cannot be read or has invalid format.

```cpp
static void Aspose::Words::Hyphenation::RegisterDictionary(const System::String &language, const System::SharedPtr<System::IO::Stream> &stream)
```


| Parameter | Type | Description |
| --- | --- | --- |
| language | const System::String\& | A language name, e.g. "en-US". See .NET documentation for "culture name" and RFC 4646 for details. |
| stream | const System::SharedPtr\<System::IO::Stream\>\& | A stream for the dictionary file in OpenOffice format. |

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

* Class [Hyphenation](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words](../../../)
## Hyphenation::RegisterDictionary(const System::String\&, const System::String\&) method


Registers and loads a hyphenation dictionary for the specified language from file. Throws if dictionary cannot be read or has invalid format. This method can also be used to register Null dictionary to prevent [Callback](../get_callback/) from being called repeatedly for the same language.

```cpp
static void Aspose::Words::Hyphenation::RegisterDictionary(const System::String &language, const System::String &fileName)
```


| Parameter | Type | Description |
| --- | --- | --- |
| language | const System::String\& | A language name, e.g. "en-US". See .NET documentation for "culture name" and RFC 4646 for details. |
| fileName | const System::String\& | A path to the dictionary file in Open Office format. If this parameter is null or empty string then registered is Null dictionary and callback is not called anymore for this language. To enable callback again use [UnregisterDictionary()](../) method. |

## Examples



Shows how to register a hyphenation dictionary. 
```cpp
// A hyphenation dictionary contains a list of strings that define hyphenation rules for the dictionary's language.
// When a document contains lines of text in which a word could be split up and continued on the next line,
// hyphenation will look through the dictionary's list of strings for that word's substrings.
// If the dictionary contains a substring, then hyphenation will split the word across two lines
// by the substring and add a hyphen to the first half.
// Register a dictionary file from the local file system to the "de-CH" locale.
Hyphenation::RegisterDictionary(u"de-CH", MyDir + u"hyph_de_CH.dic");

ASSERT_TRUE(Hyphenation::IsDictionaryRegistered(u"de-CH"));

// Open a document containing text with a locale matching that of our dictionary,
// and save it to a fixed-page save format. The text in that document will be hyphenated.
auto doc = MakeObject<Document>(MyDir + u"German text.docx");

ASSERT_TRUE(doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_Runs()->LINQ_OfType<SharedPtr<Run>>()->LINQ_All(
    [](SharedPtr<Run> r) { return r->get_Font()->get_LocaleId() == MakeObject<System::Globalization::CultureInfo>(u"de-CH")->get_LCID(); }));

doc->Save(ArtifactsDir + u"Hyphenation.Dictionary.Registered.pdf");

// Re-load the document after un-registering the dictionary,
// and save it to another PDF, which will not have hyphenated text.
Hyphenation::UnregisterDictionary(u"de-CH");

ASSERT_FALSE(Hyphenation::IsDictionaryRegistered(u"de-CH"));

doc = MakeObject<Document>(MyDir + u"German text.docx");
doc->Save(ArtifactsDir + u"Hyphenation.Dictionary.Unregistered.pdf");
```


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

* Class [Hyphenation](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words](../../../)
## Hyphenation::RegisterDictionary(System::String, std::basic_istream\<CharType, Traits\>\&) method




```cpp
template<typename CharType,typename Traits> static void Aspose::Words::Hyphenation::RegisterDictionary(System::String language, std::basic_istream<CharType, Traits> &stream)
```

## See Also

* Class [Hyphenation](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words](../../../)
