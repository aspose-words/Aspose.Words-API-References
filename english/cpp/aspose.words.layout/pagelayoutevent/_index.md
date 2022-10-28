---
title: PageLayoutEvent
second_title: Aspose.Words for C++ API Reference
description: A code of event raised during page layout model build and rendering. Page layout model is built in two steps. First, "conversion step", this is when page layout pulls document content and creates object graph. Second, "reflow step", this is when structures are split, merged and arranged into pages. Depending of the operation which triggered build, page layout model may or may not be further rendered into fixed page format. For example, computing number of pages in the document or updating fields does not require rendering, whereas export to Pdf does.
type: docs
weight: 118
url: /cpp/aspose.words.layout/pagelayoutevent/
---
## PageLayoutEvent enum


A code of event raised during page layout model build and rendering. Page layout model is built in two steps. First, "conversion step", this is when page layout pulls document content and creates object graph. Second, "reflow step", this is when structures are split, merged and arranged into pages. Depending of the operation which triggered build, page layout model may or may not be further rendered into fixed page format. For example, computing number of pages in the document or updating fields does not require rendering, whereas export to Pdf does.

### Values

| Name | Value | Description |
| --- | --- | --- |
| None | 0 | Default value. |
| WatchDog | 1 | Corresponds to a checkpoint in code which is often visited and which is suitable to abort process. While inside [Notify()](../ipagelayoutcallback/notify/) throw custom exception to abort process. You can throw when handling any callback event to abort process. Note that if process is aborted the page layout model remains in undefined state. If process is aborted upon reflow of a complete page, however, it should be possible to use layout model up to the end of that page. |
| BuildStarted | 2 | Build of the page layout has started. Fired once. This is the first event which occurs when [UpdatePageLayout](../../aspose.words/document/updatepagelayout/) is called. |
| BuildFinished | 3 | Build of the page layout has finished. Fired once. This is the last event which occurs when [UpdatePageLayout](../../aspose.words/document/updatepagelayout/) is called. |
| ConversionStarted | 4 | Conversion of document model to page layout has started. Fired once. This occurs when layout model starts pulling document content. |
| ConversionFinished | 5 | Conversion of document model to page layout has finished. Fired once. This occurs when layout model stops pulling document content. |
| ReflowStarted | 6 | Reflow of the page layout has started. Fired once. This occurs when layout model starts reflowing document content. |
| ReflowFinished | 7 | Reflow of the page layout has finished. Fired once. This occurs when layout model stops reflowing document content. |
| PartReflowStarted | 8 | Reflow of the page has started. Note that page may reflow multiple times and that reflow may restart before it is finished. |
| PartReflowFinished | 9 | Reflow of the page has finished. Note that page may reflow multiple times and that reflow may restart before it is finished. |
| PartRenderingStarted | 10 | [Rendering](../../aspose.words.rendering/) of page has started. This is fired once per page. |
| PartRenderingFinished | 11 | [Rendering](../../aspose.words.rendering/) of page has finished. This is fired once per page. |


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

