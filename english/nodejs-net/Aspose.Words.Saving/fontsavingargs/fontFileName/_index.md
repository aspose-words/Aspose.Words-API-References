---
title: FontSavingArgs.fontFileName property
linktitle: fontFileName property
articleTitle: fontFileName property
second_title: Aspose.Words for Node.js
description: "FontSavingArgs.fontFileName property. Gets or sets the file name (without path) where the font will be saved to."
type: docs
weight: 40
url: /nodejs-net/aspose.words.saving/fontsavingargs/fontFileName/
---

## FontSavingArgs.fontFileName property

Gets or sets the file name (without path) where the font will be saved to.


```js
get fontFileName(): string
```

### Remarks

This property allows you to redefine how the font file names are generated
during export to HTML.

When the event is fired, this property contains the file name that was generated 
by Aspose.Words. You can change the value of this property to save the font into a 
different file. Note that file names must be unique.

Aspose.Words automatically generates a unique file name for every embedded font when 
exporting to HTML format. How the font file name is generated 
depends on whether you save the document to a file or to a stream.

When saving a document to a file, the generated font file name looks like 
*\<document base file name\>.\<original file name\>\<optional suffix\>.\<extension\>*.

When saving a document to a stream, the generated font file name looks like 
*Aspose.Words.\<document guid\>.\<original file name\>\<optional suffix\>.\<extension\>*.

[FontSavingArgs.fontFileName](./) must contain only the file name without the path.
Aspose.Words determines the path for saving using the document file name, 
the [HtmlSaveOptions.fontsFolder](../../htmlsaveoptions/fontsFolder/) and
[HtmlSaveOptions.fontsFolderAlias](../../htmlsaveoptions/fontsFolderAlias/) properties.




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
* property [HtmlSaveOptions.fontsFolder](../../htmlsaveoptions/fontsFolder/)
* property [HtmlSaveOptions.fontsFolderAlias](../../htmlsaveoptions/fontsFolderAlias/)

