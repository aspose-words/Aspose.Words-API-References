---
title: ImportFormatOptions Class
linktitle: ImportFormatOptions
articleTitle: ImportFormatOptions
second_title: Aspose.Words pour .NET
description: Découvrez Aspose.Words.ImportFormatOptions pour une mise en forme personnalisable de vos documents. Améliorez vos résultats grâce à des paramètres d'importation personnalisés.
type: docs
weight: 3690
url: /fr/net/aspose.words/importformatoptions/
---
## ImportFormatOptions class

Permet de spécifier diverses options d'importation pour formater la sortie.

Pour en savoir plus, visitez le[Spécifier les options de chargement](https://docs.aspose.com/words/net/specify-load-options/) article de documentation.

```csharp
public class ImportFormatOptions
```

## Constructeurs

| Nom | La description |
| --- | --- |
| [ImportFormatOptions](importformatoptions/)() | Default_Constructor |

## Propriétés

| Nom | La description |
| --- | --- |
| [AdjustSentenceAndWordSpacing](../../aspose.words/importformatoptions/adjustsentenceandwordspacing/) { get; set; } | Obtient ou définit une valeur booléenne qui spécifie s'il faut ajuster automatiquement l'espacement des phrases et des mots. La valeur par défaut est`FAUX` . |
| [ForceCopyStyles](../../aspose.words/importformatoptions/forcecopystyles/) { get; set; } | Obtient ou définit une valeur booléenne indiquant de copier les styles conflictuels dansKeepSourceFormatting mode. La valeur par défaut est`FAUX` . |
| [IgnoreHeaderFooter](../../aspose.words/importformatoptions/ignoreheaderfooter/) { get; set; } | Obtient ou définit une valeur booléenne qui spécifie que le formatage source du contenu des en-têtes/pieds de page est ignoré siKeepSourceFormatting le mode est utilisé. La valeur par défaut est`vrai` . |
| [IgnoreTextBoxes](../../aspose.words/importformatoptions/ignoretextboxes/) { get; set; } | Obtient ou définit une valeur booléenne qui spécifie que la mise en forme source du contenu des zones de texte est ignorée siKeepSourceFormatting le mode est utilisé. La valeur par défaut est`vrai` . |
| [KeepSourceNumbering](../../aspose.words/importformatoptions/keepsourcenumbering/) { get; set; } | Obtient ou définit une valeur booléenne qui spécifie comment la numérotation sera importée lorsqu'elle entre en conflit dans les documents source et de destination. La valeur par défaut est`FAUX` . |
| [MergePastedLists](../../aspose.words/importformatoptions/mergepastedlists/) { get; set; } | Obtient ou définit une valeur booléenne qui spécifie si les listes collées seront fusionnées avec les listes environnantes. La valeur par défaut est`FAUX` . |
| [SmartStyleBehavior](../../aspose.words/importformatoptions/smartstylebehavior/) { get; set; } | Obtient ou définit une valeur booléenne qui spécifie comment les styles seront importés lorsqu'ils ont des noms égaux dans les documents source et de destination. La valeur par défaut est`FAUX` . |

## Exemples

Montre comment résoudre les styles en double lors de l'insertion de documents.

```csharp
Document dstDoc = new Document();
DocumentBuilder builder = new DocumentBuilder(dstDoc);

Style myStyle = builder.Document.Styles.Add(StyleType.Paragraph, "MyStyle");
myStyle.Font.Size = 14;
myStyle.Font.Name = "Courier New";
myStyle.Font.Color = Color.Blue;

builder.ParagraphFormat.StyleName = myStyle.Name;
builder.Writeln("Hello world!");

// Clonez le document et modifiez le style « MyStyle » du clone, afin qu'il soit d'une couleur différente de celle de l'original.
// Si nous insérons le clone dans le document original, les deux styles portant le même nom provoqueront un conflit.
Document srcDoc = dstDoc.Clone();
srcDoc.Styles["MyStyle"].Font.Color = Color.Red;

// Lorsque nous activons SmartStyleBehavior et utilisons le mode de format d'importation KeepSourceFormatting,
// Aspose.Words résoudra les conflits de style en convertissant les styles du document source.
// avec les mêmes noms que les styles de destination dans les attributs de paragraphe directs.
ImportFormatOptions options = new ImportFormatOptions();
options.SmartStyleBehavior = true;

builder.InsertDocument(srcDoc, ImportFormatMode.KeepSourceFormatting, options);

dstDoc.Save(ArtifactsDir + "DocumentBuilder.SmartStyleBehavior.docx");
```

### Voir également

* espace de noms [Aspose.Words](../../aspose.words/)
* Assemblée [Aspose.Words](../../)
