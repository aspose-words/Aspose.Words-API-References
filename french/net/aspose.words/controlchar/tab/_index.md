---
title: ControlChar.Tab
second_title: Référence de l'API Aspose.Words pour .NET
description: ControlChar champ. Caractère de tabulation  x0009 ou t.
type: docs
weight: 270
url: /fr/net/aspose.words/controlchar/tab/
---
## ControlChar.Tab field

Caractère de tabulation : "\x0009" ou "\t".

```csharp
public static readonly string Tab;
```

### Exemples

Montre comment définir un intervalle personnalisé pour les positions des taquets de tabulation.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Définit les taquets de tabulation pour qu'ils apparaissent tous les 72 points (1 pouce).
builder.Document.DefaultTabStop = 72;

// Chaque caractère de tabulation accroche le texte qui le suit à la position de taquet de tabulation la plus proche.
builder.Writeln("Hello" + ControlChar.Tab + "World!");
builder.Writeln("Hello" + ControlChar.TabChar + "World!");
```

### Voir également

* class [ControlChar](../)
* espace de noms [Aspose.Words](../../controlchar/)
* Assemblée [Aspose.Words](../../../)


