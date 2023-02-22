---
title: DocumentBuilder.InsertDocument
second_title: Référence de l'API Aspose.Words pour .NET
description: DocumentBuilder méthode. Insère un document à la position du curseur.
type: docs
weight: 290
url: /fr/net/aspose.words/documentbuilder/insertdocument/
---
## InsertDocument(Document, ImportFormatMode) {#insertdocument}

Insère un document à la position du curseur.

```csharp
public Node InsertDocument(Document srcDoc, ImportFormatMode importFormatMode)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| srcDoc | Document | Document source à insérer. |
| importFormatMode | ImportFormatMode | Spécifie comment fusionner les mises en forme de style qui entrent en conflit. |

### Return_Value

Premier nœud du contenu inséré.

### Remarques

Cette méthode imite le comportement de MS Word, comme si CTRL+'A' (sélectionner tout le contenu) était pressé, puis CTRL+'C' (copier la sélection dans le tampon) à l'intérieur d'un document puis CTRL+'V' (insérer le contenu du tampon) dans un autre document.

### Exemples

Montre comment insérer un document dans un autre document.

```csharp
Document doc = new Document(MyDir + "Document.docx");

DocumentBuilder builder = new DocumentBuilder(doc);
builder.MoveToDocumentEnd();
builder.InsertBreak(BreakType.PageBreak);

Document docToInsert = new Document(MyDir + "Formatted elements.docx");

builder.InsertDocument(docToInsert, ImportFormatMode.KeepSourceFormatting);
builder.Document.Save(ArtifactsDir + "DocumentBuilder.InsertDocument.docx");
```

### Voir également

* class [Node](../../node/)
* class [Document](../../document/)
* enum [ImportFormatMode](../../importformatmode/)
* class [DocumentBuilder](../)
* espace de noms [Aspose.Words](../../documentbuilder/)
* Assemblée [Aspose.Words](../../../)

---

## InsertDocument(Document, ImportFormatMode, ImportFormatOptions) {#insertdocument_1}

Insère un document à la position du curseur.

```csharp
public Node InsertDocument(Document srcDoc, ImportFormatMode importFormatMode, 
    ImportFormatOptions importFormatOptions)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| srcDoc | Document | Document source à insérer. |
| importFormatMode | ImportFormatMode | Spécifie comment fusionner les mises en forme de style qui entrent en conflit. |
| importFormatOptions | ImportFormatOptions | Permet de spécifier les options qui affectent le formatage d'un document de résultat. |

### Return_Value

Premier nœud du contenu inséré.

### Remarques

Cette méthode imite le comportement de MS Word, comme si CTRL+'A' (sélectionner tout le contenu) était pressé, puis CTRL+'C' (copier la sélection dans le tampon) à l'intérieur d'un document puis CTRL+'V' (insérer le contenu du tampon) dans un autre document.

### Exemples

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

// Clone le document et édite le style "MyStyle" du clone, de sorte qu'il soit d'une couleur différente de celle de l'original.
// Si nous insérons le clone dans le document d'origine, les deux styles portant le même nom provoqueront un conflit.
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

* class [Node](../../node/)
* class [Document](../../document/)
* enum [ImportFormatMode](../../importformatmode/)
* class [ImportFormatOptions](../../importformatoptions/)
* class [DocumentBuilder](../)
* espace de noms [Aspose.Words](../../documentbuilder/)
* Assemblée [Aspose.Words](../../../)


