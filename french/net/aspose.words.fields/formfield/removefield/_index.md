---
title: FormField.RemoveField
linktitle: RemoveField
articleTitle: RemoveField
second_title: Aspose.Words pour .NET
description: FormField RemoveField méthode. Supprime le champ de formulaire complet pas seulement le caractère spécial du champ de formulaire en C#.
type: docs
weight: 240
url: /fr/net/aspose.words.fields/formfield/removefield/
---
## FormField.RemoveField method

Supprime le champ de formulaire complet, pas seulement le caractère spécial du champ de formulaire.

```csharp
public void RemoveField()
```

## Remarques

S'il existe un signet associé au champ du formulaire, le signet n'est pas supprimé.

## Exemples

Montre comment supprimer un champ de formulaire.

```csharp
Document doc = new Document(MyDir + "Form fields.docx");

FormField formField = doc.Range.FormFields[3];
formField.RemoveField();
```

### Voir également

* class [FormField](../)
* espace de noms [Aspose.Words.Fields](../../../aspose.words.fields/)
* Assemblée [Aspose.Words](../../../)
