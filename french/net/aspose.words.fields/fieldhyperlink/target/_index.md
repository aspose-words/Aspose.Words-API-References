---
title: FieldHyperlink.Target
linktitle: Target
articleTitle: Target
second_title: Aspose.Words pour .NET
description: Découvrez la propriété FieldHyperlink Target, configurez facilement la redirection de lien pour une navigation utilisateur améliorée et des expériences Web transparentes.
type: docs
weight: 70
url: /fr/net/aspose.words.fields/fieldhyperlink/target/
---
## FieldHyperlink.Target property

Obtient ou définit la cible vers laquelle le lien doit être redirigé.

```csharp
public string Target { get; set; }
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
