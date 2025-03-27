---
title: HtmlSaveOptions.exportFontResources property
linktitle: exportFontResources property
articleTitle: exportFontResources property
second_title: Aspose.Words for NodeJs
description: "HtmlSaveOptions.exportFontResources property. Specifies whether font resources should be exported to HTML, MHTML or EPUB"
type: docs
weight: 140
url: /nodejs-net/Aspose.Words.Saving/htmlsaveoptions/exportFontResources/
---

## HtmlSaveOptions.exportFontResources property

Specifies whether font resources should be exported to HTML, MHTML or EPUB.
Default is ``False``.



```js
get exportFontResources(): boolean
```

### Remarks

Exporting font resources allows for consistent document rendering independent of the fonts available
in a given user's environment.

If [HtmlSaveOptions.exportFontResources](./) is set to ``True``, main HTML document will refer to every font via 
the CSS 3 **@font-face** at-rule and fonts will be output as separate files. When exporting to IDPF EPUB or MHTML 
formats, fonts will be embedded into the corresponding package along with other subsidiary files.

If [HtmlSaveOptions.exportFontsAsBase64](../exportFontsAsBase64/) is set to ``True``, fonts will not be saved to separate files.
Instead, they will be embedded into **@font-face** at-rules in Base64 encoding.

**Important!** When exporting font resources, font licensing issues should be considered. Authors who want to use specific fonts via a downloadable
font mechanism must always carefully verify that their intended use is within the scope of the font license. Many commercial fonts presently do not
allow web downloading of their fonts in any form. License agreements that cover some fonts specifically note that usage via **@font-face** rules
in CSS style sheets is not allowed. Font subsetting can also violate license terms.





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
* class [HtmlSaveOptions](../)
* property [HtmlSaveOptions.fontResourcesSubsettingSizeThreshold](../fontResourcesSubsettingSizeThreshold/)

