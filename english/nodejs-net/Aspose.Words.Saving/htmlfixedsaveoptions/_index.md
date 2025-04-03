---
title: HtmlFixedSaveOptions class
linktitle: HtmlFixedSaveOptions class
articleTitle: HtmlFixedSaveOptions class
second_title: Aspose.Words for NodeJs
description: "Aspose.Words.Saving.HtmlFixedSaveOptions class. Can be used to specify additional options when saving a document into the [SaveFormat.HtmlFixed](../../aspose.words/saveformat/#HtmlFixed) format"
type: docs
weight: 240
url: /nodejs-net/aspose.words.saving/htmlfixedsaveoptions/
---

## HtmlFixedSaveOptions class

Can be used to specify additional options when saving a document into the [SaveFormat.HtmlFixed](../../aspose.words/saveformat/#HtmlFixed) format.
To learn more, visit the [Specify Save Options](https://docs.aspose.com/words/nodejs-net/specify-save-options/) documentation article.




**Inheritance:** [HtmlFixedSaveOptions](./) → [FixedPageSaveOptions](../fixedpagesaveoptions/) → [SaveOptions](../saveoptions/)

### Constructors
| Name | Description |
| --- | --- |
| [HtmlFixedSaveOptions()](./constructor/#default) | The default constructor. |

### Properties

| Name | Description |
| --- | --- |
| [allowEmbeddingPostScriptFonts](../saveoptions/allowEmbeddingPostScriptFonts/) | Gets or sets a boolean value indicating whether to allow embedding fonts with PostScript outlines when embedding TrueType fonts in a document upon it is saved. The default value is ``false``.<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [colorMode](../fixedpagesaveoptions/colorMode/) | Gets or sets a value determining how colors are rendered.<br>(Inherited from [FixedPageSaveOptions](../fixedpagesaveoptions/)) |
| [cssClassNamesPrefix](./cssClassNamesPrefix/) | Specifies prefix which is added to all class names in style.css file. Default value is ``"aw"``. |
| [defaultTemplate](../saveoptions/defaultTemplate/) | Gets or sets path to default template (including filename). Default value for this property is **empty string** ().<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [dml3DEffectsRenderingMode](../saveoptions/dml3DEffectsRenderingMode/) | Gets or sets a value determining how 3D effects are rendered.<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [dmlEffectsRenderingMode](../saveoptions/dmlEffectsRenderingMode/) | Gets or sets a value determining how DrawingML effects are rendered.<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [dmlRenderingMode](../saveoptions/dmlRenderingMode/) | Gets or sets a value determining how DrawingML shapes are rendered.<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [encoding](./encoding/) | Specifies the encoding to use when exporting to HTML. Default value is ``new UTF8Encoding(true)`` (UTF-8 with BOM). |
| [exportEmbeddedCss](./exportEmbeddedCss/) | Specifies whether the CSS (Cascading Style Sheet) should be embedded into Html document. |
| [exportEmbeddedFonts](./exportEmbeddedFonts/) | Specifies whether fonts should be embedded into Html document in Base64 format. Note setting this flag can significantly increase size of output Html file. |
| [exportEmbeddedImages](./exportEmbeddedImages/) | Specifies whether images should be embedded into Html document in Base64 format. Note setting this flag can significantly increase size of output Html file. |
| [exportEmbeddedSvg](./exportEmbeddedSvg/) | Specifies whether SVG resources should be embedded into Html document. Default value is ``true``. |
| [exportFormFields](./exportFormFields/) | Gets or sets indication of whether form fields are exported as interactive items (as 'input' tag) rather than converted to text or graphics. |
| [exportGeneratorName](../saveoptions/exportGeneratorName/) | When ``true``, causes the name and version of Aspose.Words to be embedded into produced files. Default value is ``true``.<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [fontFormat](./fontFormat/) | Gets or sets [ExportFontFormat](../exportfontformat/) used for font exporting. Default value is [ExportFontFormat.Woff](../exportfontformat/#Woff). |
| [idPrefix](./idPrefix/) | Specifies a prefix that is prepended to all generated element IDs in the output document. Default value is null and no prefix is prepended. |
| [imlRenderingMode](../saveoptions/imlRenderingMode/) | Gets or sets a value determining how ink (InkML) objects are rendered.<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [jpegQuality](../fixedpagesaveoptions/jpegQuality/) | Gets or sets a value determining the quality of the JPEG images inside Html document.<br>(Inherited from [FixedPageSaveOptions](../fixedpagesaveoptions/)) |
| [memoryOptimization](../saveoptions/memoryOptimization/) | Gets or sets value determining if memory optimization should be performed before saving the document. Default value for this property is ``false``.<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [metafileRenderingOptions](../fixedpagesaveoptions/metafileRenderingOptions/) | Allows to specify metafile rendering options.<br>(Inherited from [FixedPageSaveOptions](../fixedpagesaveoptions/)) |
| [numeralFormat](../fixedpagesaveoptions/numeralFormat/) | Gets or sets [NumeralFormat](../numeralformat/) used for rendering of numerals. European numerals are used by default.<br>(Inherited from [FixedPageSaveOptions](../fixedpagesaveoptions/)) |
| [optimizeOutput](./optimizeOutput/) | Flag indicates whether it is required to optimize output. If this flag is set redundant nested canvases and empty canvases are removed, also neighbor glyphs with the same formating are concatenated. Note: The accuracy of the content display may be affected if this property is set to ``true``. |
| [pageHorizontalAlignment](./pageHorizontalAlignment/) | Specifies the horizontal alignment of pages in an HTML document. Default value is [HtmlFixedPageHorizontalAlignment.Center](../htmlfixedpagehorizontalalignment/#Center). |
| [pageMargins](./pageMargins/) | Specifies the margins around pages in an HTML document. The margins value is measured in points and should be equal to or greater than 0. Default value is 10 points. |
| [pageSavingCallback](../fixedpagesaveoptions/pageSavingCallback/) | Allows to control how separate pages are saved when a document is exported to fixed page format.<br>(Inherited from [FixedPageSaveOptions](../fixedpagesaveoptions/)) |
| [pageSet](../fixedpagesaveoptions/pageSet/) | Gets or sets the pages to render. Default is all the pages in the document.<br>(Inherited from [FixedPageSaveOptions](../fixedpagesaveoptions/)) |
| [prettyFormat](../saveoptions/prettyFormat/) | When ``true``, pretty formats output where applicable. Default value is ``false``.<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [progressCallback](../saveoptions/progressCallback/) | Called during saving a document and accepts data about saving progress.<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [removeJavaScriptFromLinks](./removeJavaScriptFromLinks/) | Specifies whether JavaScript will be removed from links. Default is ``false``. If this option is enabled, all links containing JavaScript will be replaced with "javascript:void(0)". |
| [resourceSavingCallback](./resourceSavingCallback/) | Allows to control how resources (images, fonts and css) are saved when a document is exported to fixed page Html format. |
| [resourcesFolder](./resourcesFolder/) | Specifies the physical folder where resources (images, fonts, css) are saved when exporting a document to Html format. Default is ``null``. |
| [resourcesFolderAlias](./resourcesFolderAlias/) | Specifies the name of the folder used to construct image URIs written into an Html document. Default is ``null``. |
| [saveFontFaceCssSeparately](./saveFontFaceCssSeparately/) | Flag indicates whether "@font-face" CSS rules should be placed into a separate file "fontFaces.css" when a document is being saved with external stylesheet (that is, when [HtmlFixedSaveOptions.exportEmbeddedCss](./exportEmbeddedCss/) is ``false``). Default value is ``false``, all CSS rules are written into single file "styles.css". |
| [saveFormat](./saveFormat/) | Specifies the format in which the document will be saved if this save options object is used. Can only be [SaveFormat.HtmlFixed](../../aspose.words/saveformat/#HtmlFixed). |
| [showPageBorder](./showPageBorder/) | Specifies whether border around pages should be shown. Default is ``true``. |
| [tempFolder](../saveoptions/tempFolder/) | Specifies the folder for temporary files used when saving to a DOC or DOCX file. By default this property is ``null`` and no temporary files are used.<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [updateAmbiguousTextFont](../saveoptions/updateAmbiguousTextFont/) | Determines whether the font attributes will be changed according to the character code being used.<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [updateCreatedTimeProperty](../saveoptions/updateCreatedTimeProperty/) | Gets or sets a value determining whether the [BuiltInDocumentProperties.createdTime](../../aspose.words.properties/builtindocumentproperties/createdTime/) property is updated before saving. Default value is ``false``;<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [updateFields](../saveoptions/updateFields/) | Gets or sets a value determining if fields of certain types should be updated before saving the document to a fixed page format. Default value for this property is ``true``.<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [updateLastPrintedProperty](../saveoptions/updateLastPrintedProperty/) | Gets or sets a value determining whether the [BuiltInDocumentProperties.lastPrinted](../../aspose.words.properties/builtindocumentproperties/lastPrinted/) property is updated before saving.<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [updateLastSavedTimeProperty](../saveoptions/updateLastSavedTimeProperty/) | Gets or sets a value determining whether the [BuiltInDocumentProperties.lastSavedTime](../../aspose.words.properties/builtindocumentproperties/lastSavedTime/) property is updated before saving.<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [useAntiAliasing](../saveoptions/useAntiAliasing/) | Gets or sets a value determining whether or not to use anti-aliasing for rendering.<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [useHighQualityRendering](../saveoptions/useHighQualityRendering/) | Gets or sets a value determining whether or not to use high quality (i.e. slow) rendering algorithms.<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [useTargetMachineFonts](./useTargetMachineFonts/) | Flag indicates whether fonts from target machine must be used to display the document. If this flag is set to ``true``, [HtmlFixedSaveOptions.fontFormat](./fontFormat/) and [HtmlFixedSaveOptions.exportEmbeddedFonts](./exportEmbeddedFonts/) properties do not have effect, also [HtmlFixedSaveOptions.resourceSavingCallback](./resourceSavingCallback/) is not fired for fonts. Default is ``false``. |

### Methods

| Name | Description |
| --- | --- |
|[ createSaveOptions(saveFormat)](../saveoptions/createSaveOptions/#saveformat) | Creates a save options object of a class suitable for the specified save format.<br>(Inherited from [SaveOptions](../saveoptions/)) |
|[ createSaveOptions(fileName)](../saveoptions/createSaveOptions/#string) | Creates a save options object of a class suitable for the file extension specified in the given file name.<br>(Inherited from [SaveOptions](../saveoptions/)) |

### See Also

* module [Aspose.Words.Saving](../)
* class [FixedPageSaveOptions](../fixedpagesaveoptions/)

