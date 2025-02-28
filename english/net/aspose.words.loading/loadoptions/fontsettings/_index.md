---
title: LoadOptions.FontSettings
linktitle: FontSettings
articleTitle: FontSettings
second_title: Aspose.Words for .NET
description: Customize your document's font settings with LoadOptions FontSettings for enhanced readability and style. Optimize your documents effortlessly!
type: docs
weight: 60
url: /net/aspose.words.loading/loadoptions/fontsettings/
---
## LoadOptions.FontSettings property

Allows to specify document font settings.

```csharp
public FontSettings FontSettings { get; set; }
```

## Remarks

When loading some formats, Aspose.Words may require to resolve the fonts. For example, when loading HTML documents Aspose.Words may resolve the fonts to perform font fallback.

If set to `null`, default static font settings [`DefaultInstance`](../../../aspose.words.fonts/fontsettings/defaultinstance/) will be used.

The default value is `null`.

## Examples

Shows how to apply font substitution settings while loading a document.

```csharp
// Create a FontSettings object that will substitute the "Times New Roman" font
// with the font "Arvo" from our "MyFonts" folder.
FontSettings fontSettings = new FontSettings();
fontSettings.SetFontsFolder(FontsDir, false);
fontSettings.SubstitutionSettings.TableSubstitution.AddSubstitutes("Times New Roman", "Arvo");

// Set that FontSettings object as a property of a newly created LoadOptions object.
LoadOptions loadOptions = new LoadOptions();
loadOptions.FontSettings = fontSettings;

// Load the document, then render it as a PDF with the font substitution.
Document doc = new Document(MyDir + "Document.docx", loadOptions);

doc.Save(ArtifactsDir + "LoadOptions.FontSettings.pdf");
```

Shows how to designate font substitutes during loading.

```csharp
LoadOptions loadOptions = new LoadOptions();
loadOptions.FontSettings = new FontSettings();

// Set a font substitution rule for a LoadOptions object.
// If the document we are loading uses a font which we do not have,
// this rule will substitute the unavailable font with one that does exist.
// In this case, all uses of the "MissingFont" will convert to "Comic Sans MS".
TableSubstitutionRule substitutionRule = loadOptions.FontSettings.SubstitutionSettings.TableSubstitution;
substitutionRule.AddSubstitutes("MissingFont", "Comic Sans MS");

Document doc = new Document(MyDir + "Missing font.html", loadOptions);

// At this point such text will still be in "MissingFont".
// Font substitution will take place when we render the document.
Assert.AreEqual("MissingFont", doc.FirstSection.Body.FirstParagraph.Runs[0].Font.Name);

doc.Save(ArtifactsDir + "FontSettings.ResolveFontsBeforeLoadingDocument.pdf");
```

### See Also

* class [FontSettings](../../../aspose.words.fonts/fontsettings/)
* class [LoadOptions](../)
* namespace [Aspose.Words.Loading](../../../aspose.words.loading/)
* assembly [Aspose.Words](../../../)
