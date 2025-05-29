---
title: FieldAutoTextList.ScreenTip
linktitle: ScreenTip
articleTitle: ScreenTip
second_title: Aspose.Words pour .NET
description: Découvrez la propriété ScreenTip FieldAutoTextList, personnalisez facilement votre texte ScreenTip pour une expérience utilisateur améliorée et une clarté dans votre application.
type: docs
weight: 40
url: /fr/net/aspose.words.fields/fieldautotextlist/screentip/
---
## FieldAutoTextList.ScreenTip property

Obtient ou définit le texte de l'info-bulle à afficher.

```csharp
public string ScreenTip { get; set; }
```

## Exemples

Montre comment utiliser un champ AUTOTEXTLIST pour sélectionner dans une liste d'entrées de texte automatique.

```csharp
public void FieldAutoTextList()
{
    Document doc = new Document();

    // Créez un document de glossaire et remplissez-le avec des entrées de texte automatiques.
    doc.GlossaryDocument = new GlossaryDocument();
    AppendAutoTextEntry(doc.GlossaryDocument, "AutoText 1", "Contents of AutoText 1");
    AppendAutoTextEntry(doc.GlossaryDocument, "AutoText 2", "Contents of AutoText 2");
    AppendAutoTextEntry(doc.GlossaryDocument, "AutoText 3", "Contents of AutoText 3");

    DocumentBuilder builder = new DocumentBuilder(doc);

    // Créez un champ AUTOTEXTLIST et définissez le texte que le champ affichera dans Microsoft Word.
    // Définissez le texte pour inviter l'utilisateur à cliquer avec le bouton droit sur ce champ pour sélectionner un bloc de construction de texte automatique,
    // dont le contenu sera affiché dans le champ.
    FieldAutoTextList field = (FieldAutoTextList)builder.InsertField(FieldType.FieldAutoTextList, true);
    field.EntryName = "Right click here to select an AutoText block";
    field.ListStyle = "Heading 1";
    field.ScreenTip = "Hover tip text for AutoTextList goes here";

    Assert.AreEqual(" AUTOTEXTLIST  \"Right click here to select an AutoText block\" " +
                    "\\s \"Heading 1\" " +
                    "\\t \"Hover tip text for AutoTextList goes here\"", field.GetFieldCode());

    doc.Save(ArtifactsDir + "Field.AUTOTEXTLIST.dotx");
}

/// <summary>
/// Créez un bloc de construction de type AutoText et ajoutez-le à un document de glossaire.
/// </summary>
private static void AppendAutoTextEntry(GlossaryDocument glossaryDoc, string name, string contents)
{
    BuildingBlock buildingBlock = new BuildingBlock(glossaryDoc);
    buildingBlock.Name = name;
    buildingBlock.Gallery = BuildingBlockGallery.AutoText;
    buildingBlock.Category = "General";
    buildingBlock.Behavior = BuildingBlockBehavior.Paragraph;

    Section section = new Section(glossaryDoc);
    section.AppendChild(new Body(glossaryDoc));
    section.Body.AppendParagraph(contents);
    buildingBlock.AppendChild(section);

    glossaryDoc.AppendChild(buildingBlock);
}
```

### Voir également

* class [FieldAutoTextList](../)
* espace de noms [Aspose.Words.Fields](../../../aspose.words.fields/)
* Assemblée [Aspose.Words](../../../)
