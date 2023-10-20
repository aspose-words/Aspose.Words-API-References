---
title: ImportFormatOptions.IgnoreTextBoxes
linktitle: IgnoreTextBoxes
articleTitle: IgnoreTextBoxes
second_title: Aspose.Words pour .NET
description: ImportFormatOptions IgnoreTextBoxes propriété. Obtient ou définit une valeur booléenne qui spécifie que le formatage source du contenu des zones de texte est ignoré siKeepSourceFormatting Le mode est utilisé. La valeur par défaut estvrai  en C#.
type: docs
weight: 50
url: /fr/net/aspose.words/importformatoptions/ignoretextboxes/
---
## ImportFormatOptions.IgnoreTextBoxes property

Obtient ou définit une valeur booléenne qui spécifie que le formatage source du contenu des zones de texte est ignoré siKeepSourceFormatting Le mode est utilisé. La valeur par défaut est`vrai` .

```csharp
public bool IgnoreTextBoxes { get; set; }
```

## Exemples

Montre comment gérer le formatage de la zone de texte lors de l’ajout d’un document.

```csharp
// Crée un document dans lequel seront insérés des nœuds d'un autre document.
Document dstDoc = new Document();
DocumentBuilder builder = new DocumentBuilder(dstDoc);

builder.Writeln("Hello world!");

// Créez un autre document avec une zone de texte, que nous importerons dans le premier document.
Document srcDoc = new Document();
builder = new DocumentBuilder(srcDoc);

Shape textBox = builder.InsertShape(ShapeType.TextBox, 300, 100);
builder.MoveTo(textBox.FirstParagraph);
builder.ParagraphFormat.Style.Font.Name = "Courier New";
builder.ParagraphFormat.Style.Font.Size = 24;
builder.Write("Textbox contents");

// Définit un indicateur pour spécifier s'il faut effacer ou conserver le formatage de la zone de texte
// en les important dans d'autres documents.
ImportFormatOptions importFormatOptions = new ImportFormatOptions();
importFormatOptions.IgnoreTextBoxes = ignoreTextBoxes;

// Importez la zone de texte du document source dans le document destination,
// puis vérifiez si nous avons conservé le style de son contenu textuel.
NodeImporter importer = new NodeImporter(srcDoc, dstDoc, ImportFormatMode.KeepSourceFormatting, importFormatOptions);
Shape importedTextBox = (Shape)importer.ImportNode(textBox, true);
dstDoc.FirstSection.Body.Paragraphs[1].AppendChild(importedTextBox);

if (ignoreTextBoxes)
{
    Assert.AreEqual(12.0d, importedTextBox.FirstParagraph.Runs[0].Font.Size);
    Assert.AreEqual("Times New Roman", importedTextBox.FirstParagraph.Runs[0].Font.Name);
}
else
{
    Assert.AreEqual(24.0d, importedTextBox.FirstParagraph.Runs[0].Font.Size);
    Assert.AreEqual("Courier New", importedTextBox.FirstParagraph.Runs[0].Font.Name);
}

dstDoc.Save(ArtifactsDir + "DocumentBuilder.IgnoreTextBoxes.docx");
```

### Voir également

* class [ImportFormatOptions](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)
