---
title: PageSetup.SheetsPerBooklet
second_title: Référence de l'API Aspose.Words pour .NET
description: PageSetup propriété. Renvoie ou définit le nombre de pages à inclure dans chaque livret.
type: docs
weight: 390
url: /fr/net/aspose.words/pagesetup/sheetsperbooklet/
---
## PageSetup.SheetsPerBooklet property

Renvoie ou définit le nombre de pages à inclure dans chaque livret.

```csharp
public int SheetsPerBooklet { get; set; }
```

### Exemples

Montre comment configurer un document pouvant être imprimé sous forme de pli de livre.

```csharp
Document doc = new Document();

// Insère un texte qui s'étend sur 16 pages.
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("My Booklet:");

for (int i = 0; i < 15; i++)
{
    builder.InsertBreak(BreakType.PageBreak);
    builder.Write($"Booklet face #{i}");
}

// Configurez la propriété "PageSetup" de la première section pour imprimer le document sous la forme d'un pli de livre.
// Quand on imprime ce document recto verso, on peut prendre les pages pour les empiler
// et pliez-les tous au milieu à la fois. Le contenu du document s'alignera dans un pli de livre.
PageSetup pageSetup = doc.Sections[0].PageSetup;
pageSetup.MultiplePages = MultiplePagesType.BookFoldPrinting;

// Nous ne pouvons spécifier le nombre de feuilles qu'en multiples de 4.
pageSetup.SheetsPerBooklet = 4;

doc.Save(ArtifactsDir + "PageSetup.Booklet.docx");
```

### Voir également

* class [PageSetup](../)
* espace de noms [Aspose.Words](../../pagesetup/)
* Assemblée [Aspose.Words](../../../)


