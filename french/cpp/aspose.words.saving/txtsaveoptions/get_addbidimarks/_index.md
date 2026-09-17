---
title: "Aspose::Words::Saving::TxtSaveOptions::get_AddBidiMarks method"
linktitle: "get_AddBidiMarks"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Saving::TxtSaveOptions::get_AddBidiMarks method. Spécifie s'il faut ajouter des marques bidirectionnelles avant chaque exécution BiDi lors de l'exportation au format texte brut. La valeur par défaut est false en C++."
type: docs
weight: 3000
url: /fr/cpp/aspose.words.saving/txtsaveoptions/get_addbidimarks/
---
## TxtSaveOptions::get_AddBidiMarks method


Spécifie s'il faut ajouter des marques bidirectionnelles avant chaque séquence BiDi lors de l'exportation au format texte brut. La valeur par défaut est **false**.

```cpp
bool Aspose::Words::Saving::TxtSaveOptions::get_AddBidiMarks() const
```


## Exemples



Montre comment insérer le caractère Unicode 'RIGHT-TO-LEFT MARK' (U+200F) avant chaque [Run](../../../aspose.words/run/) bidirectionnel dans le texte.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln(u"Hello world!");
builder->get_ParagraphFormat()->set_Bidi(true);
builder->Writeln(u"שלום עולם!");
builder->Writeln(u"مرحبا بالعالم!");

// Créez un objet "TxtSaveOptions" que nous pouvons passer à la méthode "Save" du document
// pour modifier la façon dont nous enregistrons le document en texte brut.
auto saveOptions = System::MakeObject<Aspose::Words::Saving::TxtSaveOptions>();
saveOptions->set_Encoding(System::Text::Encoding::get_Unicode());

// Définissez la propriété "AddBidiMarks" sur "true" pour ajouter des marques avant les exécutions
// avec du texte de droite à gauche afin d'indiquer ce fait.
// Définissez la propriété "AddBidiMarks" sur "false" pour écrire tout le texte de gauche à droite
// et de droite à gauche de manière égale sans rien indiquer lequel est lequel.
saveOptions->set_AddBidiMarks(addBidiMarks);

doc->Save(get_ArtifactsDir() + u"TxtSaveOptions.AddBidiMarks.txt", saveOptions);

System::String docText = System::Text::Encoding::get_Unicode()->GetString(System::IO::File::ReadAllBytes(get_ArtifactsDir() + u"TxtSaveOptions.AddBidiMarks.txt"));

if (addBidiMarks)
{
    ASSERT_EQ(u"\ufeffHello world!‎\r\nשלום עולם!‏\r\nمرحبا بالعالم!‏\r\n\r\n", docText);
    ASSERT_TRUE(docText.Contains(u"\u200f"));
}
else
{
    ASSERT_EQ(u"\ufeffHello world!\r\nשלום עולם!\r\nمرحبا بالعالم!\r\n\r\n", docText);
    ASSERT_FALSE(docText.Contains(u"\u200f"));
}
```

## Voir aussi

* Class [TxtSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
