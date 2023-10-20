---
title: CompatibilityOptions.OptimizeFor
linktitle: OptimizeFor
articleTitle: OptimizeFor
second_title: Aspose.Words für .NET
description: CompatibilityOptions OptimizeFor methode. Ermöglicht die Optimierung des Dokumentinhalts sowie des Standardverhaltens von Aspose.Words für bestimmte Versionen von MS Word in C#.
type: docs
weight: 720
url: /de/net/aspose.words.settings/compatibilityoptions/optimizefor/
---
## CompatibilityOptions.OptimizeFor method

Ermöglicht die Optimierung des Dokumentinhalts sowie des Standardverhaltens von Aspose.Words für bestimmte Versionen von MS Word.

Verwenden Sie diese Methode, um zu verhindern, dass MS Word beim Laden des Dokuments das Menüband „Kompatibilitätsmodus“ anzeigt. (Beachten Sie, dass Sie möglicherweise auch festlegen müssen[`Compliance`](../../../aspose.words.saving/ooxmlsaveoptions/compliance/) Eigenschaft zu Iso29500_2008_Transitional oder höher.)

```csharp
public void OptimizeFor(MsWordVersion version)
```

## Beispiele

Zeigt, wie der Textinhalt eines Textfelds vertikal ausgerichtet wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertShape(ShapeType.TextBox, 200, 200);

// Setzen Sie die Eigenschaft „VerticalAnchor“ auf „TextBoxAnchor.Top“.
// Richten Sie den Text in diesem Textfeld an der Oberseite der Form aus.
// Setzen Sie die Eigenschaft „VerticalAnchor“ auf „TextBoxAnchor.Middle“.
// Richten Sie den Text in diesem Textfeld an der Mitte der Form aus.
// Setzen Sie die Eigenschaft „VerticalAnchor“ auf „TextBoxAnchor.Bottom“.
// Richten Sie den Text in diesem Textfeld am unteren Rand der Form aus.
shape.TextBox.VerticalAnchor = verticalAnchor;

builder.MoveTo(shape.FirstParagraph);
builder.Write("Hello world!");

// Die vertikale Ausrichtung von Text innerhalb von Textfeldern ist ab Microsoft Word 2007 verfügbar.
doc.CompatibilityOptions.OptimizeFor(MsWordVersion.Word2007);
doc.Save(ArtifactsDir + "Shape.VerticalAnchor.docx");
```

Zeigt, wie eine OOXML-Konformitätsspezifikation festgelegt wird, die ein gespeichertes Dokument einhalten soll.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Wenn wir Kompatibilitätsoptionen so konfigurieren, dass sie mit Microsoft Word 2003 kompatibel sind,
// Durch das Einfügen eines Bildes wird dessen Form mithilfe von VML definiert.
doc.CompatibilityOptions.OptimizeFor(MsWordVersion.Word2003);
builder.InsertImage(ImageDir + "Transparent background logo.png");

Assert.AreEqual(ShapeMarkupLanguage.Vml, ((Shape)doc.GetChild(NodeType.Shape, 0, true)).MarkupLanguage);

// Der OOXML-Standard „ISO/IEC 29500:2008“ unterstützt keine VML-Formen.
// Wenn wir die Eigenschaft „Compliance“ des SaveOptions-Objekts auf „OoxmlCompliance.Iso29500_2008_Strict“ setzen,
 // Jedes Dokument, das wir speichern, während wir dieses Objekt übergeben, muss diesem Standard folgen.
OoxmlSaveOptions saveOptions = new OoxmlSaveOptions
{
    Compliance = OoxmlCompliance.Iso29500_2008_Strict,
    SaveFormat = SaveFormat.Docx
};

doc.Save(ArtifactsDir + "OoxmlSaveOptions.Iso29500Strict.docx", saveOptions);

// Unser gespeichertes Dokument definiert die Form mithilfe von DML, um dem OOXML-Standard „ISO/IEC 29500:2008“ zu entsprechen.
doc = new Document(ArtifactsDir + "OoxmlSaveOptions.Iso29500Strict.docx");

Assert.AreEqual(ShapeMarkupLanguage.Dml, ((Shape)doc.GetChild(NodeType.Shape, 0, true)).MarkupLanguage);
```

Zeigt, wie das Dokument für verschiedene Versionen von Microsoft Word optimiert wird.

```csharp
public void OptimizeFor()
{
    Document doc = new Document();

    // Dieses Objekt enthält eine umfangreiche Liste von Flags, die für jedes Dokument einzigartig sind
    // die es uns ermöglichen, die Abwärtskompatibilität mit älteren Versionen von Microsoft Word zu erleichtern.
    CompatibilityOptions options = doc.CompatibilityOptions;

    // Standardeinstellungen für ein leeres Dokument drucken.
    Console.WriteLine("\nDefault optimization settings:");
    PrintCompatibilityOptions(options);

    // Auf diese Einstellungen können wir in Microsoft Word über „Datei“ -> zugreifen. „Optionen“ -> „Erweitert“ –> „Kompatibilitätsoptionen für…“.
    doc.Save(ArtifactsDir + "CompatibilityOptions.OptimizeFor.DefaultSettings.docx");

    // Wir können die OptimizeFor-Methode verwenden, um eine optimale Kompatibilität mit einer bestimmten Microsoft Word-Version sicherzustellen.
    doc.CompatibilityOptions.OptimizeFor(MsWordVersion.Word2010);
    Console.WriteLine("\nOptimized for Word 2010:");
    PrintCompatibilityOptions(options);

    doc.CompatibilityOptions.OptimizeFor(MsWordVersion.Word2000);
    Console.WriteLine("\nOptimized for Word 2000:");
    PrintCompatibilityOptions(options);
}

/// <summary>
/// Gruppiert alle Flags in den Kompatibilitätsoptionen eines Dokuments nach Status und gibt dann jede Gruppe aus.
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

### Siehe auch

* enum [MsWordVersion](../../mswordversion/)
* class [CompatibilityOptions](../)
* namensraum [Aspose.Words.Settings](../../../aspose.words.settings/)
* Montage [Aspose.Words](../../../)
