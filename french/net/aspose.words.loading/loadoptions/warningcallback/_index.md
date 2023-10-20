---
title: LoadOptions.WarningCallback
linktitle: WarningCallback
articleTitle: WarningCallback
second_title: Aspose.Words pour .NET
description: LoadOptions WarningCallback propriété. Appelé lors dune opération de chargement lorsquun problème est détecté pouvant entraîner une perte de fidélité des données ou du formatage en C#.
type: docs
weight: 170
url: /fr/net/aspose.words.loading/loadoptions/warningcallback/
---
## LoadOptions.WarningCallback property

Appelé lors d'une opération de chargement, lorsqu'un problème est détecté pouvant entraîner une perte de fidélité des données ou du formatage.

```csharp
public IWarningCallback WarningCallback { get; set; }
```

## Exemples

Montre comment imprimer et stocker les avertissements qui se produisent lors du chargement du document.

```csharp
public void LoadOptionsWarningCallback()
{
    // Créez un nouvel objet LoadOptions et définissez son attribut WarningCallback
    // en tant qu'instance de notre implémentation IWarningCallback.
    LoadOptions loadOptions = new LoadOptions();
    loadOptions.WarningCallback = new DocumentLoadingWarningCallback();

    // Notre rappel imprimera tous les avertissements qui surviennent pendant l'opération de chargement.
    Document doc = new Document(MyDir + "Document.docx", loadOptions);

    List<WarningInfo> warnings = ((DocumentLoadingWarningCallback)loadOptions.WarningCallback).GetWarnings();
    Assert.AreEqual(3, warnings.Count);
}

/// <summary>
/// IWarningCallback qui imprime les avertissements et leurs détails au fur et à mesure qu'ils surviennent lors du chargement du document.
/// </summary>
private class DocumentLoadingWarningCallback : IWarningCallback
{
    public void Warning(WarningInfo info)
    {
        Console.WriteLine($"Warning: {info.WarningType}");
        Console.WriteLine($"\tSource: {info.Source}");
        Console.WriteLine($"\tDescription: {info.Description}");
        mWarnings.Add(info);
    }

    public List<WarningInfo> GetWarnings()
    {
        return mWarnings;
    }

    private readonly List<WarningInfo> mWarnings = new List<WarningInfo>();
}
```

### Voir également

* interface [IWarningCallback](../../../aspose.words/iwarningcallback/)
* class [LoadOptions](../)
* espace de noms [Aspose.Words.Loading](../../../aspose.words.loading/)
* Assemblée [Aspose.Words](../../../)
