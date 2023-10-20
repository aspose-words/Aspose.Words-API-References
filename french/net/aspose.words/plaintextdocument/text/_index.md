---
title: PlainTextDocument.Text
linktitle: Text
articleTitle: Text
second_title: Aspose.Words pour .NET
description: PlainTextDocument Text propriété. Obtient le contenu textuel du document concaténé sous forme de chaîne en C#.
type: docs
weight: 40
url: /fr/net/aspose.words/plaintextdocument/text/
---
## PlainTextDocument.Text property

Obtient le contenu textuel du document concaténé sous forme de chaîne.

```csharp
public string Text { get; }
```

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

* class [PlainTextDocument](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)
