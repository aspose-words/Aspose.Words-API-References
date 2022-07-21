---
title: Protect
second_title: Référence de l'API Aspose.Words pour .NET
description: Protège le document des modifications sans modifier le mot de passe existant ou attribue un mot de passe aléatoire.
type: docs
weight: 630
url: /fr/net/aspose.words/document/protect/
---
## Protect(ProtectionType) {#protect}

Protège le document des modifications sans modifier le mot de passe existant ou attribue un mot de passe aléatoire.

```csharp
public void Protect(ProtectionType type)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| type | ProtectionType | Spécifie le type de protection du document. |

### Remarques

Lorsqu'un document est protégé, l'utilisateur ne peut apporter que des modifications limitées, telles que l'ajout d'annotations, la réalisation de révisions ou le remplissage d'un formulaire.

Lorsque vous protégez un document et que le document possède déjà un mot de passe de protection, le mot de passe de protection existant n'est pas modifié.

Lorsque vous protégez un document et que le document n'a pas de mot de passe de protection, cette méthode attribue un mot de passe aléatoire qui rend impossible la déprotection du document dans Microsoft Word, mais vous pouvez toujours déprotéger le document dans Aspose.Words car il ne le fait pas exiger un mot de passe lors de la suppression de la protection.

### Exemples

Montre comment désactiver la protection d'une section.

```csharp
Document doc = new Document();

DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Section 1. Hello world!");
builder.InsertBreak(BreakType.SectionBreakNewPage);

builder.Writeln("Section 2. Hello again!");
builder.Write("Please enter text here: ");
builder.InsertTextInput("TextInput1", TextFormFieldType.Regular, "", "Placeholder text", 0);

// Appliquez la protection en écriture à chaque section du document.
doc.Protect(ProtectionType.AllowOnlyFormFields);

// Désactiver la protection en écriture pour la première section.
doc.Sections[0].ProtectedForForms = false;

// Dans ce document de sortie, nous pourrons éditer librement la première section,
// et nous ne pourrons modifier que le contenu du champ du formulaire dans la deuxième section.
doc.Save(ArtifactsDir + "Section.Protect.docx");
```

### Voir également

* enum [ProtectionType](../../protectiontype)
* class [Document](../../document)
* espace de noms [Aspose.Words](../../document)
* Assemblée [Aspose.Words](../../../)

---

## Protect(ProtectionType, string) {#protect_1}

Protège le document des modifications et définit éventuellement un mot de passe de protection.

```csharp
public void Protect(ProtectionType type, string password)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| type | ProtectionType | Spécifie le type de protection du document. |
| password | String | Le mot de passe avec lequel protéger le document. Spécifiez une chaîne nulle ou vide si vous souhaitez protéger le document sans mot de passe. |

### Remarques

Lorsqu'un document est protégé, l'utilisateur ne peut apporter que des modifications limitées, telles que l'ajout d'annotations, la réalisation de révisions ou le remplissage d'un formulaire.

Notez que la protection du document est différente de la protection en écriture. La protection en écriture est spécifiée à l'aide de la[`WriteProtection`](../writeprotection).

### Exemples

Montre comment protéger et déprotéger un document.

```csharp
Document doc = new Document();
doc.Protect(ProtectionType.ReadOnly, "password");

Assert.AreEqual(ProtectionType.ReadOnly, doc.ProtectionType);

// Si nous ouvrons ce document avec Microsoft Word dans l'intention de le modifier,
// nous devrons appliquer le mot de passe pour passer la protection.
doc.Save(ArtifactsDir + "Document.Protect.docx");

// Notez que la protection ne s'applique qu'aux utilisateurs de Microsoft Word ouvrant notre document.
// Nous n'avons en aucun cas chiffré le document et nous n'avons pas besoin du mot de passe pour l'ouvrir et le modifier par programme.
Document protectedDoc = new Document(ArtifactsDir + "Document.Protect.docx");

Assert.AreEqual(ProtectionType.ReadOnly, protectedDoc.ProtectionType);

DocumentBuilder builder = new DocumentBuilder(protectedDoc);
builder.Writeln("Text added to a protected document.");
// Il existe deux manières de supprimer la protection d'un document.
// 1 - Sans mot de passe :
doc.Unprotect();

Assert.AreEqual(ProtectionType.NoProtection, doc.ProtectionType);

doc.Protect(ProtectionType.ReadOnly, "NewPassword");

Assert.AreEqual(ProtectionType.ReadOnly, doc.ProtectionType);

doc.Unprotect("WrongPassword");

Assert.AreEqual(ProtectionType.ReadOnly, doc.ProtectionType);

// 2 - Avec le bon mot de passe :
doc.Unprotect("NewPassword");

Assert.AreEqual(ProtectionType.NoProtection, doc.ProtectionType);
```

### Voir également

* enum [ProtectionType](../../protectiontype)
* class [Document](../../document)
* espace de noms [Aspose.Words](../../document)
* Assemblée [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
