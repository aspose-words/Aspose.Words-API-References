---
title: PageSetup.OtherPagesTray
linktitle: OtherPagesTray
articleTitle: OtherPagesTray
second_title: Aspose.Words pour .NET
description: Découvrez la propriété PageSetup OtherPagesTray pour personnaliser facilement les paramètres du bac à papier de votre imprimante. Optimisez l'efficacité de l'impression pour chaque section !
type: docs
weight: 300
url: /fr/net/aspose.words/pagesetup/otherpagestray/
---
## PageSetup.OtherPagesTray property

Obtient ou définit le bac à papier (bin) à utiliser pour toutes les pages d'une section sauf la première. La valeur est spécifique à l'implémentation (imprimante).

```csharp
public int OtherPagesTray { get; set; }
```

## Exemples

Montre comment faire en sorte que toutes les sections d'un document utilisent le bac à papier par défaut de l'imprimante sélectionnée.

```csharp
Document doc = new Document();

// Trouvez l'imprimante par défaut que nous utiliserons pour imprimer ce document.
// Vous pouvez définir une imprimante spécifique à l'aide de la propriété « PrinterName » de l'objet PrinterSettings.
PrinterSettings settings = new PrinterSettings();

// La valeur du bac à papier stockée dans les documents est spécifique à l'imprimante.
// Cela signifie que le code ci-dessous réinitialise toutes les valeurs du bac de page pour utiliser le bac par défaut actuel de l'imprimante.
// Vous pouvez énumérer PrinterSettings.PaperSources pour trouver les autres valeurs de bac à papier valides de l'imprimante sélectionnée.
foreach (Section section in doc.Sections.OfType<Section>())
{
    section.PageSetup.FirstPageTray = settings.DefaultPageSettings.PaperSource.RawKind;
    section.PageSetup.OtherPagesTray = settings.DefaultPageSettings.PaperSource.RawKind;
}
```

Montre comment configurer l'impression à l'aide de différents bacs d'imprimante pour différents formats de papier.

```csharp
Document doc = new Document();

// Trouvez l'imprimante par défaut que nous utiliserons pour imprimer ce document.
// Vous pouvez définir une imprimante spécifique à l'aide de la propriété « PrinterName » de l'objet PrinterSettings.
PrinterSettings settings = new PrinterSettings();

// Il s'agit du bac que nous utiliserons pour les pages au format papier « A4 ».
int printerTrayForA4 = settings.PaperSources[0].RawKind;

// Il s'agit du bac que nous utiliserons pour les pages au format de papier « Lettre ».
int printerTrayForLetter = settings.PaperSources[1].RawKind;

// Modifiez l'objet PageSettings de cette section pour que Microsoft Word donne des instructions à l'imprimante
// pour utiliser l'un des bacs que nous avons identifiés ci-dessus, en fonction du format de papier de cette section.
foreach (Section section in doc.Sections.OfType<Section>())
{
    if (section.PageSetup.PaperSize == Aspose.Words.PaperSize.Letter)
    {
        section.PageSetup.FirstPageTray = printerTrayForLetter;
        section.PageSetup.OtherPagesTray = printerTrayForLetter;
    }
    else if (section.PageSetup.PaperSize == Aspose.Words.PaperSize.A4)
    {
        section.PageSetup.FirstPageTray = printerTrayForA4;
        section.PageSetup.OtherPagesTray = printerTrayForA4;
    }
}
```

### Voir également

* class [PageSetup](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)
