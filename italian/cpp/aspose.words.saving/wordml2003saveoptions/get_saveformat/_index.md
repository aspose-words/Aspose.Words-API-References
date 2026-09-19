---
title: "Metodo get_SaveFormat della classe Aspose::Words::Saving::WordML2003SaveOptions."
linktitle: "get_SaveFormat"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo get_SaveFormat della classe Aspose::Words::Saving::WordML2003SaveOptions. Specifica il formato in cui il documento verrà salvato se questo oggetto di opzioni di salvataggio viene utilizzato. Può essere solo WordML in C++."
type: docs
weight: 2000
url: /it/cpp/aspose.words.saving/wordml2003saveoptions/get_saveformat/
---
## WordML2003SaveOptions::get_SaveFormat method


Specifica il formato in cui il documento verrà salvato se questo oggetto di opzioni di salvataggio viene utilizzato. Può essere solo [WordML](../../../aspose.words/saveformat/).

```cpp
Aspose::Words::SaveFormat Aspose::Words::Saving::WordML2003SaveOptions::get_SaveFormat() override
```


## Esempi



Mostra come gestire il contenuto grezzo del documento di output.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->Writeln(u"Hello world!");

// Crea un oggetto "WordML2003SaveOptions" da passare al metodo "Save" del documento
// per modificare il modo in cui salviamo il documento nel formato di salvataggio WordML.
auto options = System::MakeObject<Aspose::Words::Saving::WordML2003SaveOptions>();

ASSERT_EQ(Aspose::Words::SaveFormat::WordML, options->get_SaveFormat());

// Imposta la proprietà "PrettyFormat" su "true" per applicare l'indentazione con carattere tabulazione e
// nuove linee per rendere il contenuto grezzo del documento di output più leggibile.
// Imposta la proprietà "PrettyFormat" su "false" per salvare il contenuto grezzo del documento in un unico blocco continuo di testo.
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

## Vedi anche

* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [WordML2003SaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
