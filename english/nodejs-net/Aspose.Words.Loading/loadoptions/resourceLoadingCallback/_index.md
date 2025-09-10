---
title: LoadOptions.resourceLoadingCallback property
linktitle: resourceLoadingCallback property
articleTitle: resourceLoadingCallback property
second_title: Aspose.Words for Node.js
description: "LoadOptions.resourceLoadingCallback property. Allows to control how external resources (images, style sheets) are loaded when a document is imported from HTML, MHTML."
type: docs
weight: 140
url: /nodejs-net/aspose.words.loading/loadoptions/resourceLoadingCallback/
---

## LoadOptions.resourceLoadingCallback property

Allows to control how external resources (images, style sheets) are loaded when a document is imported from HTML, MHTML.


```js
get resourceLoadingCallback(): Aspose.Words.Loading.IResourceLoadingCallback
```

### Examples

Shows how to handle external resources when loading Html documents.

```js
test.skip('LoadOptionsCallback - TODO: WORDSNODEJS-121 - Add support of loadOptions.resourceLoadingCallback', () => {
    let loadOptions = new aw.Loading.LoadOptions();
    loadOptions.resourceLoadingCallback = new HtmlLinkedResourceLoadingCallback();

    // When we load the document, our callback will handle linked resources such as CSS stylesheets and images.
    let doc = new aw.Document(base.myDir + "Images.html", loadOptions);
    doc.save(base.artifactsDir + "LoadOptions.LoadOptionsCallback.pdf");
  });


/*  
    /// <summary>
    /// Prints the filenames of all external stylesheets and substitutes all images of a loaded html document.
    /// </summary>
  private class HtmlLinkedResourceLoadingCallback : IResourceLoadingCallback
  {
    public ResourceLoadingAction ResourceLoading(ResourceLoadingArgs args)
    {
      switch (args.resourceType)
      {
        case aw.Loading.ResourceType.CssStyleSheet:
          console.log(`External CSS Stylesheet found upon loading: ${args.originalUri}`);
          return aw.Loading.ResourceLoadingAction.Default;
        case aw.Loading.ResourceType.Image:
          console.log(`External Image found upon loading: ${args.originalUri}`);

          const string newImageFilename = "Logo.jpg";
          console.log(`\tImage will be substituted with: ${newImageFilename}`);

          Image newImage = Image.FromFile(base.imageDir + newImageFilename);

          let converter = new ImageConverter();
          byte.at(] imageBytes = (byte[))converter.ConvertTo(newImage, typeof(byte[]));
          args.setData(imageBytes);

          return aw.Loading.ResourceLoadingAction.UserProvided;
      }

      return aw.Loading.ResourceLoadingAction.Default;
    }
  }
```

### See Also

* module [Aspose.Words.Loading](../../)
* class [LoadOptions](../)

