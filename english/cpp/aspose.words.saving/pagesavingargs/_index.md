---
title: PageSavingArgs
second_title: Aspose.Words for C++ API Reference
description: Provides data for the PageSaving() event.
type: docs
weight: 235
url: /cpp/aspose.words.saving/pagesavingargs/
---
## PageSavingArgs class


Provides data for the [PageSaving()](../ipagesavingcallback/pagesaving/) event.

```cpp
class PageSavingArgs : public System::Object
```

## Methods

| Method | Description |
| --- | --- |
| [get_KeepPageStreamOpen](./get_keeppagestreamopen/)() const | Specifies whether Aspose.Words should keep the stream open or close it after saving a document page. |
| [get_PageFileName](./get_pagefilename/)() const | Gets or sets the file name where the document page will be saved to. |
| [get_PageIndex](./get_pageindex/)() const | Current page index. |
| [get_PageStream](./get_pagestream/)() const | Allows to specify the stream where the document page will be saved to. |
| [PageSavingArgs](./pagesavingargs/)() |  |
| [set_KeepPageStreamOpen](./set_keeppagestreamopen/)(bool) | Setter for [Aspose::Words::Saving::PageSavingArgs::get_KeepPageStreamOpen](./get_keeppagestreamopen/). |
| [set_PageFileName](./set_pagefilename/)(const System::String\&) | Setter for [Aspose::Words::Saving::PageSavingArgs::get_PageFileName](./get_pagefilename/). |
| [set_PageStream](./set_pagestream/)(const System::SharedPtr\<System::IO::Stream\>\&) | Setter for [Aspose::Words::Saving::PageSavingArgs::get_PageStream](./get_pagestream/). |
| [set_PageStream](./set_pagestream/)(std::basic_ostream\<CharType, Traits\>\&) |  |

## Examples



Shows how to use a callback to save a document to HTML page by page. 
```cpp
void PageFileNames()
{
    auto doc = MakeObject<Document>();
    auto builder = MakeObject<DocumentBuilder>(doc);

    builder->Writeln(u"Page 1.");
    builder->InsertBreak(BreakType::PageBreak);
    builder->Writeln(u"Page 2.");
    builder->InsertImage(ImageDir + u"Logo.jpg");
    builder->InsertBreak(BreakType::PageBreak);
    builder->Writeln(u"Page 3.");

    // Create an "HtmlFixedSaveOptions" object, which we can pass to the document's "Save" method
    // to modify how we convert the document to HTML.
    auto htmlFixedSaveOptions = MakeObject<HtmlFixedSaveOptions>();

    // We will save each page in this document to a separate HTML file in the local file system.
    // Set a callback that allows us to name each output HTML document.
    htmlFixedSaveOptions->set_PageSavingCallback(MakeObject<ExSavingCallback::CustomFileNamePageSavingCallback>());

    doc->Save(ArtifactsDir + u"SavingCallback.PageFileNames.html", htmlFixedSaveOptions);

    ArrayPtr<String> filePaths = System::IO::Directory::GetFiles(ArtifactsDir)
                                     ->LINQ_Where([](String s) { return s.StartsWith(ArtifactsDir + u"SavingCallback.PageFileNames.Page_"); })
                                     ->LINQ_ToArray();

    ASSERT_EQ(3, filePaths->get_Length());
}

class CustomFileNamePageSavingCallback : public IPageSavingCallback
{
public:
    void PageSaving(SharedPtr<PageSavingArgs> args) override
    {
        String outFileName = String::Format(u"{0}SavingCallback.PageFileNames.Page_{1}.html", ArtifactsDir, args->get_PageIndex());

        // Below are two ways of specifying where Aspose.Words will save each page of the document.
        // 1 -  Set a filename for the output page file:
        args->set_PageFileName(outFileName);

        // 2 -  Create a custom stream for the output page file:
        args->set_PageStream(MakeObject<System::IO::FileStream>(outFileName, System::IO::FileMode::Create));

        ASSERT_FALSE(args->get_KeepPageStreamOpen());
    }
};
```

## See Also

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words](../../)
