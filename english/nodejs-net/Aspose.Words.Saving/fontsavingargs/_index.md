---
title: FontSavingArgs class
linktitle: FontSavingArgs class
articleTitle: FontSavingArgs class
second_title: Aspose.Words for NodeJs
description: "Aspose.Words.Saving.FontSavingArgs class. Provides data for the [IFontSavingCallback.fontSaving()](../ifontsavingcallback/fontSaving/#fontsavingargs) event"
type: docs
weight: 200
url: /nodejs-net/Aspose.Words.Saving/fontsavingargs/
---

## FontSavingArgs class

Provides data for the [IFontSavingCallback.fontSaving()](../ifontsavingcallback/fontSaving/#fontsavingargs) event.
To learn more, visit the [Save a Document](https://docs.aspose.com/words/nodejs-net/save-a-document/) documentation article.




### Remarks

When Aspose.Words saves a document to HTML or related formats and [HtmlSaveOptions.exportFontResources](../htmlsaveoptions/exportFontResources/) 
is set to ``True``, it saves each font subject for export into a separate file.

[FontSavingArgs](./) controls whether particular font resource should be exported and how.

[FontSavingArgs](./) also allows to redefine how font file names are generated or to 
completely circumvent saving of fonts into files by providing your own stream objects.

To decide whether to save a particular font resource, use the [FontSavingArgs.isExportNeeded](./isExportNeeded/) property.

To save fonts into streams instead of files, use the Aspose.Words.Saving.FontSavingArgs.FontStream property.




### Properties

| Name | Description |
| --- | --- |
| [bold](./bold/) | Indicates whether the current font is bold. |
| [document](./document/) | Gets the document object that is being saved. |
| [fontFamilyName](./fontFamilyName/) | Indicates the current font family name. |
| [fontFileName](./fontFileName/) | Gets or sets the file name (without path) where the font will be saved to. |
| [isExportNeeded](./isExportNeeded/) | Allows to specify whether the current font will be exported as a font resource. Default is ``True``. |
| [isSubsettingNeeded](./isSubsettingNeeded/) | Allows to specify whether the current font will be subsetted before exporting as a font resource. |
| [italic](./italic/) | Indicates whether the current font is italic. |
| [keepFontStreamOpen](./keepFontStreamOpen/) | Specifies whether Aspose.Words should keep the stream open or close it after saving a font. |
| [originalFileName](./originalFileName/) | Gets the original font file name with an extension. |
| [originalFileSize](./originalFileSize/) | Gets the original font file size. |

### Examples

Shows how to define custom logic for exporting fonts when saving to HTML.

```js
test.skip('SaveExportedFonts - TODO: fontSavingCallback not supported yet', () => {
    let doc = new aw.Document(base.myDir + "Rendering.docx");

    // Configure a SaveOptions object to export fonts to separate files.
    // Set a callback that will handle font saving in a custom manner.
    let options = new aw.Saving.HtmlSaveOptions
    options.exportFontResources = true,
    options.fontSavingCallback = new HandleFontSaving();

    // The callback will export .ttf files and save them alongside the output document.
    doc.save(base.artifactsDir + "HtmlSaveOptions.SaveExportedFonts.html", options);

    for (var fontFilename of fs.readdirSync(base.artifactsDir).filter((s) => s.endsWith(".ttf")))
    {
      console.log(fontFilename);
    }

    expect(fs.readdirSync(base.artifactsDir).filter((s) => s.endsWith(".ttf")).count).toEqual(10);
  });

/*
  /// <summary>
  /// Prints information about exported fonts and saves them in the same local system folder as their output .html.
  /// </summary>
  public class HandleFontSaving : IFontSavingCallback
  {
    void aw.Saving.IFontSavingCallback.fontSaving(FontSavingArgs args)
    {
      Console.write(`Font:\t${args.fontFamilyName}`);
      if (args.bold) Console.write(", bold");
      if (args.italic) Console.write(", italic");
      console.log(`\nSource:\t${args.originalFileName}, ${args.originalFileSize} bytes\n`);

        // We can also access the source document from here.
      expect(args.document.originalFileName.EndsWith("Rendering.docx")).toEqual(true);

      expect(args.isExportNeeded).toEqual(true);
      expect(args.isSubsettingNeeded).toEqual(true);

        // There are two ways of saving an exported font.
        // 1 -  Save it to a local file system location:
      args.fontFileName = args.originalFileName.split(Path.DirectorySeparatorChar).Last();

        // 2 -  Save it to a stream:
      args.fontStream =
        new FileStream(base.artifactsDir + args.originalFileName.split(Path.DirectorySeparatorChar).Last(), FileMode.create);
      expect(args.keepFontStreamOpen).toEqual(false);
    }
  }
```

### See Also

* module [Aspose.Words.Saving](../)

