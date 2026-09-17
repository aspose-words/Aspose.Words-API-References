---
title: "Aspose::Words::Saving::OoxmlSaveOptions::get_KeepLegacyControlChars méthode"
linktitle: "get_KeepLegacyControlChars"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Saving::OoxmlSaveOptions::get_KeepLegacyControlChars méthode. Conserve la représentation originale des caractères de contrôle hérités en C++."
type: docs
weight: 5000
url: /fr/cpp/aspose.words.saving/ooxmlsaveoptions/get_keeplegacycontrolchars/
---
## OoxmlSaveOptions::get_KeepLegacyControlChars method


Conserve la représentation originale des caractères de contrôle hérités.

```cpp
bool Aspose::Words::Saving::OoxmlSaveOptions::get_KeepLegacyControlChars() const
```


## Exemples



Montre comment prendre en charge les caractères de contrôle hérités lors de la conversion en .docx.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Legacy control character.doc");

// Lorsque nous enregistrons le document au format OOXML, nous pouvons créer un objet OoxmlSaveOptions
// et le transmettre ensuite à la méthode d'enregistrement du document pour modifier la façon dont nous enregistrons le document.
// Définissez la propriété "KeepLegacyControlChars" sur "true" pour conserver
// le caractère hérité "ShortDateTime" lors de l'enregistrement.
// Définissez la propriété "KeepLegacyControlChars" sur "false" pour supprimer
// le caractère hérité "ShortDateTime" du document de sortie.
auto so = System::MakeObject<Aspose::Words::Saving::OoxmlSaveOptions>(Aspose::Words::SaveFormat::Docx);
so->set_KeepLegacyControlChars(keepLegacyControlChars);

doc->Save(get_ArtifactsDir() + u"OoxmlSaveOptions.KeepLegacyControlChars.docx", so);

doc = System::MakeObject<Aspose::Words::Document>(get_ArtifactsDir() + u"OoxmlSaveOptions.KeepLegacyControlChars.docx");

ASSERT_EQ(keepLegacyControlChars ? System::String(u"\u0013date \\@ \"MM/dd/yyyy\"\u0014\u0015\f") : System::String(u"\u001e\f"), doc->get_FirstSection()->get_Body()->GetText());
```

## Voir aussi

* Class [OoxmlSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
