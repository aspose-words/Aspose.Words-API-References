---
title: get_Document
second_title: Aspose.Words for C++ API Reference
description: Gets document.
type: docs
weight: 1
url: /cpp/aspose.words.layout/pagelayoutcallbackargs/get_document/
---
## PageLayoutCallbackArgs.get_Document method


Gets document.

```cpp
const System::SharedPtr<Aspose::Words::Document> & Aspose::Words::Layout::PageLayoutCallbackArgs::get_Document() const
```


## Examples




Shows how to track layout changes with a layout callback. 
```cpp
void PageLayoutCallback()
{
    auto doc = MakeObject<Document>();
    doc->get_BuiltInDocumentProperties()->set_Title(u"My Document");

    auto builder = MakeObject<DocumentBuilder>(doc);
    builder->Writeln(u"Hello world!");

    doc->get_LayoutOptions()->set_Callback(MakeObject<ExLayout::RenderPageLayoutCallback>());
    doc->UpdatePageLayout();

    doc->Save(ArtifactsDir + u"Layout.PageLayoutCallback.pdf");
}

class RenderPageLayoutCallback : public IPageLayoutCallback
{
public:
    void Notify(SharedPtr<PageLayoutCallbackArgs> a) override
    {
        switch (a->get_Event())
        {
        case PageLayoutEvent::PartReflowFinished:
            NotifyPartFinished(a);
            break;

        case PageLayoutEvent::ConversionFinished:
            NotifyConversionFinished(a);
            break;

        default:
            break;
        }
    }

    RenderPageLayoutCallback() : mNum(0)
    {
    }

private:
    int mNum;

    void NotifyPartFinished(SharedPtr<PageLayoutCallbackArgs> a)
    {
        std::cout << "Part at page " << (a->get_PageIndex() + 1) << " reflow." << std::endl;
        RenderPage(a, a->get_PageIndex());
    }

    void NotifyConversionFinished(SharedPtr<PageLayoutCallbackArgs> a)
    {
        std::cout << "Document \"" << a->get_Document()->get_BuiltInDocumentProperties()->get_Title() << "\" converted to page format." << std::endl;
    }

    void RenderPage(SharedPtr<PageLayoutCallbackArgs> a, int pageIndex)
    {
        auto saveOptions = MakeObject<ImageSaveOptions>(SaveFormat::Png);
        saveOptions->set_PageSet(MakeObject<PageSet>(pageIndex));

        {
            auto stream = MakeObject<System::IO::FileStream>(ArtifactsDir + String::Format(u"PageLayoutCallback.page-{0} {1}.png", pageIndex + 1, ++mNum),
                                                             System::IO::FileMode::Create);
            a->get_Document()->Save(stream, saveOptions);
        }
    }
};
```

