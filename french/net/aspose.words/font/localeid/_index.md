---
title: Font.LocaleId
linktitle: LocaleId
articleTitle: LocaleId
second_title: Aspose.Words pour .NET
description: Découvrez comment la propriété Font LocaleId améliore la mise en forme de votre texte en gérant les identifiants régionaux pour différentes langues de caractères. Améliorez votre codage dès aujourd'hui !
type: docs
weight: 200
url: /fr/net/aspose.words/font/localeid/
---
## Font.LocaleId property

Obtient ou définit l'identifiant régional (langue) des caractères formatés.

```csharp
public int LocaleId { get; set; }
```

## Remarques

Pour la liste des identifiants de paramètres régionaux, voir https://msdn.microsoft.com/en-us/library/cc233965.aspx

## Exemples

Montre comment définir les paramètres régionaux du texte que nous ajoutons avec un générateur de documents.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Si nous définissons les paramètres régionaux de la police sur l'anglais et insérons du texte russe,
// Le correcteur orthographique local anglais ne reconnaîtra pas le texte et le détectera comme une erreur d'orthographe.
builder.Font.LocaleId = new CultureInfo("en-US", false).LCID;
builder.Writeln("Привет!");

// Définissez des paramètres régionaux correspondants pour le texte que nous sommes sur le point d'ajouter pour appliquer le correcteur orthographique approprié.
builder.Font.LocaleId = new CultureInfo("ru-RU", false).LCID;
builder.Writeln("Привет!");

doc.Save(ArtifactsDir + "Font.LocaleId.docx");
```

### Voir également

* class [Font](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)
