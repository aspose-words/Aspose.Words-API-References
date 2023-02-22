---
title: ImportFormatOptions.KeepSourceNumbering
second_title: Référence de l'API Aspose.Words pour .NET
description: ImportFormatOptions propriété. Obtient ou définit une valeur booléenne qui spécifie comment la numérotation sera importée en cas de conflit dans les documents source et destination. La valeur par défaut estfaux .
type: docs
weight: 50
url: /fr/net/aspose.words/importformatoptions/keepsourcenumbering/
---
## ImportFormatOptions.KeepSourceNumbering property

Obtient ou définit une valeur booléenne qui spécifie comment la numérotation sera importée en cas de conflit dans les documents source et destination. La valeur par défaut est`faux` .

```csharp
public bool KeepSourceNumbering { get; set; }
```

### Exemples

Montre comment résoudre un conflit lors de l'importation de documents contenant des listes avec le même identifiant de définition de liste.

```csharp
Document srcDoc = new Document(MyDir + "List with the same definition identifier - source.docx");
Document dstDoc = new Document(MyDir + "List with the same definition identifier - destination.docx");

// Définissez la propriété "KeepSourceNumbering" sur "true" pour appliquer un ID de définition de liste différent
// aux styles identiques car Aspose.Words les importe dans les documents de destination.
ImportFormatOptions importFormatOptions = new ImportFormatOptions { KeepSourceNumbering = true };

dstDoc.AppendDocument(srcDoc, ImportFormatMode.UseDestinationStyles, importFormatOptions);
dstDoc.UpdateListLabels();
```

Montre comment importer un document avec des listes numérotées.

```csharp
Document srcDoc = new Document(MyDir + "List source.docx");
Document dstDoc = new Document(MyDir + "List destination.docx");

Assert.AreEqual(4, dstDoc.Lists.Count);

ImportFormatOptions options = new ImportFormatOptions();

// S'il y a un conflit de styles de liste, applique le format de liste du document source.
// Définissez la propriété "KeepSourceNumbering" sur "false" pour ne pas importer de numéros de liste dans le document de destination.
// Définit la propriété "KeepSourceNumbering" sur "true" importe tous les conflits
// liste la numérotation des styles avec la même apparence que celle qu'elle avait dans le document source.
options.KeepSourceNumbering = isKeepSourceNumbering;

dstDoc.AppendDocument(srcDoc, ImportFormatMode.KeepSourceFormatting, options);
dstDoc.UpdateListLabels();

Assert.AreEqual(isKeepSourceNumbering ? 5 : 4, dstDoc.Lists.Count);
```

Montre comment résoudre les conflits de numérotation de liste dans les documents source et de destination.

```csharp
// Ouvre un document avec un schéma de numérotation de liste personnalisé, puis le clone.
// Puisque les deux ont le même format de numérotation, les formats entreront en conflit si nous importons un document dans l'autre.
Document srcDoc = new Document(MyDir + "Custom list numbering.docx");
Document dstDoc = srcDoc.Clone();

// Lorsque nous importons le clone du document dans l'original, puis l'ajoutons,
// alors les deux listes avec le même format de liste se rejoindront.
// Si nous définissons le drapeau "KeepSourceNumbering" sur "false", alors la liste du document clone
// que nous ajoutons à l'original portera la numérotation de la liste à laquelle nous l'ajoutons.
// Cela fusionnera efficacement les deux listes en une seule.
// Si nous définissons le drapeau "KeepSourceNumbering" sur "true", alors le document clone
// list conservera sa numérotation d'origine, faisant apparaître les deux listes comme des listes séparées. 
ImportFormatOptions importFormatOptions = new ImportFormatOptions();
importFormatOptions.KeepSourceNumbering = keepSourceNumbering;

NodeImporter importer = new NodeImporter(srcDoc, dstDoc, ImportFormatMode.KeepDifferentStyles, importFormatOptions);
foreach (Paragraph paragraph in srcDoc.FirstSection.Body.Paragraphs)
{
    Node importedNode = importer.ImportNode(paragraph, true);
    dstDoc.FirstSection.Body.AppendChild(importedNode);
}

dstDoc.UpdateListLabels();

if (keepSourceNumbering)
{
    Assert.AreEqual(
        "6. Item 1\r\n" +
        "7. Item 2 \r\n" +
        "8. Item 3\r\n" +
        "9. Item 4\r\n" +
        "6. Item 1\r\n" +
        "7. Item 2 \r\n" +
        "8. Item 3\r\n" +
        "9. Item 4", dstDoc.FirstSection.Body.ToString(SaveFormat.Text).Trim());
}
else
{
    Assert.AreEqual(
        "6. Item 1\r\n" +
        "7. Item 2 \r\n" +
        "8. Item 3\r\n" +
        "9. Item 4\r\n" +
        "10. Item 1\r\n" +
        "11. Item 2 \r\n" +
        "12. Item 3\r\n" +
        "13. Item 4", dstDoc.FirstSection.Body.ToString(SaveFormat.Text).Trim());
}
```

### Voir également

* class [ImportFormatOptions](../)
* espace de noms [Aspose.Words](../../importformatoptions/)
* Assemblée [Aspose.Words](../../../)


