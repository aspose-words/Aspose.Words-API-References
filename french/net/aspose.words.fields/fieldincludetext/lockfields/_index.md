---
title: FieldIncludeText.LockFields
linktitle: LockFields
articleTitle: LockFields
second_title: Aspose.Words pour .NET
description: Contrôlez les mises à jour des documents avec la propriété LockFields de FieldIncludeText. Empêchez facilement la modification des champs inclus pour une meilleure intégrité des documents.
type: docs
weight: 40
url: /fr/net/aspose.words.fields/fieldincludetext/lockfields/
---
## FieldIncludeText.LockFields property

Obtient ou définit s'il faut empêcher la mise à jour des champs du document inclus.

```csharp
public bool LockFields { get; set; }
```

## Exemples

Montre comment créer un champ INCLUDETEXT et définir ses propriétés.

```csharp
public void FieldIncludeText()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    // Vous trouverez ci-dessous deux manières d'utiliser les champs INCLUDETEXT pour afficher le contenu d'un fichier XML dans le système de fichiers local.
    // 1 - Effectuer une transformation XSL sur un document XML :
    FieldIncludeText fieldIncludeText = CreateFieldIncludeText(builder, MyDir + "CD collection data.xml", false, "text/xml", "XML", "ISO-8859-1");
    fieldIncludeText.XslTransformation = MyDir + "CD collection XSL transformation.xsl";

    builder.Writeln();

    // 2 - Utiliser un XPath pour extraire des éléments spécifiques d'un document XML :
    fieldIncludeText = CreateFieldIncludeText(builder, MyDir + "CD collection data.xml", false, "text/xml", "XML", "ISO-8859-1");
    fieldIncludeText.NamespaceMappings = "xmlns:n='myNamespace'";
    fieldIncludeText.XPath = "/catalog/cd/title";

    doc.UpdateFields();
    doc.Save(ArtifactsDir + "Field.INCLUDETEXT.docx");
}

/// <summary>
/// Utilisez un générateur de documents pour insérer un champ INCLUDETEXT avec des propriétés personnalisées.
/// </summary>
public FieldIncludeText CreateFieldIncludeText(DocumentBuilder builder, string sourceFullName, bool lockFields, string mimeType, string textConverter, string encoding)
{
    FieldIncludeText fieldIncludeText = (FieldIncludeText)builder.InsertField(FieldType.FieldIncludeText, true);
    fieldIncludeText.SourceFullName = sourceFullName;
    fieldIncludeText.LockFields = lockFields;
    fieldIncludeText.MimeType = mimeType;
    fieldIncludeText.TextConverter = textConverter;
    fieldIncludeText.Encoding = encoding;

    return fieldIncludeText;
}
```

### Voir également

* class [FieldIncludeText](../)
* espace de noms [Aspose.Words.Fields](../../../aspose.words.fields/)
* Assemblée [Aspose.Words](../../../)
