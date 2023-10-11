---
title: FieldHyperlink.OpenInNewWindow
second_title: Référence de l'API Aspose.Words pour .NET
description: FieldHyperlink propriété. Obtient ou définit sil faut ouvrir le site de destination dans une nouvelle fenêtre de navigateur Web.
type: docs
weight: 40
url: /fr/net/aspose.words.fields/fieldhyperlink/openinnewwindow/
---
## FieldHyperlink.OpenInNewWindow property

Obtient ou définit s'il faut ouvrir le site de destination dans une nouvelle fenêtre de navigateur Web.

```csharp
public bool OpenInNewWindow { get; set; }
```

### Exemples

Montre comment utiliser les champs HYPERLINK pour créer des liens vers des documents dans le système de fichiers local.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

FieldHyperlink field = (FieldHyperlink)builder.InsertField(FieldType.FieldHyperlink, true);

// Lorsque l'on clique sur ce champ HYPERLIEN dans Microsoft Word,
// il ouvrira le document lié puis placera le curseur sur le signet spécifié.
field.Address = MyDir + "Bookmarks.docx";
field.SubAddress = "MyBookmark3";
field.ScreenTip = "Open " + field.Address + " on bookmark " + field.SubAddress + " in a new window";

builder.Writeln();

// Lorsque l'on clique sur ce champ HYPERLIEN dans Microsoft Word,
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


