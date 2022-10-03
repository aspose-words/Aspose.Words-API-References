---
title: OptimizeFor
second_title: Aspose.Words per .NET API Reference
description: Consente di ottimizzare il contenuto del documento e il comportamento predefinito di Aspose.Words in una particolare versione di MS Word.
type: docs
weight: 720
url: /it/net/aspose.words.settings/compatibilityoptions/optimizefor/
---
## CompatibilityOptions.OptimizeFor method

Consente di ottimizzare il contenuto del documento e il comportamento predefinito di Aspose.Words in una particolare versione di MS Word.

Utilizzare questo metodo per impedire a MS Word di visualizzare la barra multifunzione "Modalità compatibilità" al caricamento del documento. (Si noti che potrebbe essere necessario anche impostare il[`Compliance`](../../../aspose.words.saving/ooxmlsaveoptions/compliance/) proprietà a Iso29500_2008_Transitional o superiore.)

```csharp
public void OptimizeFor(MsWordVersion version)
```

### Esempi

Mostra come allineare verticalmente il contenuto del testo di una casella di testo.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertShape(ShapeType.TextBox, 200, 200);

// Imposta la proprietà "VerticalAnchor" su "TextBoxAnchor.Top" su
// allinea il testo in questa casella di testo con il lato superiore della forma.
// Imposta la proprietà "VerticalAnchor" su "TextBoxAnchor.Middle" su
// allinea il testo in questa casella di testo al centro della forma.
// Imposta la proprietà "VerticalAnchor" su "TextBoxAnchor.Bottom" su
// allinea il testo in questa casella di testo alla parte inferiore della forma.
shape.TextBox.VerticalAnchor = verticalAnchor;

builder.MoveTo(shape.FirstParagraph);
builder.Write("Hello world!");

// L'allineamento verticale del testo all'interno delle caselle di testo è disponibile da Microsoft Word 2007 in poi.
doc.CompatibilityOptions.OptimizeFor(MsWordVersion.Word2007);
doc.Save(ArtifactsDir + "Shape.VerticalAnchor.docx");
```

Mostra come impostare una specifica di conformità OOXML a cui aderire un documento salvato.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Se configuriamo le opzioni di compatibilità per essere conformi a Microsoft Word 2003,
// l'inserimento di un'immagine ne definirà la forma usando VML.
doc.CompatibilityOptions.OptimizeFor(MsWordVersion.Word2003);
builder.InsertImage(ImageDir + "Transparent background logo.png");

Assert.AreEqual(ShapeMarkupLanguage.Vml, ((Shape)doc.GetChild(NodeType.Shape, 0, true)).MarkupLanguage);

// Lo standard OOXML "ISO/IEC 29500:2008" non supporta le forme VML.
// Se impostiamo la proprietà "Compliance" dell'oggetto SaveOptions su "OoxmlCompliance.Iso29500_2008_Strict",
 // qualsiasi documento che salviamo mentre passiamo questo oggetto dovrà seguire quello standard.
OoxmlSaveOptions saveOptions = new OoxmlSaveOptions
{
    Compliance = OoxmlCompliance.Iso29500_2008_Strict,
    SaveFormat = SaveFormat.Docx
};

doc.Save(ArtifactsDir + "OoxmlSaveOptions.Iso29500Strict.docx", saveOptions);

// Il nostro documento salvato definisce la forma utilizzando DML per aderire allo standard OOXML "ISO/IEC 29500:2008".
doc = new Document(ArtifactsDir + "OoxmlSaveOptions.Iso29500Strict.docx");

Assert.AreEqual(ShapeMarkupLanguage.Dml, ((Shape)doc.GetChild(NodeType.Shape, 0, true)).MarkupLanguage);
```

Mostra come ottimizzare il documento per diverse versioni di Microsoft Word.

```csharp
public void OptimizeFor()
{
    Document doc = new Document();

    // Questo oggetto contiene un ampio elenco di flag univoci per ogni documento
    // che ci consentono di facilitare la compatibilità con le versioni precedenti di Microsoft Word.
    CompatibilityOptions options = doc.CompatibilityOptions;

    // Stampa le impostazioni predefinite per un documento vuoto.
    Console.WriteLine("\nDefault optimization settings:");
    PrintCompatibilityOptions(options);

    // Possiamo accedere a queste impostazioni in Microsoft Word tramite "File" -> "Opzioni" -> "Avanzate" -> "Opzioni di compatibilità per...".
    doc.Save(ArtifactsDir + "CompatibilityOptions.OptimizeFor.DefaultSettings.docx");

    // Possiamo utilizzare il metodo OptimizeFor per garantire la compatibilità ottimale con una specifica versione di Microsoft Word.
    doc.CompatibilityOptions.OptimizeFor(MsWordVersion.Word2010);
    Console.WriteLine("\nOptimized for Word 2010:");
    PrintCompatibilityOptions(options);

    doc.CompatibilityOptions.OptimizeFor(MsWordVersion.Word2000);
    Console.WriteLine("\nOptimized for Word 2000:");
    PrintCompatibilityOptions(options);
}

/// <summary>
/// Raggruppa tutti i flag nelle opzioni di compatibilità di un documento oggetto per stato, quindi stampa ogni gruppo.
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

### Guarda anche

* enum [MsWordVersion](../../mswordversion/)
* class [CompatibilityOptions](../)
* spazio dei nomi [Aspose.Words.Settings](../../compatibilityoptions/)
* assemblea [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
