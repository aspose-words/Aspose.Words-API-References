---
title: Aspose::Words::Loading::LoadOptions::get_WarningCallback method
linktitle: get_WarningCallback
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Loading::LoadOptions::get_WarningCallback method. Called during a load operation, when an issue is detected that might result in data or formatting fidelity loss in C++.'
type: docs
weight: 18000
url: /cpp/aspose.words.loading/loadoptions/get_warningcallback/
---
## LoadOptions::get_WarningCallback method


Called during a load operation, when an issue is detected that might result in data or formatting fidelity loss.

```cpp
System::SharedPtr<Aspose::Words::IWarningCallback> Aspose::Words::Loading::LoadOptions::get_WarningCallback() const
```


## Examples



Shows how to print and store warnings that occur during document loading. 
```cpp
void LoadOptionsWarningCallback()
{
    // Create a new LoadOptions object and set its WarningCallback attribute
    // as an instance of our IWarningCallback implementation.
    auto loadOptions = MakeObject<LoadOptions>();
    loadOptions->set_WarningCallback(MakeObject<ExLoadOptions::DocumentLoadingWarningCallback>());

    // Our callback will print all warnings that come up during the load operation.
    auto doc = MakeObject<Document>(MyDir + u"Document.docx", loadOptions);

    SharedPtr<System::Collections::Generic::List<SharedPtr<WarningInfo>>> warnings =
        (System::StaticCast<ApiExamples::ExLoadOptions::DocumentLoadingWarningCallback>(loadOptions->get_WarningCallback()))->GetWarnings();
    ASSERT_EQ(3, warnings->get_Count());
}

class DocumentLoadingWarningCallback : public IWarningCallback
{
public:
    void Warning(SharedPtr<WarningInfo> info) override
    {
        std::cout << String::Format(u"Warning: {0}", info->get_WarningType()) << std::endl;
        std::cout << String::Format(u"\tSource: {0}", info->get_Source()) << std::endl;
        std::cout << "\tDescription: " << info->get_Description() << std::endl;
        mWarnings->Add(info);
    }

    SharedPtr<System::Collections::Generic::List<SharedPtr<WarningInfo>>> GetWarnings()
    {
        return mWarnings;
    }

    DocumentLoadingWarningCallback() : mWarnings(MakeObject<System::Collections::Generic::List<SharedPtr<WarningInfo>>>())
    {
    }

private:
    SharedPtr<System::Collections::Generic::List<SharedPtr<WarningInfo>>> mWarnings;
};
```

## See Also

* Interface [IWarningCallback](../../../aspose.words/iwarningcallback/)
* Class [LoadOptions](../)
* Namespace [Aspose::Words::Loading](../../)
* Library [Aspose.Words for C++](../../../)
