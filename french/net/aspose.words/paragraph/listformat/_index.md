---
title: Paragraph.ListFormat
linktitle: ListFormat
articleTitle: ListFormat
second_title: Aspose.Words pour .NET
description: Découvrez la propriété Paragraph ListFormat pour accéder et personnaliser facilement la mise en forme de la liste de vos paragraphes, améliorant ainsi la présentation de votre document.
type: docs
weight: 150
url: /fr/net/aspose.words/paragraph/listformat/
---
## Paragraph.ListFormat property

Donne accès aux propriétés de formatage de la liste du paragraphe.

```csharp
public ListFormat ListFormat { get; }
```

## Exemples

Montre comment générer tous les paragraphes d'un document qui sont des éléments de liste.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.ListFormat.ApplyNumberDefault();
builder.Writeln("Numbered list item 1");
builder.Writeln("Numbered list item 2");
builder.Writeln("Numbered list item 3");
builder.ListFormat.RemoveNumbers();

builder.ListFormat.ApplyBulletDefault();
builder.Writeln("Bulleted list item 1");
builder.Writeln("Bulleted list item 2");
builder.Writeln("Bulleted list item 3");
builder.ListFormat.RemoveNumbers();

NodeCollection paras = doc.GetChildNodes(NodeType.Paragraph, true);

foreach (Paragraph para in paras.OfType<Paragraph>().Where(p => p.ListFormat.IsListItem).ToList())
{ 
    Console.WriteLine($"This paragraph belongs to list ID# {para.ListFormat.List.ListId}, number style \"{para.ListFormat.ListLevel.NumberStyle}\"");
    Console.WriteLine($"\t\"{para.GetText().Trim()}\"");
}
```

### Voir également

* class [ListFormat](../../../aspose.words.lists/listformat/)
* class [Paragraph](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)
