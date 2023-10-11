---
title: Paragraph.ListFormat
second_title: Référence de l'API Aspose.Words pour .NET
description: Paragraph propriété. Donne accès aux propriétés de formatage de liste du paragraphe.
type: docs
weight: 150
url: /fr/net/aspose.words/paragraph/listformat/
---
## Paragraph.ListFormat property

Donne accès aux propriétés de formatage de liste du paragraphe.

```csharp
public ListFormat ListFormat { get; }
```

### Exemples

Montre comment afficher tous les paragraphes d’un document qui sont des éléments de liste.

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

foreach (Paragraph para in paras.OfType<Paragraph>().Where(p => p.ListFormat.IsListItem))
{ 
    Console.WriteLine($"This paragraph belongs to list ID# {para.ListFormat.List.ListId}, number style \"{para.ListFormat.ListLevel.NumberStyle}\"");
    Console.WriteLine($"\t\"{para.GetText().Trim()}\"");
}
```

### Voir également

* class [ListFormat](../../../aspose.words.lists/listformat/)
* class [Paragraph](../)
* espace de noms [Aspose.Words](../../paragraph/)
* Assemblée [Aspose.Words](../../../)


