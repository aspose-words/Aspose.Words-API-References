---
title: ControlChar.Tab
linktitle: Tab
articleTitle: Tab
second_title: Aspose.Words pour .NET
description: Découvrez le champ Tab ControlChar, comprenez le caractère Tab x0009 pour un formatage de texte efficace et une gestion améliorée des données.
type: docs
weight: 270
url: /fr/net/aspose.words/controlchar/tab/
---
## ControlChar.Tab field

Caractère de tabulation : « \x0009 » ou « \t ».

```csharp
public static readonly string Tab;
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

* class [ControlChar](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)
