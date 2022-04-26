---
title: HtmlFixedSaveOptions
second_title: Aspose.Words for .NET API Reference
description: 
type: docs
weight: 4680
url: /net/aspose.words.saving/htmlfixedsaveoptions/
---
## HtmlFixedSaveOptions class

Can be used to specify additional options when saving a document into the HtmlFixed format.

```csharp
public class HtmlFixedSaveOptions : FixedPageSaveOptions
```

## Constructors

| Name | Description |
| --- | --- |
| [HtmlFixedSaveOptions](htmlfixedsaveoptions)() | The default constructor. |

## Properties

| Name | Description |
| --- | --- |
| [CssClassNamesPrefix](cssclassnamesprefix) { get; set; } | Specifies prefix which is added to all class names in style.css file. Default value is `"aw"`. |
| [Encoding](encoding) { get; set; } | Specifies the encoding to use when exporting to HTML. Default value is `new UTF8Encoding(true)` (UTF-8 with BOM). |
| [ExportEmbeddedCss](exportembeddedcss) { get; set; } | Specifies whether the CSS (Cascading Style Sheet) should be embedded into Html document. |
| [ExportEmbeddedFonts](exportembeddedfonts) { get; set; } | Specifies whether fonts should be embedded into Html document in Base64 format. Note setting this flag can significantly increase size of output Html file. |
| [ExportEmbeddedImages](exportembeddedimages) { get; set; } | Specifies whether images should be embedded into Html document in Base64 format. Note setting this flag can significantly increase size of output Html file. |
| [ExportEmbeddedSvg](exportembeddedsvg) { get; set; } | Specifies whether SVG resources should be embedded into Html document. Default value is `true`. |
| [ExportFormFields](exportformfields) { get; set; } | Gets or sets indication of whether form fields are exported as interactive items (as 'input' tag) rather than converted to text or graphics. |
| [FontFormat](fontformat) { get; set; } | Gets or sets [`ExportFontFormat`](../exportfontformat) used for font exporting. Default value is Woff. |
| override [OptimizeOutput](optimizeoutput) { get; set; } | Flag indicates whether it is required to optimize output. If this flag is set redundant nested canvases and empty canvases are removed, also neighbor glyphs with the same formating are concatenated. Note: The accuracy of the content display may be affected if this property is set to true. Default is true. |
| [PageHorizontalAlignment](pagehorizontalalignment) { get; set; } | Specifies the horizontal alignment of pages in an HTML document. Default value is `HtmlFixedHorizontalPageAlignment.Center`. |
| [PageMargins](pagemargins) { get; set; } | Specifies the margins around pages in an HTML document. The margins value is measured in points and should be equal to or greater than 0. Default value is 10 points. |
| [ResourceSavingCallback](resourcesavingcallback) { get; set; } | Allows to control how resources (images, fonts and css) are saved when a document is exported to fixed page Html format. |
| [ResourcesFolder](resourcesfolder) { get; set; } | Specifies the physical folder where resources (images, fonts, css) are saved when exporting a document to Html format. Default is `null`. |
| [ResourcesFolderAlias](resourcesfolderalias) { get; set; } | Specifies the name of the folder used to construct image URIs written into an Html document. Default is `null`. |
| [SaveFontFaceCssSeparately](savefontfacecssseparately) { get; set; } | Flag indicates whether "@font-face" CSS rules should be placed into a separate file "fontFaces.css" when a document is being saved with external stylesheet (that is, when [`ExportEmbeddedCss`](./exportembeddedcss) is `false`). Default value is `false`, all CSS rules are written into single file "styles.css". |
| override [SaveFormat](saveformat) { get; set; } | Specifies the format in which the document will be saved if this save options object is used. Can only be HtmlFixed. |
| [ShowPageBorder](showpageborder) { get; set; } | Specifies whether border around pages should be shown. Default is `true`. |
| [UseTargetMachineFonts](usetargetmachinefonts) { get; set; } | Flag indicates whether fonts from target machine must be used to display the document. If this flag is set to true, [`FontFormat`](./fontformat) and [`ExportEmbeddedFonts`](./exportembeddedfonts) properties do not have effect, also [`ResourceSavingCallback`](./resourcesavingcallback) is not fired for fonts. Default is false. |

### Examples

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

* class [FixedPageSaveOptions](../fixedpagesaveoptions)
* namespace [Aspose.Words.Saving](../../aspose.words.saving)
* assembly [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
