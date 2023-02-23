---
title: ResourceLoadingArgs.ResourceType
linktitle: ResourceType
second_title: Aspose.Words for .NET API Reference
description: ResourceLoadingArgs property. Type of resource in C#.
type: docs
weight: 20
url: /net/aspose.words.loading/resourceloadingargs/resourcetype/
---
## ResourceLoadingArgs.ResourceType property

Type of resource.

```csharp
public ResourceType ResourceType { get; }
```

## Examples

Shows how to customize the process of loading external resources into a document.

```csharp
{
    Document doc = new Document();
    doc.ResourceLoadingCallback = new ImageNameHandler();

    DocumentBuilder builder = new DocumentBuilder(doc);

    // Images usually are inserted using a URI, or a byte array.
    // Every instance of a resource load will call our callback's ResourceLoading method.
    builder.InsertImage("Google logo");
    builder.InsertImage("Aspose logo");
    builder.InsertImage("Watermark");

    Assert.AreEqual(3, doc.GetChildNodes(NodeType.Shape, true).Count);

    doc.Save(ArtifactsDir + "DocumentBase.ResourceLoadingCallback.docx");

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
                    using (WebClient webClient = new WebClient())
                    {
                        args.SetData(webClient.DownloadData("http://www.google.com/images/logos/ps_logo2.png"));
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

* enum [ResourceType](../../resourcetype/)
* class [ResourceLoadingArgs](../)
* namespace [Aspose.Words.Loading](../../resourceloadingargs/)
* assembly [Aspose.Words](../../../)
