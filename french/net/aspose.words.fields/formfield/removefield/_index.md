---
title: FormField.RemoveField
linktitle: RemoveField
articleTitle: RemoveField
second_title: Aspose.Words pour .NET
description: Supprimez sans effort des champs de formulaire entiers avec la méthode FormField RemoveField, améliorant ainsi la clarté et l'organisation de votre document.
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

S'il existe un signet associé au champ de formulaire, le signet n'est pas supprimé.

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
