---
title: ControlChar.Cr
linktitle: Cr
articleTitle: Cr
second_title: Aspose.Words pour .NET
description: ControlChar Cr champ. Caractère de retour chariot  x000d ou r. Pareil queParagraphBreak  en C#.
type: docs
weight: 50
url: /fr/net/aspose.words/controlchar/cr/
---
## ControlChar.Cr field

Caractère de retour chariot : "\x000d" ou "\r". Pareil que[`ParagraphBreak`](../paragraphbreak/) .

```csharp
public static readonly string Cr;
```

## Exemples

Montre comment utiliser les caractères de contrôle.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Insérez des paragraphes avec du texte avec DocumentBuilder.
builder.Writeln("Hello world!");
builder.Writeln("Hello again!");

// La conversion du document sous forme de texte révèle que les caractères de contrôle
// représente certains des éléments structurels du document, tels que les sauts de page.
Assert.AreEqual($"Hello world!{ControlChar.Cr}" +
                $"Hello again!{ControlChar.Cr}" +
                ControlChar.PageBreak, doc.GetText());

// Lors de la conversion d'un document sous forme de chaîne,
// nous pouvons omettre certains caractères de contrôle avec la méthode Trim.
Assert.AreEqual($"Hello world!{ControlChar.Cr}" +
                "Hello again!", doc.GetText().Trim());
```

### Voir également

* class [ControlChar](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)
