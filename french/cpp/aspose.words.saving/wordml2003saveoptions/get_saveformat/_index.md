---
title: "Aspose::Words::Saving::WordML2003SaveOptions::get_SaveFormat méthode"
linktitle: "get_SaveFormat"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Saving::WordML2003SaveOptions::get_SaveFormat méthode. Spécifie le format dans lequel le document sera enregistré si cet objet d'options d'enregistrement est utilisé. Peut uniquement être WordML en C++."
type: docs
weight: 2000
url: /fr/cpp/aspose.words.saving/wordml2003saveoptions/get_saveformat/
---
## WordML2003SaveOptions::get_SaveFormat method


Spécifie le format dans lequel le document sera enregistré si cet objet d'options d'enregistrement est utilisé. Peut uniquement être [WordML](../../../aspose.words/saveformat/).

```cpp
Aspose::Words::SaveFormat Aspose::Words::Saving::WordML2003SaveOptions::get_SaveFormat() override
```


## Exemples



Montre comment gérer le contenu brut du document de sortie.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->Writeln(u"Hello world!");

// Créez un objet \"WordML2003SaveOptions\" à transmettre à la méthode \"Save\" du document
// pour modifier la façon dont nous enregistrons le document au format d'enregistrement WordML.
auto options = System::MakeObject<Aspose::Words::Saving::WordML2003SaveOptions>();

ASSERT_EQ(Aspose::Words::SaveFormat::WordML, options->get_SaveFormat());

// Définissez la propriété \"PrettyFormat\" sur \"true\" pour appliquer une indentation avec des caractères de tabulation et
// des sauts de ligne afin de rendre le contenu brut du document de sortie plus lisible.
// Définissez la propriété \"PrettyFormat\" sur \"false\" pour enregistrer le contenu brut du document en un seul bloc continu de texte.
options->set_PrettyFormat(prettyFormat);

doc->Save(get_ArtifactsDir() + u"WordML2003SaveOptions.PrettyFormat.xml", options);

System::String fileContents = System::IO::File::ReadAllText(get_ArtifactsDir() + u"WordML2003SaveOptions.PrettyFormat.xml");
System::String newLine = System::Environment::get_NewLine();
if (prettyFormat)
{
    ASSERT_TRUE(fileContents.Contains(System::String::Format(u"<o:DocumentProperties>{0}\t\t", newLine) + System::String::Format(u"<o:Revision>1</o:Revision>{0}\t\t", newLine) + System::String::Format(u"<o:TotalTime>0</o:TotalTime>{0}\t\t", newLine) + System::String::Format(u"<o:Pages>1</o:Pages>{0}\t\t", newLine) + System::String::Format(u"<o:Words>0</o:Words>{0}\t\t", newLine) + System::String::Format(u"<o:Characters>0</o:Characters>{0}\t\t", newLine) + System::String::Format(u"<o:Lines>1</o:Lines>{0}\t\t", newLine) + System::String::Format(u"<o:Paragraphs>1</o:Paragraphs>{0}\t\t", newLine) + System::String::Format(u"<o:CharactersWithSpaces>0</o:CharactersWithSpaces>{0}\t\t", newLine) + System::String::Format(u"<o:Version>11.5606</o:Version>{0}\t", newLine) + u"</o:DocumentProperties>"));
}
else
{
    ASSERT_TRUE(fileContents.Contains(System::String(u"<o:DocumentProperties><o:Revision>1</o:Revision><o:TotalTime>0</o:TotalTime><o:Pages>1</o:Pages>") + u"<o:Words>0</o:Words><o:Characters>0</o:Characters><o:Lines>1</o:Lines><o:Paragraphs>1</o:Paragraphs>" + u"<o:CharactersWithSpaces>0</o:CharactersWithSpaces><o:Version>11.5606</o:Version></o:DocumentProperties>"));
}
```

## Voir aussi

* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [WordML2003SaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
