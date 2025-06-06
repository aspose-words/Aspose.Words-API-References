---
title: FieldTC.TypeIdentifier
linktitle: TypeIdentifier
articleTitle: TypeIdentifier
second_title: Aspose.Words pour .NET
description: Découvrez la propriété FieldTC TypeIdentifier. Gérez facilement les identifiants de type de champ grâce à cette fonctionnalité polyvalente, améliorant ainsi l'organisation et l'efficacité de vos données.
type: docs
weight: 50
url: /fr/net/aspose.words.fields/fieldtc/typeidentifier/
---
## FieldTC.TypeIdentifier property

Obtient ou définit un identifiant de type pour ce champ (qui est généralement une lettre).

```csharp
public string TypeIdentifier { get; set; }
```

## Exemples

Montre comment insérer un champ TOC et filtrer les champs TC qui finissent par être des entrées.

```csharp
public void FieldTocEntryIdentifier()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    // Insérez un champ TOC, qui compilera tous les champs TC dans une table des matières.
    FieldToc fieldToc = (FieldToc)builder.InsertField(FieldType.FieldTOC, true);

    // Configurez le champ uniquement pour récupérer les entrées TC de type « A » et un niveau d'entrée compris entre 1 et 3.
    fieldToc.EntryIdentifier = "A";
    fieldToc.EntryLevelRange = "1-3";

    Assert.AreEqual(" TOC  \\f A \\l 1-3", fieldToc.GetFieldCode());

    // Ces deux entrées apparaîtront dans le tableau.
    builder.InsertBreak(BreakType.PageBreak);
    InsertTocEntry(builder, "TC field 1", "A", "1");
    InsertTocEntry(builder, "TC field 2", "A", "2");

    Assert.AreEqual(" TC  \"TC field 1\" \\n \\f A \\l 1", doc.Range.Fields[1].GetFieldCode());

    // Cette entrée sera omise du tableau car elle a un type différent de « A ».
    InsertTocEntry(builder, "TC field 3", "B", "1");

    // Cette entrée sera omise du tableau car elle a un niveau d'entrée en dehors de la plage 1-3.
    InsertTocEntry(builder, "TC field 4", "A", "5");

    doc.UpdateFields();
    doc.Save(ArtifactsDir + "Field.TC.docx");
}

/// <summary>
/// Utilisez un générateur de documents pour insérer un champ TC.
/// </summary>
public void InsertTocEntry(DocumentBuilder builder, string text, string typeIdentifier, string entryLevel)
{
    FieldTC fieldTc = (FieldTC)builder.InsertField(FieldType.FieldTOCEntry, true);
    fieldTc.OmitPageNumber = true;
    fieldTc.Text = text;
    fieldTc.TypeIdentifier = typeIdentifier;
    fieldTc.EntryLevel = entryLevel;
}
```

### Voir également

* class [FieldTC](../)
* espace de noms [Aspose.Words.Fields](../../../aspose.words.fields/)
* Assemblée [Aspose.Words](../../../)
