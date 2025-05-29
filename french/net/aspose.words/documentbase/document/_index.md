---
title: DocumentBase.Document
linktitle: Document
articleTitle: Document
second_title: Aspose.Words pour .NET
description: Explorez les propriétés de DocumentBase pour gérer efficacement vos documents. Accédez à un accès fluide et optimisez votre flux de travail dès aujourd'hui !
type: docs
weight: 20
url: /fr/net/aspose.words/documentbase/document/
---
## DocumentBase.Document property

Obtient cette instance.

```csharp
public override DocumentBase Document { get; }
```

## Exemples

Montre comment créer un document simple.

```csharp
Document doc = new Document();

// Les nouveaux objets Document sont livrés par défaut avec l'ensemble minimal de nœuds
// requis pour commencer à ajouter du contenu tel que du texte et des formes : une section, un corps et un paragraphe.
doc.AppendChild(new Section(doc))
    .AppendChild(new Body(doc))
    .AppendChild(new Paragraph(doc))
    .AppendChild(new Run(doc, "Hello world!"));
```

### Voir également

* class [DocumentBase](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)
