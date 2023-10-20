---
title: PlainTextDocument Class
linktitle: PlainTextDocument
articleTitle: PlainTextDocument
second_title: Aspose.Words pour .NET
description: Aspose.Words.PlainTextDocument classe. Permet dextraire une représentation en texte brut du contenu du document en C#.
type: docs
weight: 4440
url: /fr/net/aspose.words/plaintextdocument/
---
## PlainTextDocument class

Permet d'extraire une représentation en texte brut du contenu du document.

Pour en savoir plus, visitez le[Travailler avec un document texte](https://docs.aspose.com/words/net/working-with-text-document/) article documentaire.

```csharp
public class PlainTextDocument
```

## Constructeurs

| Nom | La description |
| --- | --- |
| [PlainTextDocument](plaintextdocument/#constructor)(*Stream*) | Crée un document en texte brut à partir d'un flux. Détecte automatiquement le format de fichier. |
| [PlainTextDocument](plaintextdocument/#constructor_2)(*string*) | Crée un document en texte brut à partir d'un fichier. Détecte automatiquement le format de fichier. |
| [PlainTextDocument](plaintextdocument/#constructor_1)(*Stream, [LoadOptions](../../aspose.words.loading/loadoptions/)*) | Crée un document en texte brut à partir d'un flux. Permet de spécifier des options supplémentaires telles qu'un mot de passe de cryptage. |
| [PlainTextDocument](plaintextdocument/#constructor_3)(*string, [LoadOptions](../../aspose.words.loading/loadoptions/)*) | Crée un document en texte brut à partir d'un fichier. Permet de spécifier des options supplémentaires telles qu'un mot de passe de cryptage. |

## Propriétés

| Nom | La description |
| --- | --- |
| [BuiltInDocumentProperties](../../aspose.words/plaintextdocument/builtindocumentproperties/) { get; } | Obtient[`BuiltInDocumentProperties`](./builtindocumentproperties/) du document. |
| [CustomDocumentProperties](../../aspose.words/plaintextdocument/customdocumentproperties/) { get; } | Obtient[`CustomDocumentProperties`](./customdocumentproperties/) du document. |
| [Text](../../aspose.words/plaintextdocument/text/) { get; } | Obtient le contenu textuel du document concaténé sous forme de chaîne. |

## Exemples

Montre comment charger le contenu d'un document Microsoft Word en texte brut.

```csharp
Document doc = new Document(); 
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Hello world!");

doc.Save(ArtifactsDir + "PlainTextDocument.Load.docx");

PlainTextDocument plaintext = new PlainTextDocument(ArtifactsDir + "PlainTextDocument.Load.docx");

Assert.AreEqual("Hello world!", plaintext.Text.Trim());
```

### Voir également

* espace de noms [Aspose.Words](../../aspose.words/)
* Assemblée [Aspose.Words](../../)
