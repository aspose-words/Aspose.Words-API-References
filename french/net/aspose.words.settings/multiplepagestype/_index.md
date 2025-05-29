---
title: MultiplePagesType Enum
linktitle: MultiplePagesType
articleTitle: MultiplePagesType
second_title: Aspose.Words pour .NET
description: Découvrez l'énumération Aspose.Words.Settings.MultiplePagesType pour des options d'impression de documents efficaces. Optimisez votre flux de travail grâce à des paramètres d'impression flexibles !
type: docs
weight: 6700
url: /fr/net/aspose.words.settings/multiplepagestype/
---
## MultiplePagesType enumeration

Spécifie comment le document est imprimé.

```csharp
public enum MultiplePagesType
```

### Valeurs

| Nom | Évaluer | La description |
| --- | --- | --- |
| Normal | `0` | Impression normale, aucune page multiple spécifiée. |
| MirrorMargins | `1` | Échange les marges gauche et droite sur les pages en vis-à-vis. |
| TwoPagesPerSheet | `2` | Imprime deux pages par feuille. |
| BookFoldPrinting | `3` | Spécifie s'il faut imprimer le document sous forme de livre plié. |
| BookFoldPrintingReverse | `4` | Spécifie s'il faut imprimer le document sous forme de pli de livre inversé. |
| Default | `0` | La valeur par défaut estNormal |

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

* espace de noms [Aspose.Words.Settings](../../aspose.words.settings/)
* Assemblée [Aspose.Words](../../)
