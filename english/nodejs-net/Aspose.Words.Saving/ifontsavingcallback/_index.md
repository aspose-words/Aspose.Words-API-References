﻿---
title: IFontSavingCallback class
linktitle: IFontSavingCallback class
articleTitle: IFontSavingCallback class
second_title: Aspose.Words for Node.js
description: "Aspose.Words.Saving.IFontSavingCallback class. Implement this interface if you want to receive notifications and control how Aspose.Words saves fonts when exporting a document to HTML format."
type: docs
weight: 310
url: /nodejs-net/aspose.words.saving/ifontsavingcallback/
---

## IFontSavingCallback class

Implement this interface if you want to receive notifications and control how
Aspose.Words saves fonts when exporting a document to HTML format.


### Methods

| Name | Description |
| --- | --- |
|[ fontSaving(args)](./fontSaving/#fontsavingargs) | Called when Aspose.Words is about to save a font resource. |

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

