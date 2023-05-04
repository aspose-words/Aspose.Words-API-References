---
title: HtmlFixedSaveOptions.ResourcesFolder
linktitle: ResourcesFolder
articleTitle: ResourcesFolder
second_title: Aspose.Words for .NET
description: HtmlFixedSaveOptions ResourcesFolder property. Specifies the physical folder where resources images fonts css are saved when exporting a document to Html format. Default is null in C#.
type: docs
weight: 140
url: /net/aspose.words.saving/htmlfixedsaveoptions/resourcesfolder/
---
## HtmlFixedSaveOptions.ResourcesFolder property

Specifies the physical folder where resources (images, fonts, css) are saved when exporting a document to Html format. Default is `null`.

```csharp
public string ResourcesFolder { get; set; }
```

## Remarks

Has effect only if [`ExportEmbeddedImages`](../exportembeddedimages/) property is `false`.

When you save a [`Document`](../../../aspose.words/document/) in Html format, Aspose.Words needs to save all images embedded in the document as standalone files. `ResourcesFolder` allows you to specify where the images will be saved and [`ResourcesFolderAlias`](../resourcesfolderalias/) allows to specify how the image URIs will be constructed.

If you save a document into a file and provide a file name, Aspose.Words, by default, saves the images in the same folder where the document file is saved. Use `ResourcesFolder` to override this behavior.

If you save a document into a stream, Aspose.Words does not have a folder where to save the images, but still needs to save the images somewhere. In this case, you need to specify an accessible folder by using the `ResourcesFolder` property

## Examples

Shows how to use a callback to print the URIs of external resources created while converting a document to HTML.

```csharp
public void HtmlFixedResourceFolder()
{
    Document doc = new Document(MyDir + "Rendering.docx");

    ResourceUriPrinter callback = new ResourceUriPrinter();

    HtmlFixedSaveOptions options = new HtmlFixedSaveOptions
    {
        SaveFormat = SaveFormat.HtmlFixed,
        ExportEmbeddedImages = false,
        ResourcesFolder = ArtifactsDir + "HtmlFixedResourceFolder",
        ResourcesFolderAlias = ArtifactsDir + "HtmlFixedResourceFolderAlias",
        ShowPageBorder = false,
        ResourceSavingCallback = callback
    };

    // A folder specified by ResourcesFolderAlias will contain the resources instead of ResourcesFolder.
    // We must ensure the folder exists before the streams can put their resources into it.
    Directory.CreateDirectory(options.ResourcesFolderAlias);

    doc.Save(ArtifactsDir + "HtmlFixedSaveOptions.HtmlFixedResourceFolder.html", options);

    Console.WriteLine(callback.GetText());

    string[] resourceFiles = Directory.GetFiles(ArtifactsDir + "HtmlFixedResourceFolderAlias");

    Assert.False(Directory.Exists(ArtifactsDir + "HtmlFixedResourceFolder"));
    Assert.AreEqual(6, resourceFiles.Count(f => f.EndsWith(".jpeg") || f.EndsWith(".png") || f.EndsWith(".css")));
}

/// <summary>
/// Counts and prints URIs of resources contained by as they are converted to fixed HTML.
/// </summary>
private class ResourceUriPrinter : IResourceSavingCallback
{
    void IResourceSavingCallback.ResourceSaving(ResourceSavingArgs args)
    {
        // If we set a folder alias in the SaveOptions object, we will be able to print it from here.
        mText.AppendLine($"Resource #{++mSavedResourceCount} \"{args.ResourceFileName}\"");

        string extension = Path.GetExtension(args.ResourceFileName);
        switch (extension)
        {
            case ".ttf":
            case ".woff":
            {
                // By default, 'ResourceFileUri' uses system folder for fonts.
                // To avoid problems in other platforms you must explicitly specify the path for the fonts.
                args.ResourceFileUri = ArtifactsDir + Path.DirectorySeparatorChar + args.ResourceFileName;
                break;
            }
        }

        mText.AppendLine("\t" + args.ResourceFileUri);

        // If we have specified a folder in the "ResourcesFolderAlias" property,
        // we will also need to redirect each stream to put its resource in that folder.
        args.ResourceStream = new FileStream(args.ResourceFileUri, FileMode.Create);
        args.KeepResourceStreamOpen = false;
    }

    public string GetText()
    {
        return mText.ToString();
    }

    private int mSavedResourceCount;
    private readonly StringBuilder mText = new StringBuilder();
}
```

### See Also

* class [HtmlFixedSaveOptions](../)
* namespace [Aspose.Words.Saving](../../htmlfixedsaveoptions/)
* assembly [Aspose.Words](../../../)
