---
title: CompatibilityOptions.OptimizeFor
second_title: Référence de l'API Aspose.Words pour .NET
description: CompatibilityOptions méthode. Permet doptimiser le contenu du document ainsi que le comportement par défaut dAspose.Words pour une version particulière de MS Word.
type: docs
weight: 720
url: /fr/net/aspose.words.settings/compatibilityoptions/optimizefor/
---
## CompatibilityOptions.OptimizeFor method

Permet d'optimiser le contenu du document ainsi que le comportement par défaut d'Aspose.Words pour une version particulière de MS Word.

Utilisez cette méthode pour empêcher MS Word d'afficher le ruban "Mode de compatibilité" lors du chargement du document. (Notez que vous devrez peut-être également définir le[`Compliance`](../../../aspose.words.saving/ooxmlsaveoptions/compliance/) propriété à Iso29500_2008_Transitional ou supérieur.)

```csharp
public void OptimizeFor(MsWordVersion version)
```

### Exemples

Montre comment aligner verticalement le contenu du texte d’une zone de texte.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertShape(ShapeType.TextBox, 200, 200);

// Définissez la propriété "VerticalAnchor" sur "TextBoxAnchor.Top" pour
// aligne le texte de cette zone de texte avec le côté supérieur de la forme.
// Définissez la propriété "VerticalAnchor" sur "TextBoxAnchor.Middle" pour
// aligne le texte de cette zone de texte au centre de la forme.
// Définissez la propriété "VerticalAnchor" sur "TextBoxAnchor.Bottom" pour
// aligne le texte de cette zone de texte au bas de la forme.
shape.TextBox.VerticalAnchor = verticalAnchor;

builder.MoveTo(shape.FirstParagraph);
builder.Write("Hello world!");

// L'alignement vertical du texte à l'intérieur des zones de texte est disponible à partir de Microsoft Word 2007.
doc.CompatibilityOptions.OptimizeFor(MsWordVersion.Word2007);
doc.Save(ArtifactsDir + "Shape.VerticalAnchor.docx");
```

Montre comment définir une spécification de conformité OOXML à laquelle un document enregistré doit adhérer.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Si nous configurons les options de compatibilité pour se conformer à Microsoft Word 2003,
// l'insertion d'une image définira sa forme en utilisant VML.
doc.CompatibilityOptions.OptimizeFor(MsWordVersion.Word2003);
builder.InsertImage(ImageDir + "Transparent background logo.png");

Assert.AreEqual(ShapeMarkupLanguage.Vml, ((Shape)doc.GetChild(NodeType.Shape, 0, true)).MarkupLanguage);

// La norme OOXML "ISO/IEC 29500:2008" ne prend pas en charge les formes VML.
// Si on fixe la propriété "Compliance" de l'objet SaveOptions à "OoxmlCompliance.Iso29500_2008_Strict",
 // tout document que nous enregistrons en transmettant cet objet devra suivre cette norme.
OoxmlSaveOptions saveOptions = new OoxmlSaveOptions
{
    Compliance = OoxmlCompliance.Iso29500_2008_Strict,
    SaveFormat = SaveFormat.Docx
};

doc.Save(ArtifactsDir + "OoxmlSaveOptions.Iso29500Strict.docx", saveOptions);

// Notre document enregistré définit la forme à l'aide de DML pour adhérer à la norme OOXML "ISO/IEC 29500:2008".
doc = new Document(ArtifactsDir + "OoxmlSaveOptions.Iso29500Strict.docx");

Assert.AreEqual(ShapeMarkupLanguage.Dml, ((Shape)doc.GetChild(NodeType.Shape, 0, true)).MarkupLanguage);
```

Montre comment optimiser le document pour différentes versions de Microsoft Word.

```csharp
public void OptimizeFor()
{
    Document doc = new Document();

    // Cet objet contient une liste complète d'indicateurs uniques à chaque document
    // qui nous permettent de faciliter la rétrocompatibilité avec les anciennes versions de Microsoft Word.
    CompatibilityOptions options = doc.CompatibilityOptions;

    // Imprime les paramètres par défaut pour un document vierge.
    Console.WriteLine("\nDefault optimization settings:");
    PrintCompatibilityOptions(options);

    // Nous pouvons accéder à ces paramètres dans Microsoft Word via "Fichier" -> "Options" -> "Avancé" -> "Options de compatibilité pour...".
    doc.Save(ArtifactsDir + "CompatibilityOptions.OptimizeFor.DefaultSettings.docx");

    // Nous pouvons utiliser la méthode OptimizeFor pour assurer une compatibilité optimale avec une version spécifique de Microsoft Word.
    doc.CompatibilityOptions.OptimizeFor(MsWordVersion.Word2010);
    Console.WriteLine("\nOptimized for Word 2010:");
    PrintCompatibilityOptions(options);

    doc.CompatibilityOptions.OptimizeFor(MsWordVersion.Word2000);
    Console.WriteLine("\nOptimized for Word 2000:");
    PrintCompatibilityOptions(options);
}

/// <summary>
/// Regroupe tous les indicateurs dans l'objet d'options de compatibilité d'un document par état, puis imprime chaque groupe.
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

### Voir également

* enum [MsWordVersion](../../mswordversion/)
* class [CompatibilityOptions](../)
* espace de noms [Aspose.Words.Settings](../../compatibilityoptions/)
* Assemblée [Aspose.Words](../../../)


