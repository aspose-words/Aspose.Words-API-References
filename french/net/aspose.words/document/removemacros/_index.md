---
title: Document.RemoveMacros
linktitle: RemoveMacros
articleTitle: RemoveMacros
second_title: Aspose.Words pour .NET
description: Supprimez sans effort toutes les macros, barres d'outils et paramètres de commande personnalisés de votre projet VBA avec la méthode Document RemoveMacros pour un document plus propre.
type: docs
weight: 720
url: /fr/net/aspose.words/document/removemacros/
---
## Document.RemoveMacros method

Supprime toutes les macros (le projet VBA) ainsi que les barres d'outils et les personnalisations de commandes du document.

```csharp
public void RemoveMacros()
```

## Remarques

En supprimant toutes les macros d’un document, vous pouvez garantir que le document ne contient aucun virus de macro.

## Exemples

Montre comment supprimer toutes les macros d'un document.

```csharp
Document doc = new Document(MyDir + "Macro.docm");

Assert.IsTrue(doc.HasMacros);
Assert.AreEqual("Project", doc.VbaProject.Name);

// Supprimez le projet VBA du document, ainsi que toutes ses macros.
doc.RemoveMacros();

Assert.IsFalse(doc.HasMacros);
Assert.Null(doc.VbaProject);
```

### Voir également

* class [Document](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)
