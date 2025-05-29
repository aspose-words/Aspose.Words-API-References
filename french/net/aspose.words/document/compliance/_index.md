---
title: Document.Compliance
linktitle: Compliance
articleTitle: Compliance
second_title: Aspose.Words pour .NET
description: Assurez-vous facilement que vos documents OOXML respectent les normes de conformité. Notre outil analyse le contenu pour vérifier la conformité OOXML et améliorer l'intégrité des documents.
type: docs
weight: 70
url: /fr/net/aspose.words/document/compliance/
---
## Document.Compliance property

Obtient la version de conformité OOXML déterminée à partir du contenu du document chargé. N'a de sens que pour les documents OOXML.

```csharp
public OoxmlCompliance Compliance { get; }
```

## Remarques

Si vous avez créé un nouveau document vierge ou chargé un document non OOXML, document renvoie leEcma376_2006 valeur.

## Exemples

Montre comment lire la version de conformité Open Office XML d'un document chargé.

```csharp
// La version de conformité varie selon les documents créés par différentes versions de Microsoft Word.
Document doc = new Document(MyDir + "Document.doc");
Assert.AreEqual(doc.Compliance, OoxmlCompliance.Ecma376_2006);

doc = new Document(MyDir + "Document.docx");
Assert.AreEqual(doc.Compliance, OoxmlCompliance.Iso29500_2008_Transitional);
```

### Voir également

* enum [OoxmlCompliance](../../../aspose.words.saving/ooxmlcompliance/)
* class [Document](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)
