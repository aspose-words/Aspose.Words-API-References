---
title: FieldIncludeText.XPath
linktitle: XPath
articleTitle: XPath
second_title: Aspose.Words pour .NET
description: Découvrez la propriété XPath FieldIncludeText pour accéder et modifier facilement des sections XML spécifiques, améliorant ainsi l'efficacité de votre gestion des données.
type: docs
weight: 90
url: /fr/net/aspose.words.fields/fieldincludetext/xpath/
---
## FieldIncludeText.XPath property

Obtient ou définit XPath pour la partie souhaitée du fichier XML.

```csharp
public string XPath { get; set; }
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
