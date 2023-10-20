---
title: Section.ProtectedForForms
linktitle: ProtectedForForms
articleTitle: ProtectedForForms
second_title: Aspose.Words pour .NET
description: Section ProtectedForForms propriété. True si la section est protégée pour les formulaires. Lorsquune section est protégée pour les formulaires les utilisateurs peuvent sélectionner et modifier le texte uniquement dans les champs de formulaire de Microsoft Word en C#.
type: docs
weight: 60
url: /fr/net/aspose.words/section/protectedforforms/
---
## Section.ProtectedForForms property

True si la section est protégée pour les formulaires. Lorsqu'une section est protégée pour les formulaires, les utilisateurs peuvent sélectionner et modifier le texte uniquement dans les champs de formulaire de Microsoft Word.

```csharp
public bool ProtectedForForms { get; set; }
```

## Exemples

Montre comment désactiver la protection d’une section.

```csharp
Document doc = new Document();

DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Section 1. Hello world!");
builder.InsertBreak(BreakType.SectionBreakNewPage);

builder.Writeln("Section 2. Hello again!");
builder.Write("Please enter text here: ");
builder.InsertTextInput("TextInput1", TextFormFieldType.Regular, "", "Placeholder text", 0);

// Applique une protection en écriture à chaque section du document.
doc.Protect(ProtectionType.AllowOnlyFormFields);

// Désactive la protection en écriture pour la première section.
doc.Sections[0].ProtectedForForms = false;

// Dans ce document de sortie, nous pourrons éditer librement la première section,
// et nous ne pourrons éditer que le contenu du champ du formulaire dans la deuxième section.
doc.Save(ArtifactsDir + "Section.Protect.docx");
```

### Voir également

* class [Section](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)
