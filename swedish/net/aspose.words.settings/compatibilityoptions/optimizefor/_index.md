---
title: CompatibilityOptions.OptimizeFor
second_title: Aspose.Words för .NET API Referens
description: CompatibilityOptions metod. Tillåter att optimera dokumentinnehållet såväl som standard Aspose.Wordsbeteende för en viss version av MS Word.
type: docs
weight: 720
url: /sv/net/aspose.words.settings/compatibilityoptions/optimizefor/
---
## CompatibilityOptions.OptimizeFor method

Tillåter att optimera dokumentinnehållet såväl som standard Aspose.Words-beteende för en viss version av MS Word.

Använd den här metoden för att förhindra att MS Word visar bandet "Kompatibilitetsläge" när dokument laddas. (Observera att du också kan behöva ställa in[`Compliance`](../../../aspose.words.saving/ooxmlsaveoptions/compliance/) egenskap till Iso29500_2008_Transitional eller högre.)

```csharp
public void OptimizeFor(MsWordVersion version)
```

### Exempel

Visar hur man vertikalt justerar textinnehållet i en textruta.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertShape(ShapeType.TextBox, 200, 200);

// Ställ in egenskapen "VerticalAnchor" till "TextBoxAnchor.Top" till
// justera texten i denna textruta med formens övre sida.
// Ställ in egenskapen "VerticalAnchor" till "TextBoxAnchor.Middle" till
// justera texten i denna textruta till mitten av formen.
// Ställ in egenskapen "VerticalAnchor" till "TextBoxAnchor.Bottom" till
// justera texten i den här textrutan till botten av formen.
shape.TextBox.VerticalAnchor = verticalAnchor;

builder.MoveTo(shape.FirstParagraph);
builder.Write("Hello world!");

// Den vertikala justeringen av text inuti textrutor är tillgänglig från Microsoft Word 2007 och framåt.
doc.CompatibilityOptions.OptimizeFor(MsWordVersion.Word2007);
doc.Save(ArtifactsDir + "Shape.VerticalAnchor.docx");
```

Visar hur man ställer in en OOXML-efterlevnadsspecifikation för ett sparat dokument att följa.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Om vi konfigurerar kompatibilitetsalternativ för att följa Microsoft Word 2003,
// att infoga en bild kommer att definiera dess form med VML.
doc.CompatibilityOptions.OptimizeFor(MsWordVersion.Word2003);
builder.InsertImage(ImageDir + "Transparent background logo.png");

Assert.AreEqual(ShapeMarkupLanguage.Vml, ((Shape)doc.GetChild(NodeType.Shape, 0, true)).MarkupLanguage);

// OOXML-standarden "ISO/IEC 29500:2008" stöder inte VML-former.
// Om vi ställer in egenskapen "Compliance" för SaveOptions-objektet till "OoxmlCompliance.Iso29500_2008_Strict",
 // alla dokument vi sparar när vi skickar detta objekt måste följa den standarden.
OoxmlSaveOptions saveOptions = new OoxmlSaveOptions
{
    Compliance = OoxmlCompliance.Iso29500_2008_Strict,
    SaveFormat = SaveFormat.Docx
};

doc.Save(ArtifactsDir + "OoxmlSaveOptions.Iso29500Strict.docx", saveOptions);

// Vårt sparade dokument definierar formen med DML för att följa OOXML-standarden "ISO/IEC 29500:2008".
doc = new Document(ArtifactsDir + "OoxmlSaveOptions.Iso29500Strict.docx");

Assert.AreEqual(ShapeMarkupLanguage.Dml, ((Shape)doc.GetChild(NodeType.Shape, 0, true)).MarkupLanguage);
```

Visar hur man optimerar dokumentet för olika versioner av Microsoft Word.

```csharp
public void OptimizeFor()
{
    Document doc = new Document();

    // Detta objekt innehåller en omfattande lista med flaggor som är unika för varje dokument
    // som tillåter oss att underlätta bakåtkompatibilitet med äldre versioner av Microsoft Word.
    CompatibilityOptions options = doc.CompatibilityOptions;

    // Skriv ut standardinställningarna för ett tomt dokument.
    Console.WriteLine("\nDefault optimization settings:");
    PrintCompatibilityOptions(options);

    // Vi kan komma åt dessa inställningar i Microsoft Word via "File" -> "Alternativ" -> "Avancerat" -> "Kompatibilitetsalternativ för...".
    doc.Save(ArtifactsDir + "CompatibilityOptions.OptimizeFor.DefaultSettings.docx");

    // Vi kan använda OptimizeFor-metoden för att säkerställa optimal kompatibilitet med en specifik Microsoft Word-version.
    doc.CompatibilityOptions.OptimizeFor(MsWordVersion.Word2010);
    Console.WriteLine("\nOptimized for Word 2010:");
    PrintCompatibilityOptions(options);

    doc.CompatibilityOptions.OptimizeFor(MsWordVersion.Word2000);
    Console.WriteLine("\nOptimized for Word 2000:");
    PrintCompatibilityOptions(options);
}

/// <summary>
/// Grupperar alla flaggor i ett dokuments kompatibilitetsalternativobjekt efter tillstånd och skrivs sedan ut varje grupp.
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

### Se även

* enum [MsWordVersion](../../mswordversion/)
* class [CompatibilityOptions](../)
* namnutrymme [Aspose.Words.Settings](../../compatibilityoptions/)
* hopsättning [Aspose.Words](../../../)


