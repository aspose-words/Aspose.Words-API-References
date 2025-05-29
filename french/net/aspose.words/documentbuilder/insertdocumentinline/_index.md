---
title: DocumentBuilder.InsertDocumentInline
linktitle: InsertDocumentInline
articleTitle: InsertDocumentInline
second_title: Aspose.Words pour .NET
description: Insérez sans effort des documents en ligne avec la méthode InsertDocumentInline de DocumentBuilder, améliorant ainsi votre flux de travail et votre expérience d'édition de documents.
type: docs
weight: 320
url: /fr/net/aspose.words/documentbuilder/insertdocumentinline/
---
## DocumentBuilder.InsertDocumentInline method

Insère un document en ligne à la position du curseur.

```csharp
public Node InsertDocumentInline(Document srcDoc, ImportFormatMode importFormatMode, 
    ImportFormatOptions importFormatOptions)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| srcDoc | Document | Document source à insérer. |
| importFormatMode | ImportFormatMode | Spécifie comment fusionner les formats de style qui entrent en conflit. |
| importFormatOptions | ImportFormatOptions | Permet de spécifier les options qui affectent la mise en forme d'un document de résultat. |

### Return_Value

Premier nœud du contenu inséré.

## Remarques

Cette méthode imite le comportement de MS Word, comme si CTRL+'A' (sélectionner tout le contenu) était enfoncé, puis CTRL+'C' (copier la sélection dans le tampon) à l'intérieur d'un document puis CTRL+'V' (insérer le contenu du tampon) à l'intérieur d'un autre document.

En guise de différence avec[`InsertDocument`](../insertdocument/) Cette méthode déplace le contenu du paragraphe du document de destination, avant lequel le document source est inséré, vers le dernier paragraphe du document source inséré. En fait, cela signifie que le saut de paragraphe du dernier paragraphe inséré est supprimé.

Attention, si le dernier nœud du document source n'est pas un paragraphe, rien ne sera fait.

## Exemples

Montre comment insérer un document en ligne à la position du curseur.

```csharp
DocumentBuilder srcDoc = new DocumentBuilder();
srcDoc.Write("[src content]");

// Créer un document de destination.
DocumentBuilder dstDoc = new DocumentBuilder();
dstDoc.Write("Before ");
dstDoc.InsertNode(new BookmarkStart(dstDoc.Document, "src_place"));
dstDoc.InsertNode(new BookmarkEnd(dstDoc.Document, "src_place"));
dstDoc.Write(" after");

Assert.AreEqual("Before  after", dstDoc.Document.GetText().TrimEnd());

// Insérer le document source dans la destination en ligne.
dstDoc.MoveToBookmark("src_place");
dstDoc.InsertDocumentInline(srcDoc.Document, ImportFormatMode.UseDestinationStyles, new ImportFormatOptions());

Assert.AreEqual("Before [src content] after", dstDoc.Document.GetText().TrimEnd());
```

### Voir également

* class [Node](../../node/)
* class [Document](../../document/)
* enum [ImportFormatMode](../../importformatmode/)
* class [ImportFormatOptions](../../importformatoptions/)
* class [DocumentBuilder](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)
