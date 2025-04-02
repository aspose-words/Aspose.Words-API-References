---
title: MarkdownSaveOptions class
linktitle: MarkdownSaveOptions class
articleTitle: MarkdownSaveOptions class
second_title: Aspose.Words for NodeJs
description: "Aspose.Words.Saving.MarkdownSaveOptions class. Class to specify additional options when saving a document into the [SaveFormat.Markdown](../../Aspose.Words/saveformat/#Markdown) format"
type: docs
weight: 460
url: /nodejs-net/Aspose.Words.Saving/markdownsaveoptions/
---

## MarkdownSaveOptions class

Class to specify additional options when saving a document into the [SaveFormat.Markdown](../../Aspose.Words/saveformat/#Markdown) format.
To learn more, visit the [Specify Save Options](https://docs.aspose.com/words/nodejs-net/specify-save-options/) documentation article.




**Inheritance:** [MarkdownSaveOptions](./) → [TxtSaveOptionsBase](../txtsaveoptionsbase/) → [SaveOptions](../saveoptions/)

### Constructors
| Name | Description |
| --- | --- |
| [MarkdownSaveOptions()](./constructor/#default) | Initializes a new instance of this class that can be used to save a document in the [SaveFormat.Markdown](../../Aspose.Words/saveformat/#Markdown) format. |

### Properties

| Name | Description |
| --- | --- |
| [allowEmbeddingPostScriptFonts](../saveoptions/allowEmbeddingPostScriptFonts/) | Gets or sets a boolean value indicating whether to allow embedding fonts with PostScript outlines when embedding TrueType fonts in a document upon it is saved. The default value is ``False``.<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [defaultTemplate](../saveoptions/defaultTemplate/) | Gets or sets path to default template (including filename). Default value for this property is **empty string** ().<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [dml3DEffectsRenderingMode](../saveoptions/dml3DEffectsRenderingMode/) | Gets or sets a value determining how 3D effects are rendered.<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [dmlEffectsRenderingMode](../saveoptions/dmlEffectsRenderingMode/) | Gets or sets a value determining how DrawingML effects are rendered.<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [dmlRenderingMode](../saveoptions/dmlRenderingMode/) | Gets or sets a value determining how DrawingML shapes are rendered.<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [encoding](../txtsaveoptionsbase/encoding/) | Specifies the encoding to use when exporting in text formats.  Default value is **Encoding.UTF8**.<br>(Inherited from [TxtSaveOptionsBase](../txtsaveoptionsbase/)) |
| [exportAsHtml](./exportAsHtml/) | Allows to specify the elements to be exported to Markdown as raw HTML. Default value is [MarkdownExportAsHtml.None](../markdownexportashtml/#None). |
| [exportGeneratorName](../saveoptions/exportGeneratorName/) | When ``True``, causes the name and version of Aspose.Words to be embedded into produced files. Default value is ``True``.<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [exportHeadersFootersMode](../txtsaveoptionsbase/exportHeadersFootersMode/) | Specifies the way headers and footers are exported to the text formats. Default value is [TxtExportHeadersFootersMode.PrimaryOnly](../txtexportheadersfootersmode/#PrimaryOnly).<br>(Inherited from [TxtSaveOptionsBase](../txtsaveoptionsbase/)) |
| [exportImagesAsBase64](./exportImagesAsBase64/) | Specifies whether images are saved in Base64 format to the output file. Default value is ``False``. |
| [exportUnderlineFormatting](./exportUnderlineFormatting/) | Gets or sets a boolean value indicating either to export underline text formatting as sequence of two plus characters "++". The default value is ``False``. |
| [forcePageBreaks](../txtsaveoptionsbase/forcePageBreaks/) | Allows to specify whether the page breaks should be preserved during export.<br>(Inherited from [TxtSaveOptionsBase](../txtsaveoptionsbase/)) |
| [imageResolution](./imageResolution/) | Specifies the output resolution for images when exporting to Markdown. Default is ``96 dpi``. |
| [imageSavingCallback](./imageSavingCallback/) | Allows to control how images are saved when a document is saved to [SaveFormat.Markdown](../../Aspose.Words/saveformat/#Markdown) format. |
| [imagesFolder](./imagesFolder/) | Specifies the physical folder where images are saved when exporting a document to the [SaveFormat.Markdown](../../Aspose.Words/saveformat/#Markdown) format. Default is an empty string. |
| [imagesFolderAlias](./imagesFolderAlias/) | Specifies the name of the folder used to construct image URIs written into a document. Default is an empty string. |
| [imlRenderingMode](../saveoptions/imlRenderingMode/) | Gets or sets a value determining how ink (InkML) objects are rendered.<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [linkExportMode](./linkExportMode/) | Specifies how links will be written to the output file. Default value is [MarkdownLinkExportMode.Auto](../markdownlinkexportmode/#Auto). |
| [listExportMode](./listExportMode/) | Specifies how list items will be written to the output file. Default value is [MarkdownListExportMode.MarkdownSyntax](../markdownlistexportmode/#MarkdownSyntax). |
| [memoryOptimization](../saveoptions/memoryOptimization/) | Gets or sets value determining if memory optimization should be performed before saving the document. Default value for this property is ``False``.<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [officeMathExportMode](./officeMathExportMode/) | Specifies how OfficeMath will be written to the output file. Default value is [MarkdownOfficeMathExportMode.Text](../markdownofficemathexportmode/#Text). |
| [paragraphBreak](../txtsaveoptionsbase/paragraphBreak/) | Specifies the string to use as a paragraph break when exporting in text formats.<br>(Inherited from [TxtSaveOptionsBase](../txtsaveoptionsbase/)) |
| [prettyFormat](../saveoptions/prettyFormat/) | When ``True``, pretty formats output where applicable. Default value is ``False``.<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [progressCallback](../saveoptions/progressCallback/) | Called during saving a document and accepts data about saving progress.<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [saveFormat](./saveFormat/) | Specifies the format in which the document will be saved if this save options object is used. Can only be [SaveFormat.Markdown](../../Aspose.Words/saveformat/#Markdown). |
| [tableContentAlignment](./tableContentAlignment/) | Gets or sets a value that specifies how to align contents in tables when exporting into the [SaveFormat.Markdown](../../Aspose.Words/saveformat/#Markdown) format. The default value is [TableContentAlignment.Auto](../tablecontentalignment/#Auto). |
| [tempFolder](../saveoptions/tempFolder/) | Specifies the folder for temporary files used when saving to a DOC or DOCX file. By default this property is ``None`` and no temporary files are used.<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [updateAmbiguousTextFont](../saveoptions/updateAmbiguousTextFont/) | Determines whether the font attributes will be changed according to the character code being used.<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [updateCreatedTimeProperty](../saveoptions/updateCreatedTimeProperty/) | Gets or sets a value determining whether the [BuiltInDocumentProperties.createdTime](../../Aspose.Words.Properties/builtindocumentproperties/createdTime/) property is updated before saving. Default value is ``False``;<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [updateFields](../saveoptions/updateFields/) | Gets or sets a value determining if fields of certain types should be updated before saving the document to a fixed page format. Default value for this property is ``True``.<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [updateLastPrintedProperty](../saveoptions/updateLastPrintedProperty/) | Gets or sets a value determining whether the [BuiltInDocumentProperties.lastPrinted](../../Aspose.Words.Properties/builtindocumentproperties/lastPrinted/) property is updated before saving.<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [updateLastSavedTimeProperty](../saveoptions/updateLastSavedTimeProperty/) | Gets or sets a value determining whether the [BuiltInDocumentProperties.lastSavedTime](../../Aspose.Words.Properties/builtindocumentproperties/lastSavedTime/) property is updated before saving.<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [useAntiAliasing](../saveoptions/useAntiAliasing/) | Gets or sets a value determining whether or not to use anti-aliasing for rendering.<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [useHighQualityRendering](../saveoptions/useHighQualityRendering/) | Gets or sets a value determining whether or not to use high quality (i.e. slow) rendering algorithms.<br>(Inherited from [SaveOptions](../saveoptions/)) |

### Methods

| Name | Description |
| --- | --- |
|[ createSaveOptions(saveFormat)](../saveoptions/createSaveOptions/#saveformat) | Creates a save options object of a class suitable for the specified save format.<br>(Inherited from [SaveOptions](../saveoptions/)) |
|[ createSaveOptions(fileName)](../saveoptions/createSaveOptions/#string) | Creates a save options object of a class suitable for the file extension specified in the given file name.<br>(Inherited from [SaveOptions](../saveoptions/)) |

### See Also

* module [Aspose.Words.Saving](../)
* class [TxtSaveOptionsBase](../txtsaveoptionsbase/)

