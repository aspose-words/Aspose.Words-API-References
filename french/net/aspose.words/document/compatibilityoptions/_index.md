---
title: Document.CompatibilityOptions
linktitle: CompatibilityOptions
articleTitle: CompatibilityOptions
second_title: Aspose.Words pour .NET
description: Document CompatibilityOptions propriété. Donne accès aux options de compatibilité des documents cestàdire les préférences utilisateur saisies dans leCompatibilité Onglet duPossibilités boîte de dialogue dans Word en C#.
type: docs
weight: 50
url: /fr/net/aspose.words/document/compatibilityoptions/
---
## Document.CompatibilityOptions property

Donne accès aux options de compatibilité des documents (c'est-à-dire les préférences utilisateur saisies dans le**Compatibilité** Onglet du**Possibilités** boîte de dialogue dans Word).

```csharp
public CompatibilityOptions CompatibilityOptions { get; }
```

## Exemples

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

* class [CompatibilityOptions](../../../aspose.words.settings/compatibilityoptions/)
* class [Document](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)
