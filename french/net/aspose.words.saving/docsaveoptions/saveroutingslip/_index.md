---
title: DocSaveOptions.SaveRoutingSlip
second_title: Référence de l'API Aspose.Words pour .NET
description: DocSaveOptions propriété. QuandFAUX  les données Routingslip ne sont pas enregistrées dans le document de sortie. La valeur par défaut estvrai .
type: docs
weight: 60
url: /fr/net/aspose.words.saving/docsaveoptions/saveroutingslip/
---
## DocSaveOptions.SaveRoutingSlip property

Quand`FAUX` , les données Routingslip ne sont pas enregistrées dans le document de sortie. La valeur par défaut est`vrai` .

```csharp
public bool SaveRoutingSlip { get; set; }
```

### Exemples

Montre comment définir les options d’enregistrement pour les anciens formats Microsoft Word.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Write("Hello world!");

DocSaveOptions options = new DocSaveOptions(SaveFormat.Doc);

// Définir un mot de passe qui protégera le chargement du document par Microsoft Word ou Aspose.Words.
// Notez que cela ne crypte en aucun cas le contenu du document.
options.Password = "MyPassword";

// Si le document contient un bordereau de routage, nous pouvons le conserver lors de l'enregistrement en mettant cet indicateur à true.
options.SaveRoutingSlip = true;

doc.Save(ArtifactsDir + "DocSaveOptions.SaveAsDoc.doc", options);

// Pour pouvoir charger le document,
// nous devrons appliquer le mot de passe que nous avons spécifié dans l'objet DocSaveOptions dans un objet LoadOptions.
Assert.Throws<IncorrectPasswordException>(() => doc = new Document(ArtifactsDir + "DocSaveOptions.SaveAsDoc.doc"));

LoadOptions loadOptions = new LoadOptions("MyPassword");
doc = new Document(ArtifactsDir + "DocSaveOptions.SaveAsDoc.doc", loadOptions);

Assert.AreEqual("Hello world!", doc.GetText().Trim());
```

### Voir également

* class [DocSaveOptions](../)
* espace de noms [Aspose.Words.Saving](../../docsaveoptions/)
* Assemblée [Aspose.Words](../../../)


