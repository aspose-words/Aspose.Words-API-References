---
title: Aspose::Words::Loading::LoadOptions::get_ResourceLoadingCallback method
linktitle: get_ResourceLoadingCallback
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Loading::LoadOptions::get_ResourceLoadingCallback method. Allows to control how external resources (images, style sheets) are loaded when a document is imported from HTML, MHTML in C++.'
type: docs
weight: 15000
url: /cpp/aspose.words.loading/loadoptions/get_resourceloadingcallback/
---
## LoadOptions::get_ResourceLoadingCallback method


Allows to control how external resources (images, style sheets) are loaded when a document is imported from HTML, MHTML.

```cpp
System::SharedPtr<Aspose::Words::Loading::IResourceLoadingCallback> Aspose::Words::Loading::LoadOptions::get_ResourceLoadingCallback() const
```

## Examples


Shows how to handle external resources when loading Html documents.

```cpp
auto loadOptions = System::MakeObject<Aspose::Words::Loading::LoadOptions>();
loadOptions->set_ResourceLoadingCallback(System::MakeObject<Aspose::Words::ApiExamples::ExLoadOptions::HtmlLinkedResourceLoadingCallback>());

// When we load the document, our callback will handle linked resources such as CSS stylesheets and images.
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Images.html", loadOptions);
doc->Save(get_ArtifactsDir() + u"LoadOptions.LoadOptionsCallback.pdf");
```

Shows how to handle external resources when loading Html documents (HtmlLinkedResourceLoadingCallback).

```cpp
/// <summary>
    /// Prints the filenames of all external stylesheets and substitutes all images of a loaded html document.
    /// </summary>
    class HtmlLinkedResourceLoadingCallback : public IResourceLoadingCallback
    {
        typedef HtmlLinkedResourceLoadingCallback ThisType;
        typedef IResourceLoadingCallback BaseType;

        typedef ::System::BaseTypesInfo<BaseType> ThisTypeBaseTypesInfo;
        RTTI_INFO_DECL();

    public:

        Aspose::Words::Loading::ResourceLoadingAction ResourceLoading(System::SharedPtr<Aspose::Words::Loading::ResourceLoadingArgs> args) override;

    };

    /// <summary>
    /// IWarningCallback that prints warnings and their details as they arise during document loading.
    /// </summary>
    class DocumentLoadingWarningCallback : public IWarningCallback
    {
        typedef DocumentLoadingWarningCallback ThisType;
        typedef IWarningCallback BaseType;

        typedef ::System::BaseTypesInfo<BaseType> ThisTypeBaseTypesInfo;
        RTTI_INFO_DECL();

    public:

        void Warning(System::SharedPtr<Aspose::Words::WarningInfo> info) override;
        System::SharedPtr<System::Collections::Generic::List<System::SharedPtr<Aspose::Words::WarningInfo>>> GetWarnings();

        DocumentLoadingWarningCallback();

    private:

        System::SharedPtr<System::Collections::Generic::List<System::SharedPtr<Aspose::Words::WarningInfo>>> mWarnings;

    };


public:

    void LoadOptionsCallback();
```
## See Also

* Class [LoadOptions](../)
* Namespace [Aspose::Words::Loading](../../)
* Library [Aspose.Words for C++](../../../)
