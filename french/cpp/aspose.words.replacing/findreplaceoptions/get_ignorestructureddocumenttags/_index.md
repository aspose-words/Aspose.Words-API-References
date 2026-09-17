---
title: "Méthode Aspose::Words::Replacing::FindReplaceOptions::get_IgnoreStructuredDocumentTags"
linktitle: "get_IgnoreStructuredDocumentTags"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Replacing::FindReplaceOptions::get_IgnoreStructuredDocumentTags method. Obtient ou définit une valeur booléenne indiquant s'il faut ignorer le contenu de StructuredDocumentTag. La valeur par défaut est false en C++."
type: docs
weight: 12000
url: /fr/cpp/aspose.words.replacing/findreplaceoptions/get_ignorestructureddocumenttags/
---
## FindReplaceOptions::get_IgnoreStructuredDocumentTags method


Obtient ou définit une valeur booléenne indiquant s'il faut ignorer le contenu de [StructuredDocumentTag](../../../aspose.words.markup/structureddocumenttag/). La valeur par défaut est **false**.

```cpp
bool Aspose::Words::Replacing::FindReplaceOptions::get_IgnoreStructuredDocumentTags() const
```

## Remarques


Lorsque cette option est définie sur **true**, le contenu de [StructuredDocumentTag](../../../aspose.words.markup/structureddocumenttag/) sera traité comme un texte simple.

Sinon, [StructuredDocumentTag](../../../aspose.words.markup/structureddocumenttag/) sera traité comme un [Story](../../../aspose.words/story/) autonome et le modèle de remplacement sera recherché séparément pour chaque [StructuredDocumentTag](../../../aspose.words.markup/structureddocumenttag/), de sorte que si le modèle traverse un [StructuredDocumentTag](../../../aspose.words.markup/structureddocumenttag/), le remplacement ne sera pas effectué pour ce modèle.

## Exemples



Montre comment ignorer le contenu des balises lors du remplacement.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Structured document tags.docx");

// Ce paragraphe contient un SDT.
auto p = System::ExplicitCast<Aspose::Words::Paragraph>(doc->get_FirstSection()->get_Body()->GetChild(Aspose::Words::NodeType::Paragraph, 2, true));
System::String textToSearch = p->ToString(Aspose::Words::SaveFormat::Text).Trim();

auto options = System::MakeObject<Aspose::Words::Replacing::FindReplaceOptions>();
options->set_IgnoreStructuredDocumentTags(true);
doc->get_Range()->Replace(textToSearch, u"replacement", options);

doc->Save(get_ArtifactsDir() + u"StructuredDocumentTag.IgnoreStructuredDocumentTags.docx");
```

## Voir aussi

* Class [FindReplaceOptions](../)
* Namespace [Aspose::Words::Replacing](../../)
* Library [Aspose.Words for C++](../../../)
