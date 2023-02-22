---
title: Enum MsWordVersion
second_title: Référence de l'API Aspose.Words pour .NET
description: Aspose.Words.Settings.MsWordVersion énumération. Permet à Aspose.Wods dimiter le comportement de lapplication spécifique à la version de MS Word.
type: docs
weight: 5560
url: /fr/net/aspose.words.settings/mswordversion/
---
## MsWordVersion enumeration

Permet à Aspose.Wods d'imiter le comportement de l'application spécifique à la version de MS Word.

```csharp
public enum MsWordVersion
```

### Valeurs

| Nom | Évaluer | La description |
| --- | --- | --- |
| Word2000 | `0` | Optimiser le comportement de Aspose.Words pour correspondre à la version MS Word 2000. |
| Word2002 | `1` | Optimiser le comportement de Aspose.Words pour correspondre à la version MS Word 2002. |
| Word2003 | `2` | Optimiser le comportement de Aspose.Words pour correspondre à la version MS Word 2003. |
| Word2007 | `3` | Optimiser le comportement de Aspose.Words pour correspondre à la version MS Word 2007. |
| Word2010 | `4` | Optimiser le comportement de Aspose.Words pour correspondre à la version MS Word 2010. |
| Word2013 | `5` | Optimiser le comportement de Aspose.Words pour correspondre à la version MS Word 2013. |
| Word2016 | `6` | Optimiser le comportement de Aspose.Words pour correspondre à la version MS Word 2016. |
| Word2019 | `7` | Optimiser le comportement de Aspose.Words pour correspondre à la version MS Word 2019. |

### Exemples

Montre comment optimiser le document pour différentes versions de Microsoft Word.

```csharp
public void OptimizeFor()
{
    Document doc = new Document();

    // Cet objet contient une longue liste d'indicateurs uniques à chaque document
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
/// Regroupe tous les drapeaux dans l'objet d'options de compatibilité d'un document par état, puis imprime chaque groupe.
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

* espace de noms [Aspose.Words.Settings](../../aspose.words.settings/)
* Assemblée [Aspose.Words](../../)


