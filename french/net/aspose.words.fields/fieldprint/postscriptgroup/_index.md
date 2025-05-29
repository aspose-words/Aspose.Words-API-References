---
title: FieldPrint.PostScriptGroup
linktitle: PostScriptGroup
articleTitle: PostScriptGroup
second_title: Aspose.Words pour .NET
description: Découvrez la propriété FieldPrint PostScriptGroup pour gérer facilement votre rectangle de dessin pour une gestion efficace des instructions PostScript.
type: docs
weight: 20
url: /fr/net/aspose.words.fields/fieldprint/postscriptgroup/
---
## FieldPrint.PostScriptGroup property

Obtient ou définit le rectangle de dessin sur lequel opèrent les instructions PostScript.

```csharp
public string PostScriptGroup { get; set; }
```

## Exemples

Affiche l'insertion d'un champ IMPRIMER.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("My paragraph");

// Le champ IMPRIMER peut envoyer des instructions à l'imprimante.
FieldPrint field = (FieldPrint)builder.InsertField(FieldType.FieldPrint, true);

// Définissez la zone sur laquelle l'imprimante doit exécuter les instructions.
// Dans ce cas, ce sera le paragraphe qui contiendra notre champ PRINT.
field.PostScriptGroup = "para";

// Lorsque nous utilisons une imprimante prenant en charge PostScript pour imprimer notre document,
// cette commande rendra blanche toute la zone que nous avons spécifiée dans "field.PostScriptGroup".
field.PrinterInstructions = "erasepage";

Assert.AreEqual(" PRINT  erasepage \\p para", field.GetFieldCode());

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.PRINT.docx");
```

### Voir également

* class [FieldPrint](../)
* espace de noms [Aspose.Words.Fields](../../../aspose.words.fields/)
* Assemblée [Aspose.Words](../../../)
