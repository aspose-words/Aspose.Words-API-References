---
title: Document.RemoveMacros
second_title: Référence de l'API Aspose.Words pour .NET
description: Document méthode. Supprime toutes les macros le projet VBA ainsi que les barres doutils et les personnalisations de commande du document.
type: docs
weight: 650
url: /fr/net/aspose.words/document/removemacros/
---
## Document.RemoveMacros method

Supprime toutes les macros (le projet VBA) ainsi que les barres d'outils et les personnalisations de commande du document.

```csharp
public void RemoveMacros()
```

### Remarques

En supprimant toutes les macros d'un document, vous pouvez vous assurer que le document ne contient aucun virus de macro.

### Exemples

Montre comment supprimer toutes les macros d'un document.

```csharp
Document doc = new Document(MyDir + "Macro.docm");

Assert.IsTrue(doc.HasMacros);
Assert.AreEqual("Project", doc.VbaProject.Name);

// Supprime le projet VBA du document, ainsi que toutes ses macros.
doc.RemoveMacros();

Assert.IsFalse(doc.HasMacros);
Assert.Null(doc.VbaProject);
```

### Voir également

* class [Document](../)
* espace de noms [Aspose.Words](../../document/)
* Assemblée [Aspose.Words](../../../)


