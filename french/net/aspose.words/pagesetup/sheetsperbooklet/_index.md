---
title: PageSetup.SheetsPerBooklet
linktitle: SheetsPerBooklet
articleTitle: SheetsPerBooklet
second_title: Aspose.Words pour .NET
description: Découvrez la propriété PageSetup SheetsPerBooklet pour gérer facilement le nombre de pages du livret, améliorant ainsi la mise en page de votre document et l'efficacité de l'impression.
type: docs
weight: 400
url: /fr/net/aspose.words/pagesetup/sheetsperbooklet/
---
## PageSetup.SheetsPerBooklet property

Renvoie ou définit le nombre de pages à inclure dans chaque livret.

```csharp
public int SheetsPerBooklet { get; set; }
```

## Exemples

Montre comment configurer un document pouvant être imprimé sous forme de livre plié.

```csharp
Document doc = new Document();

// Insérer un texte qui s'étend sur 16 pages.
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("My Booklet:");

for (int i = 0; i < 15; i++)
{
    builder.InsertBreak(BreakType.PageBreak);
    builder.Write($"Booklet face #{i}");
}

// Configurez la propriété « PageSetup » de la première section pour imprimer le document sous la forme d'un pli de livre.
// Lorsque nous imprimons ce document en recto verso, nous pouvons prendre les pages pour les empiler
// et pliez-les tous en deux. Le contenu du document sera aligné pour former un pli de livre.
PageSetup pageSetup = doc.Sections[0].PageSetup;
pageSetup.MultiplePages = MultiplePagesType.BookFoldPrinting;

// Nous ne pouvons spécifier le nombre de feuilles qu'en multiples de 4.
pageSetup.SheetsPerBooklet = 4;

doc.Save(ArtifactsDir + "PageSetup.Booklet.docx");
```

### Voir également

* class [PageSetup](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)
