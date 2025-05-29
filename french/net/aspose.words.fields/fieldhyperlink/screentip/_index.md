---
title: FieldHyperlink.ScreenTip
linktitle: ScreenTip
articleTitle: ScreenTip
second_title: Aspose.Words pour .NET
description: Découvrez la propriété « FieldHyperlink ScreenTip » pour personnaliser le texte de vos liens hypertexte et améliorer l'expérience utilisateur et l'engagement. Optimisez vos liens dès aujourd'hui !
type: docs
weight: 50
url: /fr/net/aspose.words.fields/fieldhyperlink/screentip/
---
## FieldHyperlink.ScreenTip property

Obtient ou définit le texte de l'info-bulle pour le lien hypertexte.

```csharp
public string ScreenTip { get; set; }
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
