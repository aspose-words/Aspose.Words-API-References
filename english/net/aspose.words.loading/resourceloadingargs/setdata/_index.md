---
title: ResourceLoadingArgs.SetData
linktitle: SetData
articleTitle: SetData
second_title: Aspose.Words for .NET
description: Discover how the ResourceLoadingArgs SetData method enhances user experience by efficiently managing resource data for optimal performance.
type: docs
weight: 40
url: /net/aspose.words.loading/resourceloadingargs/setdata/
---
## ResourceLoadingArgs.SetData method

Sets user provided data of the resource which is used if [`ResourceLoading`](../../iresourceloadingcallback/resourceloading/) returns UserProvided.

```csharp
public void SetData(byte[] data)
```

## Examples

Shows how to customize the process of loading external resources into a document.

```csharp
public void ResourceLoadingCallback()
{
    Document doc = new Document();
    doc.ResourceLoadingCallback = new ImageNameHandler();

    DocumentBuilder builder = new DocumentBuilder(doc);

    // Images usually are inserted using a URI, or a byte array.
    // Every instance of a resource load will call our callback's ResourceLoading method.
    builder.InsertImage("Google logo");
    builder.InsertImage("Aspose logo");
    builder.InsertImage("Watermark");

    Assert.That(doc.GetChildNodes(NodeType.Shape, true).Count, Is.EqualTo(3));

    doc.Save(ArtifactsDir + "DocumentBase.ResourceLoadingCallback.docx");
}

/// <summary>
/// Allows us to load images into a document using predefined shorthands, as opposed to URIs.
/// This will separate image loading logic from the rest of the document construction.
/// </summary>
private class ImageNameHandler : IResourceLoadingCallback
{
    public ResourceLoadingAction ResourceLoading(ResourceLoadingArgs args)
    {
        // If this callback encounters one of the image shorthands while loading an image,
        // it will apply unique logic for each defined shorthand instead of treating it as a URI.
        if (args.ResourceType == ResourceType.Image)
            switch (args.OriginalUri)
            {
                case "Google logo":
                    using (HttpClient client = new HttpClient())
                    {
                        byte[] imageData = client.GetByteArrayAsync("http://www.google.com/images/logos/ps_logo2.png").GetAwaiter().GetResult();
                        args.SetData(imageData);
                    }

                    return ResourceLoadingAction.UserProvided;

                case "Aspose logo":
                    args.SetData(File.ReadAllBytes(ImageDir + "Logo.jpg"));

                    return ResourceLoadingAction.UserProvided;

                case "Watermark":
                    args.SetData(File.ReadAllBytes(ImageDir + "Transparent background logo.png"));

                    return ResourceLoadingAction.UserProvided;
            }

        return ResourceLoadingAction.Default;
    }
}
```

### See Also

* class [ResourceLoadingArgs](../)
* namespace [Aspose.Words.Loading](../../../aspose.words.loading/)
* assembly [Aspose.Words](../../../)
