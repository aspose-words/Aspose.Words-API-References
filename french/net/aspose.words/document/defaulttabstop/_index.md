---
title: Document.DefaultTabStop
second_title: Référence de l'API Aspose.Words pour .NET
description: Document propriété. Obtient ou définit lintervalle en points entre les taquets de tabulation par défaut.
type: docs
weight: 90
url: /fr/net/aspose.words/document/defaulttabstop/
---
## Document.DefaultTabStop property

Obtient ou définit l'intervalle (en points) entre les taquets de tabulation par défaut.

```csharp
public double DefaultTabStop { get; set; }
```

### Exemples

Montre comment définir un intervalle personnalisé pour les positions des taquets de tabulation.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Définir les taquets de tabulation pour qu'ils apparaissent tous les 72 points (1 pouce).
builder.Document.DefaultTabStop = 72;

// Chaque caractère de tabulation accroche le texte qui le suit à la prochaine position de taquet de tabulation la plus proche.
builder.Writeln("Hello" + ControlChar.Tab + "World!");
builder.Writeln("Hello" + ControlChar.TabChar + "World!");
```

### Voir également

* class [TabStopCollection](../../tabstopcollection/)
* class [TabStop](../../tabstop/)
* class [Document](../)
* espace de noms [Aspose.Words](../../document/)
* Assemblée [Aspose.Words](../../../)


