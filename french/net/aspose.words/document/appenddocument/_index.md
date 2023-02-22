---
title: Document.AppendDocument
second_title: Référence de l'API Aspose.Words pour .NET
description: Document méthode. Ajoute le document spécifié à la fin de ce document.
type: docs
weight: 510
url: /fr/net/aspose.words/document/appenddocument/
---
## AppendDocument(Document, ImportFormatMode) {#appenddocument}

Ajoute le document spécifié à la fin de ce document.

```csharp
public void AppendDocument(Document srcDoc, ImportFormatMode importFormatMode)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| srcDoc | Document | Le document à joindre. |
| importFormatMode | ImportFormatMode | Spécifie comment fusionner les mises en forme de style qui entrent en conflit. |

### Exemples

Montre comment ajouter un document à la fin d'un autre document.

```csharp
Document srcDoc = new Document();
srcDoc.FirstSection.Body.AppendParagraph("Source document text. ");

Document dstDoc = new Document();
dstDoc.FirstSection.Body.AppendParagraph("Destination document text. ");

// Ajoute le document source au document destination en préservant sa mise en forme,
// puis enregistrez le document source dans le système de fichiers local.
dstDoc.AppendDocument(srcDoc, ImportFormatMode.KeepSourceFormatting);
dstDoc.Save(ArtifactsDir + "Document.AppendDocument.docx");
```

Montre comment ajouter tous les documents d'un dossier à la fin d'un modèle de document.

```csharp
Document dstDoc = new Document();

DocumentBuilder builder = new DocumentBuilder(dstDoc);
builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading1;
builder.Writeln("Template Document");
builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Normal;
builder.Writeln("Some content here");

// Ajoute tous les documents non chiffrés avec l'extension .doc
// de notre répertoire de système de fichiers local au document de base.
List<string> docFiles = Directory.GetFiles(MyDir, "*.doc").Where(item => item.EndsWith(".doc")).ToList();
foreach (string fileName in docFiles)
{
    FileFormatInfo info = FileFormatUtil.DetectFileFormat(fileName);
    if (info.IsEncrypted)
        continue;

    Document srcDoc = new Document(fileName);
    dstDoc.AppendDocument(srcDoc, ImportFormatMode.UseDestinationStyles);
}

dstDoc.Save(ArtifactsDir + "Document.AppendAllDocumentsInFolder.doc");
```

### Voir également

* enum [ImportFormatMode](../../importformatmode/)
* class [Document](../)
* espace de noms [Aspose.Words](../../document/)
* Assemblée [Aspose.Words](../../../)

---

## AppendDocument(Document, ImportFormatMode, ImportFormatOptions) {#appenddocument_1}

Ajoute le document spécifié à la fin de ce document.

```csharp
public void AppendDocument(Document srcDoc, ImportFormatMode importFormatMode, 
    ImportFormatOptions importFormatOptions)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| srcDoc | Document | Le document à joindre. |
| importFormatMode | ImportFormatMode | Spécifie comment fusionner les mises en forme de style qui entrent en conflit. |
| importFormatOptions | ImportFormatOptions | Permet de spécifier les options qui affectent le formatage d'un document de résultat. |

### Exemples

Montre comment gérer les conflits de style de liste lors de l'ajout d'un clone d'un document à lui-même.

```csharp
Document srcDoc = new Document(MyDir + "List item.docx");
Document dstDoc = new Document(MyDir + "List item.docx");

// S'il y a un conflit de styles de liste, applique le format de liste du document source.
// Définissez la propriété "KeepSourceNumbering" sur "false" pour ne pas importer de numéros de liste dans le document de destination.
// Définit la propriété "KeepSourceNumbering" sur "true" importe tous les conflits
// liste la numérotation des styles avec la même apparence que celle qu'elle avait dans le document source.
DocumentBuilder builder = new DocumentBuilder(dstDoc);
builder.MoveToDocumentEnd();
builder.InsertBreak(BreakType.SectionBreakNewPage);

ImportFormatOptions options = new ImportFormatOptions();
options.KeepSourceNumbering = keepSourceNumbering;
builder.InsertDocument(srcDoc, ImportFormatMode.KeepSourceFormatting, options);

dstDoc.UpdateListLabels();
```

Montre comment gérer les conflits de style de liste lors de l'insertion d'un document.

```csharp
Document dstDoc = new Document();
DocumentBuilder builder = new DocumentBuilder(dstDoc);
builder.InsertBreak(BreakType.ParagraphBreak);

dstDoc.Lists.Add(ListTemplate.NumberDefault);
Aspose.Words.Lists.List list = dstDoc.Lists[0];

builder.ListFormat.List = list;

for (int i = 1; i <= 15; i++)
    builder.Write($"List Item {i}\n");

Document attachDoc = (Document)dstDoc.Clone(true);

// S'il y a un conflit de styles de liste, applique le format de liste du document source.
// Définissez la propriété "KeepSourceNumbering" sur "false" pour ne pas importer de numéros de liste dans le document de destination.
// Définit la propriété "KeepSourceNumbering" sur "true" importe tous les conflits
// liste la numérotation des styles avec la même apparence que celle qu'elle avait dans le document source.
ImportFormatOptions importOptions = new ImportFormatOptions();
importOptions.KeepSourceNumbering = keepSourceNumbering;

builder.InsertBreak(BreakType.SectionBreakNewPage);
builder.InsertDocument(attachDoc, ImportFormatMode.KeepSourceFormatting, importOptions);

dstDoc.Save(ArtifactsDir + "DocumentBuilder.InsertDocumentAndResolveStyles.docx");
```

Montre comment gérer les conflits de style de liste lors de l'ajout d'un document.

```csharp
// Charge un document avec du texte dans un style personnalisé et le clone.
Document srcDoc = new Document(MyDir + "Custom list numbering.docx");
Document dstDoc = srcDoc.Clone();

// Nous avons maintenant deux documents, chacun avec un style identique nommé "CustomStyle".
// Modifiez la couleur du texte de l'un des styles pour le distinguer de l'autre.
dstDoc.Styles["CustomStyle"].Font.Color = Color.DarkRed;

// S'il y a un conflit de styles de liste, applique le format de liste du document source.
// Définissez la propriété "KeepSourceNumbering" sur "false" pour ne pas importer de numéros de liste dans le document de destination.
// Définit la propriété "KeepSourceNumbering" sur "true" importe tous les conflits
// liste la numérotation des styles avec la même apparence que celle qu'elle avait dans le document source.
ImportFormatOptions options = new ImportFormatOptions();
options.KeepSourceNumbering = keepSourceNumbering;

// Joindre deux documents qui ont des styles différents et qui partagent le même nom provoque un conflit de style.
// Nous pouvons spécifier un mode de format d'importation lors de l'ajout de documents pour résoudre ce conflit.
dstDoc.AppendDocument(srcDoc, ImportFormatMode.KeepDifferentStyles, options);
dstDoc.UpdateListLabels();

dstDoc.Save(ArtifactsDir + "DocumentBuilder.AppendDocumentAndResolveStyles.docx");
```

### Voir également

* enum [ImportFormatMode](../../importformatmode/)
* class [ImportFormatOptions](../../importformatoptions/)
* class [Document](../)
* espace de noms [Aspose.Words](../../document/)
* Assemblée [Aspose.Words](../../../)


