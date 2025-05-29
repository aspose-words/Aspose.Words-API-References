---
title: ImportFormatOptions.SmartStyleBehavior
linktitle: SmartStyleBehavior
articleTitle: SmartStyleBehavior
second_title: Aspose.Words pour .NET
description: Découvrez comment la propriété SmartStyleBehavior d'ImportFormatOptions optimise l'importation de styles avec des noms identiques dans les documents. Personnalisez votre processus d'importation en toute simplicité !
type: docs
weight: 80
url: /fr/net/aspose.words/importformatoptions/smartstylebehavior/
---
## ImportFormatOptions.SmartStyleBehavior property

Obtient ou définit une valeur booléenne qui spécifie comment les styles seront importés lorsqu'ils ont des noms égaux dans les documents source et de destination. La valeur par défaut est`FAUX` .

```csharp
public bool SmartStyleBehavior { get; set; }
```

## Remarques

Lorsque cette option est**activé** , le style source sera étendu en attributs directs à l'intérieur d'un document de destination a , siKeepSourceFormatting le mode d'importation est utilisé.

Lorsque cette option est**désactivé**Le style source ne sera développé que s'il est numéroté. Les attributs de destination existants (existing ) ne seront pas remplacés, y compris les listes.

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

* class [ImportFormatOptions](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)
