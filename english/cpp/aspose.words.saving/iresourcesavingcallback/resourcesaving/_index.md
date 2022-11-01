---
title: ResourceSaving
second_title: Aspose.Words for C++ API Reference
description: Called when Aspose.Words saves an external resource to fixed page HTML or SVG formats.
type: docs
weight: 1
url: /cpp/aspose.words.saving/iresourcesavingcallback/resourcesaving/
---
## IResourceSavingCallback.ResourceSaving method


Called when Aspose.Words saves an external resource to fixed page HTML or SVG formats.

```cpp
virtual void Aspose::Words::Saving::IResourceSavingCallback::ResourceSaving(System::SharedPtr<Aspose::Words::Saving::ResourceSavingArgs> args)=0
```


## Examples




Shows how to use a callback to track external resources created while converting a document to HTML. 
```cpp
void ResourceSavingCallback()
{
    auto doc = MakeObject<Document>(MyDir + u"Bullet points with alternative font.docx");

    auto callback = MakeObject<ExHtmlFixedSaveOptions::FontSavingCallback>();

    auto saveOptions = MakeObject<HtmlFixedSaveOptions>();
    saveOptions->set_ResourceSavingCallback(callback);

    doc->Save(ArtifactsDir + u"HtmlFixedSaveOptions.UsingMachineFonts.html", saveOptions);

    std::cout << callback->GetText() << std::endl;
}

class FontSavingCallback : public IResourceSavingCallback
{
public:
    void ResourceSaving(SharedPtr<ResourceSavingArgs> args) override
    {
        mText->AppendLine(String::Format(u"Original document URI:\t{0}", args->get_Document()->get_OriginalFileName()));
        mText->AppendLine(String::Format(u"Resource being saved:\t{0}", args->get_ResourceFileName()));
        mText->AppendLine(String::Format(u"Full uri after saving:\t{0}\n", args->get_ResourceFileUri()));
    }

    String GetText()
    {
        return mText->ToString();
    }

    FontSavingCallback() : mText(MakeObject<System::Text::StringBuilder>())
    {
    }

private:
    SharedPtr<System::Text::StringBuilder> mText;
};
```


Shows how to use a callback to print the URIs of external resources created while converting a document to HTML. 
```cpp
void HtmlFixedResourceFolder()
{
    auto doc = MakeObject<Document>(MyDir + u"Rendering.docx");

    auto callback = MakeObject<ExHtmlFixedSaveOptions::ResourceUriPrinter>();

    auto options = MakeObject<HtmlFixedSaveOptions>();
    options->set_SaveFormat(SaveFormat::HtmlFixed);
    options->set_ExportEmbeddedImages(false);
    options->set_ResourcesFolder(ArtifactsDir + u"HtmlFixedResourceFolder");
    options->set_ResourcesFolderAlias(ArtifactsDir + u"HtmlFixedResourceFolderAlias");
    options->set_ShowPageBorder(false);
    options->set_ResourceSavingCallback(callback);

    // A folder specified by ResourcesFolderAlias will contain the resources instead of ResourcesFolder.
    // We must ensure the folder exists before the streams can put their resources into it.
    System::IO::Directory::CreateDirectory_(options->get_ResourcesFolderAlias());

    doc->Save(ArtifactsDir + u"HtmlFixedSaveOptions.HtmlFixedResourceFolder.html", options);

    std::cout << callback->GetText() << std::endl;

    ArrayPtr<String> resourceFiles = System::IO::Directory::GetFiles(ArtifactsDir + u"HtmlFixedResourceFolderAlias");

    ASSERT_FALSE(System::IO::Directory::Exists(ArtifactsDir + u"HtmlFixedResourceFolder"));
    std::function<bool(String f)> isImageOrCss = [](String f)
    {
        return f.EndsWith(u".jpeg") || f.EndsWith(u".png") || f.EndsWith(u".css");
    };

    ASSERT_EQ(6, resourceFiles->LINQ_Count(isImageOrCss));
}

class ResourceUriPrinter : public IResourceSavingCallback
{
public:
    String GetText()
    {
        return mText->ToString();
    }

    ResourceUriPrinter() : mSavedResourceCount(0), mText(MakeObject<System::Text::StringBuilder>())
    {
    }

private:
    int mSavedResourceCount;
    SharedPtr<System::Text::StringBuilder> mText;

    void ResourceSaving(SharedPtr<ResourceSavingArgs> args) override
    {
        // If we set a folder alias in the SaveOptions object, we will be able to print it from here.
        mText->AppendLine(String::Format(u"Resource #{0} \"{1}\"", ++mSavedResourceCount, args->get_ResourceFileName()));

        String extension = System::IO::Path::GetExtension(args->get_ResourceFileName());
        if (extension == u".ttf" || extension == u".woff")
        {
            // By default, 'ResourceFileUri' uses system folder for fonts.
            // To avoid problems in other platforms you must explicitly specify the path for the fonts.
            args->set_ResourceFileUri(ArtifactsDir + System::IO::Path::DirectorySeparatorChar + args->get_ResourceFileName());
        }

        mText->AppendLine(String(u"\t") + args->get_ResourceFileUri());

        // If we have specified a folder in the "ResourcesFolderAlias" property,
        // we will also need to redirect each stream to put its resource in that folder.
        args->set_ResourceStream(MakeObject<System::IO::FileStream>(args->get_ResourceFileUri(), System::IO::FileMode::Create));
        args->set_KeepResourceStreamOpen(false);
    }
};
```

