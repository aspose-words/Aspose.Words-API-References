---
title: CompositeNode.GetText
second_title: Référence de l'API Aspose.Words pour .NET
description: CompositeNode méthode. Obtient le texte de ce nœud et de tous ses enfants.
type: docs
weight: 120
url: /fr/net/aspose.words/compositenode/gettext/
---
## CompositeNode.GetText method

Obtient le texte de ce nœud et de tous ses enfants.

```csharp
public override string GetText()
```

### Remarques

La chaîne renvoyée comprend tous les caractères de contrôle et spéciaux, comme décrit dans[`ControlChar`](../../controlchar/).

### Exemples

Montre la différence entre l'appel des méthodes GetText et ToString sur un nœud.

```csharp
Document doc = new Document();

DocumentBuilder builder = new DocumentBuilder(doc);
builder.InsertField("MERGEFIELD Field");

// GetText va récupérer le texte visible ainsi que les codes de champs et les caractères spéciaux.
Assert.AreEqual("\u0013MERGEFIELD Field\u0014«Field»\u0015\u000c", doc.GetText());

// ToString nous donnera l'apparence du document s'il est enregistré dans un format d'enregistrement passé.
Assert.AreEqual("«Field»\r\n", doc.ToString(SaveFormat.Text));
```

Montre comment sortir tous les paragraphes d'un document qui sont des éléments de liste.

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

* class [CompositeNode](../)
* espace de noms [Aspose.Words](../../compositenode/)
* Assemblée [Aspose.Words](../../../)


