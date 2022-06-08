---
title: OptimizeFor
second_title: Aspose.Words for .NET API Reference
description: Allows to optimize the document contents as well as default Aspose.Words behavior to a particular versions of MS Word.
type: docs
weight: 720
url: /net/aspose.words.settings/compatibilityoptions/optimizefor/
---
## CompatibilityOptions.OptimizeFor method

Allows to optimize the document contents as well as default Aspose.Words behavior to a particular versions of MS Word.

Use this method to prevent MS Word from displaying "Compatibility mode" ribbon upon document loading. (Note that you may also need to set the [`Compliance`](../../../aspose.words.saving/ooxmlsaveoptions/compliance) property to Iso29500_2008_Transitional or higher.)

```csharp
public void OptimizeFor(MsWordVersion version)
```

## Examples

Shows how to vertically align the text contents of a text box.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertShape(ShapeType.TextBox, 200, 200);

// Set the "VerticalAnchor" property to "TextBoxAnchor.Top" to
// align the text in this text box with the top side of the shape.
// Set the "VerticalAnchor" property to "TextBoxAnchor.Middle" to
// align the text in this text box to the center of the shape.
// Set the "VerticalAnchor" property to "TextBoxAnchor.Bottom" to
// align the text in this text box to the bottom of the shape.
shape.TextBox.VerticalAnchor = verticalAnchor;

builder.MoveTo(shape.FirstParagraph);
builder.Write("Hello world!");

// The vertical aligning of text inside text boxes is available from Microsoft Word 2007 onwards.
doc.CompatibilityOptions.OptimizeFor(MsWordVersion.Word2007);
doc.Save(ArtifactsDir + "Shape.VerticalAnchor.docx");
```

Shows how to set an OOXML compliance specification for a saved document to adhere to.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// If we configure compatibility options to comply with Microsoft Word 2003,
// inserting an image will define its shape using VML.
doc.CompatibilityOptions.OptimizeFor(MsWordVersion.Word2003);
builder.InsertImage(ImageDir + "Transparent background logo.png");

Assert.AreEqual(ShapeMarkupLanguage.Vml, ((Shape)doc.GetChild(NodeType.Shape, 0, true)).MarkupLanguage);

// The "ISO/IEC 29500:2008" OOXML standard does not support VML shapes.
// If we set the "Compliance" property of the SaveOptions object to "OoxmlCompliance.Iso29500_2008_Strict",
// any document we save while passing this object will have to follow that standard. 
OoxmlSaveOptions saveOptions = new OoxmlSaveOptions
{
    Compliance = OoxmlCompliance.Iso29500_2008_Strict,
    SaveFormat = SaveFormat.Docx
};

doc.Save(ArtifactsDir + "OoxmlSaveOptions.Iso29500Strict.docx", saveOptions);

// Our saved document defines the shape using DML to adhere to the "ISO/IEC 29500:2008" OOXML standard.
doc = new Document(ArtifactsDir + "OoxmlSaveOptions.Iso29500Strict.docx");

Assert.AreEqual(ShapeMarkupLanguage.Dml, ((Shape)doc.GetChild(NodeType.Shape, 0, true)).MarkupLanguage);
```

Shows how to optimize the document for different versions of Microsoft Word.

```csharp
public void OptimizeFor()
{
    Document doc = new Document();

    // This object contains an extensive list of flags unique to each document
    // that allow us to facilitate backward compatibility with older versions of Microsoft Word.
    CompatibilityOptions options = doc.CompatibilityOptions;

    // Print the default settings for a blank document.
    Console.WriteLine("\nDefault optimization settings:");
    PrintCompatibilityOptions(options);

    // We can access these settings in Microsoft Word via "File" -> "Options" -> "Advanced" -> "Compatibility options for...".
    doc.Save(ArtifactsDir + "CompatibilityOptions.OptimizeFor.DefaultSettings.docx");

    // We can use the OptimizeFor method to ensure optimal compatibility with a specific Microsoft Word version.
    doc.CompatibilityOptions.OptimizeFor(MsWordVersion.Word2010);
    Console.WriteLine("\nOptimized for Word 2010:");
    PrintCompatibilityOptions(options);

    doc.CompatibilityOptions.OptimizeFor(MsWordVersion.Word2000);
    Console.WriteLine("\nOptimized for Word 2000:");
    PrintCompatibilityOptions(options);
}

/// <summary>
/// Groups all flags in a document's compatibility options object by state, then prints each group.
/// </summary>
private static void PrintCompatibilityOptions(CompatibilityOptions options)
{
    for (int i = 1; i >= 0; i--)
    {
        Console.WriteLine(Convert.ToBoolean(i) ? "\tEnabled options:" : "\tDisabled options:");
        SortedSet<string> optionNames = new SortedSet<string>();

        foreach (System.ComponentModel.PropertyDescriptor descriptor in System.ComponentModel.TypeDescriptor.GetProperties(options))
        {
            if (descriptor.PropertyType == Type.GetType("System.Boolean") && i == Convert.ToInt32(descriptor.GetValue(options)))
            {
                optionNames.Add(descriptor.Name);
            }
        }

        foreach (string s in optionNames)
        {
            Console.WriteLine($"\t\t{s}");
        }
    }
}
```

### See Also

* enum [MsWordVersion](../../mswordversion)
* class [CompatibilityOptions](../../compatibilityoptions)
* namespace [Aspose.Words.Settings](../../compatibilityoptions)
* assembly [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
