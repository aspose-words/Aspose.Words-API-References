---
title: WarningInfoCollection
second_title: Aspose.Words for C++ API Reference
description: Represents a typed collection of WarningInfo objects.
type: docs
weight: 963
url: /cpp/aspose.words/warninginfocollection/
---
## WarningInfoCollection class


Represents a typed collection of [WarningInfo](../warninginfo/) objects.

```cpp
class WarningInfoCollection : public Aspose::Words::IWarningCallback, public System::Collections::Generic::IEnumerable<System::SharedPtr<Aspose::Words::WarningInfo>>
```

## Methods

| Method | Description |
| --- | --- |
| [begin](./begin/)() |  |
| [begin](./begin/)() const |  |
| [cbegin](./cbegin/)() const |  |
| [cend](./cend/)() const |  |
| [Clear](./clear/)() | Removes all elements from the collection. |
| [end](./end/)() |  |
| [end](./end/)() const |  |
| [get_Count](./get_count/)() | Gets the number of elements contained in the collection. |
| [GetEnumerator](./getenumerator/)() override | Returns an enumerator object that can be used to iterate over all items in the collection. |
| [idx_get](./idx_get/)(int32_t) | Gets an item at the specified index. |
| [virtualizeBeginConstIterator](./virtualizebeginconstiterator/)() const override |  |
| [virtualizeBeginIterator](./virtualizebeginiterator/)() override |  |
| [virtualizeEndConstIterator](./virtualizeendconstiterator/)() const override |  |
| [virtualizeEndIterator](./virtualizeenditerator/)() override |  |
| [Warning](./warning/)(System::SharedPtr\<Aspose::Words::WarningInfo\>) override | Implements the [IWarningCallback](../iwarningcallback/) interface. Adds a warning to this collection. |
| [WarningInfoCollection](./warninginfocollection/)() |  |
## Typedefs

| Typedef | Description |
| --- | --- |
| [const_iterator](./const_iterator/) |  |
| [iterator](./iterator/) |  |
| [iterator_holder_type](./iterator_holder_type/) |  |
| [virtualized_iterator](./virtualized_iterator/) |  |
| [virtualized_iterator_element](./virtualized_iterator_element/) |  |

You can use this collection object as the simplest form of [IWarningCallback](../iwarningcallback/) implementation to gather all warnings that Aspose.Words generates during a load or save operation. Create an instance of this class and assign it to the [WarningCallback](../../aspose.words.loading/loadoptions/get_warningcallback/) or [WarningCallback](../documentbase/get_warningcallback/) property.

## Examples




Shows how to set the property for finding the closest match for a missing font from the available font sources. 
```cpp
void EnableFontSubstitution()
{
    // Open a document that contains text formatted with a font that does not exist in any of our font sources.
    auto doc = MakeObject<Document>(MyDir + u"Missing font.docx");

    // Assign a callback for handling font substitution warnings.
    auto substitutionWarningHandler = MakeObject<ExFontSettings::HandleDocumentSubstitutionWarnings>();
    doc->set_WarningCallback(substitutionWarningHandler);

    // Set a default font name and enable font substitution.
    auto fontSettings = MakeObject<FontSettings>();
    fontSettings->get_SubstitutionSettings()->get_DefaultFontSubstitution()->set_DefaultFontName(u"Arial");
    ;
    fontSettings->get_SubstitutionSettings()->get_FontInfoSubstitution()->set_Enabled(true);

    // We will get a font substitution warning if we save a document with a missing font.
    doc->set_FontSettings(fontSettings);
    doc->Save(ArtifactsDir + u"FontSettings.EnableFontSubstitution.pdf");

    {
        SharedPtr<System::Collections::Generic::IEnumerator<SharedPtr<WarningInfo>>> warnings = substitutionWarningHandler->FontWarnings->GetEnumerator();
        while (warnings->MoveNext())
        {
            std::cout << warnings->get_Current()->get_Description() << std::endl;
        }
    }

    // We can also verify warnings in the collection and clear them.
    ASSERT_EQ(WarningSource::Layout, substitutionWarningHandler->FontWarnings->idx_get(0)->get_Source());
    ASSERT_EQ(u"Font '28 Days Later' has not been found. Using 'Calibri' font instead. Reason: alternative name from document.",
              substitutionWarningHandler->FontWarnings->idx_get(0)->get_Description());

    substitutionWarningHandler->FontWarnings->Clear();

    ASSERT_EQ(0, substitutionWarningHandler->FontWarnings->get_Count());
}

class HandleDocumentSubstitutionWarnings : public IWarningCallback
{
public:
    SharedPtr<WarningInfoCollection> FontWarnings;

    void Warning(SharedPtr<WarningInfo> info) override
    {
        if (info->get_WarningType() == WarningType::FontSubstitution)
        {
            FontWarnings->Warning(info);
        }
    }

    HandleDocumentSubstitutionWarnings() : FontWarnings(MakeObject<WarningInfoCollection>())
    {
    }
};
```

