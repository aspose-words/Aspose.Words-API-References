---
title: FieldHyperlink.IsImageMap
second_title: Référence de l'API Aspose.Words pour .NET
description: FieldHyperlink propriété. Obtient ou définit sil faut ajouter des coordonnées au lien hypertexte pour une image cliquable côté serveur.
type: docs
weight: 30
url: /fr/net/aspose.words.fields/fieldhyperlink/isimagemap/
---
## FieldHyperlink.IsImageMap property

Obtient ou définit s'il faut ajouter des coordonnées au lien hypertexte pour une image cliquable côté serveur.

```csharp
public bool IsImageMap { get; set; }
```

### Exemples

Montre comment utiliser les champs HYPERLINK pour créer un lien vers des documents dans le système de fichiers local.

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
* espace de noms [Aspose.Words.Fields](../../fieldhyperlink/)
* Assemblée [Aspose.Words](../../../)


