---
title: TxtSaveOptions class
linktitle: TxtSaveOptions class
articleTitle: TxtSaveOptions class
second_title: Aspose.Words for NodeJs
description: "Aspose.Words.Saving.TxtSaveOptions class. Can be used to specify additional options when saving a document into the [SaveFormat.Text](../../Aspose.Words/saveformat/#Text) format"
type: docs
weight: 860
url: /nodejs-net/Aspose.Words.Saving/txtsaveoptions/
---

## TxtSaveOptions class

Can be used to specify additional options when saving a document into the [SaveFormat.Text](../../Aspose.Words/saveformat/#Text) format.
To learn more, visit the [Specify Save Options](https://docs.aspose.com/words/nodejs-net/specify-save-options/) documentation article.




**Inheritance:** [TxtSaveOptions](./) → [TxtSaveOptionsBase](../txtsaveoptionsbase/) → [SaveOptions](../saveoptions/)

### Constructors
| Name | Description |
| --- | --- |
| [TxtSaveOptions()](./constructor/#default) | The default constructor. |

### Properties

| Name | Description |
| --- | --- |
| [addBidiMarks](./addBidiMarks/) | Specifies whether to add bi-directional marks before each BiDi run when exporting in plain text format. |
| [allowEmbeddingPostScriptFonts](../saveoptions/allowEmbeddingPostScriptFonts/) | Gets or sets a boolean value indicating whether to allow embedding fonts with PostScript outlines when embedding TrueType fonts in a document upon it is saved. The default value is ``False``.<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [defaultTemplate](../saveoptions/defaultTemplate/) | Gets or sets path to default template (including filename). Default value for this property is **empty string** ().<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [dml3DEffectsRenderingMode](../saveoptions/dml3DEffectsRenderingMode/) | Gets or sets a value determining how 3D effects are rendered.<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [dmlEffectsRenderingMode](../saveoptions/dmlEffectsRenderingMode/) | Gets or sets a value determining how DrawingML effects are rendered.<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [dmlRenderingMode](../saveoptions/dmlRenderingMode/) | Gets or sets a value determining how DrawingML shapes are rendered.<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [encoding](../txtsaveoptionsbase/encoding/) | Specifies the encoding to use when exporting in text formats.  Default value is **Encoding.UTF8**.<br>(Inherited from [TxtSaveOptionsBase](../txtsaveoptionsbase/)) |
| [exportGeneratorName](../saveoptions/exportGeneratorName/) | When ``True``, causes the name and version of Aspose.Words to be embedded into produced files. Default value is ``True``.<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [exportHeadersFootersMode](../txtsaveoptionsbase/exportHeadersFootersMode/) | Specifies the way headers and footers are exported to the text formats. Default value is [TxtExportHeadersFootersMode.PrimaryOnly](../txtexportheadersfootersmode/#PrimaryOnly).<br>(Inherited from [TxtSaveOptionsBase](../txtsaveoptionsbase/)) |
| [forcePageBreaks](../txtsaveoptionsbase/forcePageBreaks/) | Allows to specify whether the page breaks should be preserved during export.<br>(Inherited from [TxtSaveOptionsBase](../txtsaveoptionsbase/)) |
| [imlRenderingMode](../saveoptions/imlRenderingMode/) | Gets or sets a value determining how ink (InkML) objects are rendered.<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [listIndentation](./listIndentation/) | Gets a [TxtListIndentation](../txtlistindentation/) object that specifies how many and which character to use for indentation of list levels. By default it is zero count of character '\\0', that means no indentation. |
| [maxCharactersPerLine](./maxCharactersPerLine/) | Gets or sets an integer value that specifies the maximum number of characters per one line. The default value is 0, that means no limit. |
| [memoryOptimization](../saveoptions/memoryOptimization/) | Gets or sets value determining if memory optimization should be performed before saving the document. Default value for this property is ``False``.<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [paragraphBreak](../txtsaveoptionsbase/paragraphBreak/) | Specifies the string to use as a paragraph break when exporting in text formats.<br>(Inherited from [TxtSaveOptionsBase](../txtsaveoptionsbase/)) |
| [preserveTableLayout](./preserveTableLayout/) | Specifies whether the program should attempt to preserve layout of tables when saving in the plain text format. The default value is ``False``. |
| [prettyFormat](../saveoptions/prettyFormat/) | When ``True``, pretty formats output where applicable. Default value is ``False``.<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [progressCallback](../saveoptions/progressCallback/) | Called during saving a document and accepts data about saving progress.<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [saveFormat](./saveFormat/) | Specifies the format in which the document will be saved if this save options object is used. Can only be [SaveFormat.Text](../../Aspose.Words/saveformat/#Text). |
| [simplifyListLabels](./simplifyListLabels/) | Specifies whether the program should simplify list labels in case of complex label formatting not being adequately represented by plain text. |
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

### Examples

Shows how to save a .txt document with a custom paragraph break.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);

builder.writeln("Paragraph 1.");
builder.writeln("Paragraph 2.");
builder.write("Paragraph 3.");

// Create a "TxtSaveOptions" object, which we can pass to the document's "Save" method
// to modify how we save the document to plaintext.
let txtSaveOptions = new aw.Saving.TxtSaveOptions();

expect(txtSaveOptions.saveFormat).toEqual(aw.SaveFormat.Text);

// Set the "ParagraphBreak" to a custom value that we wish to put at the end of every paragraph.
txtSaveOptions.paragraphBreak = " End of paragraph.\n\n\t";

doc.save(base.artifactsDir + "TxtSaveOptions.paragraphBreak.txt", txtSaveOptions);

let docText = readTextFile(base.artifactsDir + "TxtSaveOptions.paragraphBreak.txt");

expect(docText).toEqual("Paragraph 1. End of paragraph.\n\n\t" +
                        "Paragraph 2. End of paragraph.\n\n\t" +
                        "Paragraph 3. End of paragraph.\n\n\t");
```

### See Also

* module [Aspose.Words.Saving](../)
* class [TxtSaveOptionsBase](../txtsaveoptionsbase/)

