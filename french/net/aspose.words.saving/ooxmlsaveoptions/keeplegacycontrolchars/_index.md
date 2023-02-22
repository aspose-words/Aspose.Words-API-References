---
title: OoxmlSaveOptions.KeepLegacyControlChars
second_title: Référence de l'API Aspose.Words pour .NET
description: OoxmlSaveOptions propriété. Conserve la représentation originale des caractères de contrôle hérités.
type: docs
weight: 40
url: /fr/net/aspose.words.saving/ooxmlsaveoptions/keeplegacycontrolchars/
---
## OoxmlSaveOptions.KeepLegacyControlChars property

Conserve la représentation originale des caractères de contrôle hérités.

```csharp
public bool KeepLegacyControlChars { get; set; }
```

### Exemples

Montre comment prendre en charge les caractères de contrôle hérités lors de la conversion en .docx.

```csharp
Document doc = new Document(MyDir + "Legacy control character.doc");

// Lorsque nous enregistrons le document au format OOXML, nous pouvons créer un objet OoxmlSaveOptions
// puis passez-le à la méthode d'enregistrement du document pour modifier la façon dont nous enregistrons le document.
// Définissez la propriété "KeepLegacyControlChars" sur "true" pour conserver
// le caractère hérité "ShortDateTime" lors de l'enregistrement.
// Définissez la propriété "KeepLegacyControlChars" sur "false" pour supprimer
// le caractère hérité "ShortDateTime" du document de sortie.
OoxmlSaveOptions so = new OoxmlSaveOptions(SaveFormat.Docx);
so.KeepLegacyControlChars = keepLegacyControlChars;

doc.Save(ArtifactsDir + "OoxmlSaveOptions.KeepLegacyControlChars.docx", so);

doc = new Document(ArtifactsDir + "OoxmlSaveOptions.KeepLegacyControlChars.docx");

Assert.AreEqual(keepLegacyControlChars ? "\u0013date \\@ \"MM/dd/yyyy\"\u0014\u0015\f" : "\u001e\f",
    doc.FirstSection.Body.GetText());
```

### Voir également

* class [OoxmlSaveOptions](../)
* espace de noms [Aspose.Words.Saving](../../ooxmlsaveoptions/)
* Assemblée [Aspose.Words](../../../)


