---
title: ProtectionType Enum
linktitle: ProtectionType
articleTitle: ProtectionType
second_title: Aspose.Words pour .NET
description: Découvrez l'énumération Aspose.Words.ProtectionType pour une sécurité renforcée de vos documents. Améliorez vos documents grâce à des options de protection personnalisables dès aujourd'hui !
type: docs
weight: 5240
url: /fr/net/aspose.words/protectiontype/
---
## ProtectionType enumeration

Type de protection pour un document.

```csharp
public enum ProtectionType
```

### Valeurs

| Nom | Évaluer | La description |
| --- | --- | --- |
| AllowOnlyComments | `1` | L'utilisateur peut uniquement modifier les commentaires dans le document. |
| AllowOnlyFormFields | `2` | L'utilisateur ne peut saisir des données que dans les champs de formulaire du document. |
| AllowOnlyRevisions | `0` | L'utilisateur peut uniquement ajouter des marques de révision au document. |
| ReadOnly | `3` | Aucune modification n'est autorisée sur le document. Disponible depuis Microsoft Word 2003. |
| NoProtection | `-1` | Le document n'est pas protégé. |

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

* espace de noms [Aspose.Words](../../aspose.words/)
* Assemblée [Aspose.Words](../../)
