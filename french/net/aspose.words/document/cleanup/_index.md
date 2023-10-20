---
title: Document.Cleanup
linktitle: Cleanup
articleTitle: Cleanup
second_title: Aspose.Words pour .NET
description: Document Cleanup méthode. Nettoie les styles et les listes inutilisés du document en C#.
type: docs
weight: 540
url: /fr/net/aspose.words/document/cleanup/
---
## Cleanup() {#cleanup}

Nettoie les styles et les listes inutilisés du document.

```csharp
public void Cleanup()
```

## Exemples

Montre comment supprimer les styles personnalisés inutilisés d’un document.

```csharp
Document doc = new Document();

doc.Styles.Add(StyleType.List, "MyListStyle1");
doc.Styles.Add(StyleType.List, "MyListStyle2");
doc.Styles.Add(StyleType.Character, "MyParagraphStyle1");
doc.Styles.Add(StyleType.Character, "MyParagraphStyle2");

// Combiné avec les styles intégrés, le document dispose désormais de huit styles.
// Un style personnalisé compte comme "utilisé" lorsqu'il est appliqué à une partie du document,
// ce qui signifie que les quatre styles que nous avons ajoutés sont actuellement inutilisés.
Assert.AreEqual(8, doc.Styles.Count);

// Applique un style de caractère personnalisé, puis un style de liste personnalisé. Cela marquera les styles comme « utilisés ».
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Font.Style = doc.Styles["MyParagraphStyle1"];
builder.Writeln("Hello world!");

Aspose.Words.Lists.List list = doc.Lists.Add(doc.Styles["MyListStyle1"]);
builder.ListFormat.List = list;
builder.Writeln("Item 1");
builder.Writeln("Item 2");

doc.Cleanup();

Assert.AreEqual(6, doc.Styles.Count);

// La suppression de chaque nœud auquel un style personnalisé est appliqué le marque à nouveau comme "inutilisé".
// Exécutez à nouveau la méthode Cleanup pour les supprimer.
doc.FirstSection.Body.RemoveAllChildren();
doc.Cleanup();

Assert.AreEqual(4, doc.Styles.Count);
```

### Voir également

* class [Document](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)

---

## Cleanup(*[CleanupOptions](../../cleanupoptions/)*) {#cleanup_1}

Nettoie les styles et les listes inutilisés du document en fonction des données[`CleanupOptions`](../../cleanupoptions/) .

```csharp
public void Cleanup(CleanupOptions options)
```

## Exemples

Montre comment supprimer tous les styles personnalisés inutilisés d’un document.

```csharp
Document doc = new Document();

doc.Styles.Add(StyleType.List, "MyListStyle1");
doc.Styles.Add(StyleType.List, "MyListStyle2");
doc.Styles.Add(StyleType.Character, "MyParagraphStyle1");
doc.Styles.Add(StyleType.Character, "MyParagraphStyle2");

// Combiné avec les styles intégrés, le document dispose désormais de huit styles.
// Un style personnalisé est marqué comme "utilisé" alors qu'il y a du texte dans le document
// formaté dans ce style. Cela signifie que les 4 styles que nous avons ajoutés sont actuellement inutilisés.
Assert.AreEqual(8, doc.Styles.Count);

// Applique un style de caractère personnalisé, puis un style de liste personnalisé. Cela les marquera comme « utilisés ».
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Font.Style = doc.Styles["MyParagraphStyle1"];
builder.Writeln("Hello world!");

Aspose.Words.Lists.List list = doc.Lists.Add(doc.Styles["MyListStyle1"]);
builder.ListFormat.List = list;
builder.Writeln("Item 1");
builder.Writeln("Item 2");

// Il existe désormais un style de caractère et un style de liste inutilisés.
// La méthode Cleanup(), lorsqu'elle est configurée avec un objet CleanupOptions, peut cibler les styles inutilisés et les supprimer.
CleanupOptions cleanupOptions = new CleanupOptions
{
    UnusedLists = true, UnusedStyles = true, UnusedBuiltinStyles = true
};

doc.Cleanup(cleanupOptions);

Assert.AreEqual(4, doc.Styles.Count);

 // La suppression de chaque nœud auquel un style personnalisé est appliqué le marque à nouveau comme "inutilisé".
// Réexécutez la méthode Cleanup pour les supprimer.
doc.FirstSection.Body.RemoveAllChildren();
doc.Cleanup(cleanupOptions);

Assert.AreEqual(2, doc.Styles.Count);
```

### Voir également

* class [CleanupOptions](../../cleanupoptions/)
* class [Document](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)
