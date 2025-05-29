---
title: Document.DefaultTabStop
linktitle: DefaultTabStop
articleTitle: DefaultTabStop
second_title: Aspose.Words pour .NET
description: Découvrez comment personnaliser la propriété DefaultTabStop pour définir des intervalles de tabulation précis en points, améliorant ainsi la mise en forme et la mise en page de votre document.
type: docs
weight: 100
url: /fr/net/aspose.words/document/defaulttabstop/
---
## Document.DefaultTabStop property

Obtient ou définit l'intervalle (en points) entre les taquets de tabulation par défaut.

```csharp
public double DefaultTabStop { get; set; }
```

## Exemples

Montre comment définir un intervalle personnalisé pour les positions des taquets de tabulation.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Définissez les taquets de tabulation pour qu'ils apparaissent tous les 72 points (1 pouce).
builder.Document.DefaultTabStop = 72;

// Chaque caractère de tabulation accroche le texte qui le suit à la position de tabulation la plus proche.
builder.Writeln("Hello" + ControlChar.Tab + "World!");
builder.Writeln("Hello" + ControlChar.TabChar + "World!");
```

### Voir également

* class [TabStopCollection](../../tabstopcollection/)
* class [TabStop](../../tabstop/)
* class [Document](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)
