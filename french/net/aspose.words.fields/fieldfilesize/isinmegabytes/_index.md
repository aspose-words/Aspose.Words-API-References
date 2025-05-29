---
title: FieldFileSize.IsInMegabytes
linktitle: IsInMegabytes
articleTitle: IsInMegabytes
second_title: Aspose.Words pour .NET
description: Contrôlez l'affichage de la taille des fichiers avec la propriété IsInMegabytes de FieldFileSize. Basculez facilement entre octets et mégaoctets pour une meilleure clarté et une meilleure expérience utilisateur.
type: docs
weight: 30
url: /fr/net/aspose.words.fields/fieldfilesize/isinmegabytes/
---
## FieldFileSize.IsInMegabytes property

Obtient ou définit s'il faut afficher la taille du fichier en mégaoctets.

```csharp
public bool IsInMegabytes { get; set; }
```

## Exemples

Montre comment afficher la taille du fichier d'un document avec un champ FILESIZE.

```csharp
Document doc = new Document(MyDir + "Document.docx");

Assert.AreEqual(18105, doc.BuiltInDocumentProperties.Bytes);

DocumentBuilder builder = new DocumentBuilder(doc);
builder.MoveToDocumentEnd();
builder.InsertParagraph();

// Vous trouverez ci-dessous trois unités de mesure différentes
// avec lesquels les champs FILESIZE peuvent afficher la taille du fichier du document.
// 1 - Octets :
FieldFileSize field = (FieldFileSize)builder.InsertField(FieldType.FieldFileSize, true);
field.Update();

Assert.AreEqual(" FILESIZE ", field.GetFieldCode());
Assert.AreEqual("18105", field.Result);

// 2 - Kilooctets :
builder.InsertParagraph();
field = (FieldFileSize)builder.InsertField(FieldType.FieldFileSize, true);
field.IsInKilobytes = true;
field.Update();

Assert.AreEqual(" FILESIZE  \\k", field.GetFieldCode());
Assert.AreEqual("18", field.Result);

// 3 - Mégaoctets :
builder.InsertParagraph();
field = (FieldFileSize)builder.InsertField(FieldType.FieldFileSize, true);
field.IsInMegabytes = true;
field.Update();

Assert.AreEqual(" FILESIZE  \\m", field.GetFieldCode());
Assert.AreEqual("0", field.Result);

// Pour mettre à jour les valeurs de ces champs lors de l'édition dans Microsoft Word,
// nous devons d'abord enregistrer les modifications, puis mettre à jour manuellement ces champs.
doc.Save(ArtifactsDir + "Field.FILESIZE.docx");
```

### Voir également

* class [FieldFileSize](../)
* espace de noms [Aspose.Words.Fields](../../../aspose.words.fields/)
* Assemblée [Aspose.Words](../../../)
