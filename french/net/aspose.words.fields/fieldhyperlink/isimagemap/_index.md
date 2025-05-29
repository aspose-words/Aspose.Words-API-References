---
title: FieldHyperlink.IsImageMap
linktitle: IsImageMap
articleTitle: IsImageMap
second_title: Aspose.Words pour .NET
description: Découvrez comment la propriété FieldHyperlink IsImageMap améliore vos cartes d'images côté serveur en ajoutant des coordonnées aux hyperliens pour une fonctionnalité améliorée.
type: docs
weight: 30
url: /fr/net/aspose.words.fields/fieldhyperlink/isimagemap/
---
## FieldHyperlink.IsImageMap property

Obtient ou définit s'il faut ajouter des coordonnées au lien hypertexte pour une image cliquable côté serveur.

```csharp
public bool IsImageMap { get; set; }
```

## Exemples

Montre comment utiliser les champs HYPERLINK pour créer des liens vers des documents dans le système de fichiers local.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

FieldHyperlink field = (FieldHyperlink)builder.InsertField(FieldType.FieldHyperlink, true);

// Lorsque nous cliquons sur ce champ HYPERLINK dans Microsoft Word,
// il ouvrira le document lié puis placera le curseur sur le signet spécifié.
field.Address = MyDir + "Bookmarks.docx";
field.SubAddress = "MyBookmark3";
field.ScreenTip = "Open " + field.Address + " on bookmark " + field.SubAddress + " in a new window";

builder.Writeln();

// Lorsque nous cliquons sur ce champ HYPERLINK dans Microsoft Word,
// il ouvrira le document lié et défilera automatiquement jusqu'à l'iframe spécifié.
field = (FieldHyperlink)builder.InsertField(FieldType.FieldHyperlink, true);
field.Address = MyDir + "Iframes.html";
field.ScreenTip = "Open " + field.Address;
field.Target = "iframe_3";
field.OpenInNewWindow = true;
field.IsImageMap = false;

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.HYPERLINK.docx");
```

### Voir également

* class [FieldHyperlink](../)
* espace de noms [Aspose.Words.Fields](../../../aspose.words.fields/)
* Assemblée [Aspose.Words](../../../)
