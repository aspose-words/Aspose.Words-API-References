﻿---
title: FontSavingArgs.isSubsettingNeeded property
linktitle: isSubsettingNeeded property
articleTitle: isSubsettingNeeded property
second_title: Aspose.Words for Node.js
description: "FontSavingArgs.isSubsettingNeeded property. Allows to specify whether the current font will be subsetted before exporting as a font resource."
type: docs
weight: 60
url: /nodejs-net/aspose.words.saving/fontsavingargs/isSubsettingNeeded/
---

## FontSavingArgs.isSubsettingNeeded property

Allows to specify whether the current font will be subsetted before exporting as a font resource.


```js
get isSubsettingNeeded(): boolean
```

### Remarks

Fonts can be exported as complete original font files or subsetted to include only the characters
that are used in the document. Subsetting allows to reduce the resulting font resource size.

By default, Aspose.Words decides whether to perform subsetting or not by comparing the original font file size 
with the one specified in [HtmlSaveOptions.fontResourcesSubsettingSizeThreshold](../../htmlsaveoptions/fontResourcesSubsettingSizeThreshold/). 
You can override this behavior for individual fonts by setting the [FontSavingArgs.isSubsettingNeeded](./) property.




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

* module [Aspose.Words.Saving](../../)
* class [FontSavingArgs](../)

