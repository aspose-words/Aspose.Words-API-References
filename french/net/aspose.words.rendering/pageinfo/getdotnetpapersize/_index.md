---
title: PageInfo.GetDotNetPaperSize
linktitle: GetDotNetPaperSize
articleTitle: GetDotNetPaperSize
second_title: Aspose.Words pour .NET
description: Découvrez la méthode GetDotNetPaperSize dans PageInfo, conçue pour récupérer sans effort l'objet PaperSize idéal pour une impression de page transparente.
type: docs
weight: 80
url: /fr/net/aspose.words.rendering/pageinfo/getdotnetpapersize/
---
## PageInfo.GetDotNetPaperSize method

Obtient lePaperSize objet adapté à l'impression la page représentée par ceci[`PageInfo`](../) .

```csharp
public PaperSize GetDotNetPaperSize(PaperSizeCollection paperSizes)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| paperSizes | PaperSizeCollection | Formats de papier disponibles. |

### Return_Value

Un objet que vous pouvez utiliser dans le framework d’impression .NET pour spécifier le format du papier.

## Exemples

Montre comment personnaliser l'impression des documents Aspose.Words.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

    MyPrintDocument printDoc = new MyPrintDocument(doc);
    printDoc.PrinterSettings.PrintRange = System.Drawing.Printing.PrintRange.SomePages;
    printDoc.PrinterSettings.FromPage = 1;
    printDoc.PrinterSettings.ToPage = 1;

    printDoc.Print();
}

/// <summary>
/// Sélectionne un format de papier, une orientation et un bac à papier appropriés lors de l'impression.
/// </summary>
public class MyPrintDocument : PrintDocument
{
    public MyPrintDocument(Document document)
    {
        mDocument = document;
    }

    /// <summary>
    /// Initialise la plage de pages à imprimer en fonction de la sélection de l'utilisateur.
    /// </summary>
    protected override void OnBeginPrint(PrintEventArgs e)
    {
        base.OnBeginPrint(e);

        switch (PrinterSettings.PrintRange)
        {
            case System.Drawing.Printing.PrintRange.AllPages:
                mCurrentPage = 1;
                mPageTo = mDocument.PageCount;
                break;
            case System.Drawing.Printing.PrintRange.SomePages:
                mCurrentPage = PrinterSettings.FromPage;
                mPageTo = PrinterSettings.ToPage;
                break;
            default:
                throw new InvalidOperationException("Unsupported print range.");
        }
    }

    /// <summary>
     /// Appelé avant l'impression de chaque page.
    /// </summary>
    protected override void OnQueryPageSettings(QueryPageSettingsEventArgs e)
    {
        base.OnQueryPageSettings(e);

         // Un seul document Microsoft Word peut avoir plusieurs sections qui spécifient des pages de tailles différentes,
         // orientations et bacs à papier. Le framework d'impression .NET appelle ce code avant
        // chaque page est imprimée, ce qui nous donne la possibilité de spécifier comment imprimer la page actuelle.
        PageInfo pageInfo = mDocument.GetPageInfo(mCurrentPage - 1);
        e.PageSettings.PaperSize = pageInfo.GetDotNetPaperSize(PrinterSettings.PaperSizes);

        // Microsoft Word stocke la source de papier (bac d'imprimante) pour chaque section sous la forme d'une valeur spécifique à l'imprimante.
        // Pour obtenir la valeur de bac correcte, vous devrez utiliser la propriété « RawKind », que votre imprimante doit renvoyer.
        e.PageSettings.PaperSource.RawKind = pageInfo.PaperTray;
        e.PageSettings.Landscape = pageInfo.Landscape;
    }

    /// <summary>
     /// Appelé pour chaque page pour la restituer pour l'impression.
    /// </summary>
    protected override void OnPrintPage(PrintPageEventArgs e)
    {
        base.OnPrintPage(e);

        // Le moteur de rendu Aspose.Words crée une page dessinée à partir de l'origine (x = 0, y = 0) du papier.
        // L'imprimante disposera d'une marge fixe pour le rendu de chaque page. Nous devons la décaler de cette marge fixe.
        float hardOffsetX, hardOffsetY;

        // Vous trouverez ci-dessous deux manières de définir une marge fixe.
        if (e.PageSettings != null && e.PageSettings.HardMarginX != 0 && e.PageSettings.HardMarginY != 0)
        {
            // 1 - Via la propriété "PageSettings".
            hardOffsetX = e.PageSettings.HardMarginX;
            hardOffsetY = e.PageSettings.HardMarginY;
        }
        else
        {
            // 2 - Utilisation de nos propres valeurs, si la propriété « PageSettings » n'est pas disponible.
            hardOffsetX = 20;
            hardOffsetY = 20;
        }

        mDocument.RenderToScale(mCurrentPage, e.Graphics, -hardOffsetX, -hardOffsetY, 1.0f);

        mCurrentPage++;
        e.HasMorePages = mCurrentPage <= mPageTo;
    }

    private readonly Document mDocument;
    private int mCurrentPage;
    private int mPageTo;
}
```

### Voir également

* class [PageInfo](../)
* espace de noms [Aspose.Words.Rendering](../../../aspose.words.rendering/)
* Assemblée [Aspose.Words](../../../)
