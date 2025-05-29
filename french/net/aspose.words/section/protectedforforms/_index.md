---
title: Section.ProtectedForForms
linktitle: ProtectedForForms
articleTitle: ProtectedForForms
second_title: Aspose.Words pour .NET
description: Découvrez comment la propriété ProtectedForForms dans Microsoft Word améliore la sécurité des documents, permettant aux utilisateurs de modifier facilement uniquement les champs de formulaire désignés.
type: docs
weight: 60
url: /fr/net/aspose.words/section/protectedforforms/
---
## Section.ProtectedForForms property

Vrai si la section est protégée contre les formulaires. Lorsqu'une section est protégée contre les formulaires, les utilisateurs peuvent sélectionner et modifier du texte uniquement dans les champs de formulaire Microsoft Word.

```csharp
public bool ProtectedForForms { get; set; }
```

## Exemples

Montre comment désactiver la protection d'une section.

```csharp
Document doc = new Document();

DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Section 1. Hello world!");
builder.InsertBreak(BreakType.SectionBreakNewPage);

builder.Writeln("Section 2. Hello again!");
builder.Write("Please enter text here: ");
builder.InsertTextInput("TextInput1", TextFormFieldType.Regular, "", "Placeholder text", 0);

// Appliquer la protection en écriture à chaque section du document.
doc.Protect(ProtectionType.AllowOnlyFormFields);

// Désactiver la protection en écriture pour la première section.
doc.Sections[0].ProtectedForForms = false;

// Dans ce document de sortie, nous pourrons éditer librement la première section,
// et nous ne pourrons modifier que le contenu du champ de formulaire dans la deuxième section.
doc.Save(ArtifactsDir + "Section.Protect.docx");
```

### Voir également

* class [Section](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)
