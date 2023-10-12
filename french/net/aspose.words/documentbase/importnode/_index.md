---
title: DocumentBase.ImportNode
second_title: Référence de l'API Aspose.Words pour .NET
description: DocumentBase méthode. Importe un nœud dun autre document vers le document actuel.
type: docs
weight: 100
url: /fr/net/aspose.words/documentbase/importnode/
---
## ImportNode(Node, bool) {#importnode}

Importe un nœud d'un autre document vers le document actuel.

```csharp
public Node ImportNode(Node srcNode, bool isImportChildren)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| srcNode | Node | Le nœud en cours d'importation. |
| isImportChildren | Boolean | `vrai` pour importer tous les nœuds enfants de manière récursive ; sinon,`FAUX`. |

### Return_Value

Le nœud cloné qui appartient au document actuel.

### Remarques

Cette méthode utilise leUseDestinationStyles option pour résoudre le formatage.

L'importation d'un nœud crée une copie du nœud source appartenant au document importateur. Le nœud renvoyé n'a pas de parent. Le nœud source n'est ni modifié ni supprimé du document d'origine.

Avant qu'un nœud d'un autre document puisse être inséré dans ce document, il doit être importé. Lors de l'importation, les propriétés spécifiques au document telles que les références aux styles et aux listes sont traduites de l'original vers le document d'importation. Une fois le nœud importé, il peut être inséré à l'endroit approprié dans le document en utilisantNode) ou Node).

Si le nœud source appartient déjà au document de destination, alors simplement un clone profond du nœud source est créé.

### Exemples

Montre comment importer un nœud d'un document à un autre.

```csharp
Document srcDoc = new Document();
Document dstDoc = new Document();

srcDoc.FirstSection.Body.FirstParagraph.AppendChild(
    new Run(srcDoc, "Source document first paragraph text."));
dstDoc.FirstSection.Body.FirstParagraph.AppendChild(
    new Run(dstDoc, "Destination document first paragraph text."));

// Chaque nœud a un document parent, qui est le document qui contient le nœud.
// L'insertion d'un nœud dans un document auquel le nœud n'appartient pas lèvera une exception.
Assert.AreNotEqual(dstDoc, srcDoc.FirstSection.Document);
Assert.Throws<ArgumentException>(() => { dstDoc.AppendChild(srcDoc.FirstSection); });

// Utilisez la méthode ImportNode pour créer une copie d'un nœud, qui contiendra le document
// qui a appelé la méthode ImportNode définie comme son nouveau document propriétaire.
Section importedSection = (Section)dstDoc.ImportNode(srcDoc.FirstSection, true);

Assert.AreEqual(dstDoc, importedSection.Document);

// Nous pouvons maintenant insérer le nœud dans le document.
dstDoc.AppendChild(importedSection);

Assert.AreEqual("Destination document first paragraph text.\r\nSource document first paragraph text.\r\n",
    dstDoc.ToString(SaveFormat.Text));
```

### Voir également

* class [Node](../../node/)
* class [DocumentBase](../)
* espace de noms [Aspose.Words](../../documentbase/)
* Assemblée [Aspose.Words](../../../)

---

## ImportNode(Node, bool, ImportFormatMode) {#importnode_1}

Importe un nœud d'un autre document vers le document actuel avec une option pour contrôler le formatage.

```csharp
public Node ImportNode(Node srcNode, bool isImportChildren, ImportFormatMode importFormatMode)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| srcNode | Node | Le nœud à importer. |
| isImportChildren | Boolean | `vrai` pour importer tous les nœuds enfants de manière récursive ; sinon,`FAUX`. |
| importFormatMode | ImportFormatMode | Spécifie comment fusionner le formatage de style en conflit. |

### Return_Value

Le nœud cloné et importé. Le nœud appartient au document de destination, mais n'a pas de parent.

### Remarques

Cette surcharge est utile pour contrôler la façon dont les styles et le formatage des listes sont importés.

L'importation d'un nœud crée une copie du nœud source appartenant au document importateur. Le nœud renvoyé n'a pas de parent. Le nœud source n'est ni modifié ni supprimé du document d'origine.

Avant qu'un nœud d'un autre document puisse être inséré dans ce document, il doit être importé. Lors de l'importation, les propriétés spécifiques au document telles que les références aux styles et aux listes sont traduites de l'original vers le document d'importation. Une fois le nœud importé, il peut être inséré à l'endroit approprié dans le document en utilisantNode) ou Node).

Si le nœud source appartient déjà au document de destination, alors simplement un clone profond du nœud source est créé.

### Exemples

Montre comment importer un nœud du document source vers le document de destination avec des options spécifiques.

```csharp
// Créez deux documents et ajoutez un style de caractère à chaque document.
// Configurez les styles pour qu'ils aient le même nom, mais un formatage de texte différent.
Document srcDoc = new Document();
Style srcStyle = srcDoc.Styles.Add(StyleType.Character, "My style");
srcStyle.Font.Name = "Courier New";
DocumentBuilder srcBuilder = new DocumentBuilder(srcDoc);
srcBuilder.Font.Style = srcStyle;
srcBuilder.Writeln("Source document text.");

Document dstDoc = new Document();
Style dstStyle = dstDoc.Styles.Add(StyleType.Character, "My style");
dstStyle.Font.Name = "Calibri";
DocumentBuilder dstBuilder = new DocumentBuilder(dstDoc);
dstBuilder.Font.Style = dstStyle;
dstBuilder.Writeln("Destination document text.");

// Importe la section du document de destination dans le document source, provoquant une collision de noms de style.
// Si nous utilisons des styles de destination, alors le texte source importé avec le même nom de style
// car le texte de destination adoptera le style de destination.
Section importedSection = (Section)dstDoc.ImportNode(srcDoc.FirstSection, true, ImportFormatMode.UseDestinationStyles);
Assert.AreEqual(dstStyle.Font.Name, importedSection.Body.FirstParagraph.Runs[0].Font.Name);
Assert.AreEqual(dstStyle.Name, importedSection.Body.FirstParagraph.Runs[0].Font.StyleName);

// Si on utilise ImportFormatMode.KeepDifferentStyles, le style source est conservé,
// et le conflit de noms est résolu en ajoutant un suffixe.
dstDoc.ImportNode(srcDoc.FirstSection, true, ImportFormatMode.KeepDifferentStyles);
Assert.AreEqual(dstStyle.Font.Name, dstDoc.Styles["My style"].Font.Name);
Assert.AreEqual(srcStyle.Font.Name, dstDoc.Styles["My style_0"].Font.Name);
```

### Voir également

* class [Node](../../node/)
* enum [ImportFormatMode](../../importformatmode/)
* class [DocumentBase](../)
* espace de noms [Aspose.Words](../../documentbase/)
* Assemblée [Aspose.Words](../../../)


