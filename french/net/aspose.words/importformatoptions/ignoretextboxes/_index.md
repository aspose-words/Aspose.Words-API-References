---
title: ImportFormatOptions.IgnoreTextBoxes
linktitle: IgnoreTextBoxes
articleTitle: IgnoreTextBoxes
second_title: Aspose.Words pour .NET
description: Découvrez comment la propriété IgnoreTextBoxes d'ImportFormatOptions améliore la mise en forme de vos documents en contrôlant le contenu des zones de texte. Optimisez facilement dès aujourd'hui !
type: docs
weight: 50
url: /fr/net/aspose.words/importformatoptions/ignoretextboxes/
---
## ImportFormatOptions.IgnoreTextBoxes property

Obtient ou définit une valeur booléenne qui spécifie que la mise en forme source du contenu des zones de texte est ignorée siKeepSourceFormatting le mode est utilisé. La valeur par défaut est`vrai` .

```csharp
public bool IgnoreTextBoxes { get; set; }
```

## Exemples

Montre comment gérer la mise en forme de la zone de texte lors de l'ajout d'un document.

```csharp
// Créez un document dans lequel seront insérés des nœuds provenant d'un autre document.
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

// Définir un indicateur pour spécifier s'il faut effacer ou conserver la mise en forme de la zone de texte
// lors de leur importation dans d'autres documents.
ImportFormatOptions importFormatOptions = new ImportFormatOptions();
importFormatOptions.IgnoreTextBoxes = ignoreTextBoxes;

// Importer la zone de texte du document source dans le document de destination,
// et ensuite vérifier si nous avons conservé le style de son contenu textuel.
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
