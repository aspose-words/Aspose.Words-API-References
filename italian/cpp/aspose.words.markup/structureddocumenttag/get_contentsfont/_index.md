---
title: "Metodo Aspose::Words::Markup::StructuredDocumentTag::get_ContentsFont"
linktitle: "get_ContentsFont"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::Markup::StructuredDocumentTag::get_ContentsFont. Formattazione del carattere che verrà applicata al testo inserito in SDT in C++."
type: docs
weight: 11000
url: /it/cpp/aspose.words.markup/structureddocumenttag/get_contentsfont/
---
## StructuredDocumentTag::get_ContentsFont method


[Font](../../../aspose.words/font/) formatting that will be applied to text entered into **SDT**.

```cpp
System::SharedPtr<Aspose::Words::Font> Aspose::Words::Markup::StructuredDocumentTag::get_ContentsFont()
```


## Esempi



Mostra come creare un tag di documento strutturato in una casella di testo semplice e modificarne l'aspetto.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Crea un tag di documento strutturato che conterrà testo semplice.
auto tag = System::MakeObject<Aspose::Words::Markup::StructuredDocumentTag>(doc, Aspose::Words::Markup::SdtType::PlainText, Aspose::Words::Markup::MarkupLevel::Inline);

// Imposta il titolo e il colore del riquadro che appare quando si passa il mouse sul tag di documento strutturato in Microsoft Word.
tag->set_Title(u"My plain text");
tag->set_Color(System::Drawing::Color::get_Magenta());

// Imposta un tag per questo tag di documento strutturato, che è ottenibile
// come un elemento XML chiamato "tag", con la stringa sottostante nel suo attributo "@val".
tag->set_Tag(u"MyPlainTextSDT");

// Ogni tag di documento strutturato ha un ID unico casuale.
ASSERT_TRUE(tag->get_Id() > 0);

// Imposta il carattere per il testo all'interno del tag di documento strutturato.
tag->get_ContentsFont()->set_Name(u"Arial");

// Imposta il carattere per il testo alla fine del tag di documento strutturato.
// Qualsiasi testo digitato nel corpo del documento dopo aver lasciato il tag con i tasti freccia utilizzerà questo carattere.
tag->get_EndCharacterFont()->set_Name(u"Arial Black");

// Per impostazione predefinita, è false e premere invio mentre si è all'interno di un tag di documento strutturato non produce alcun effetto.
// Quando impostato su true, il nostro tag di documento strutturato può contenere più righe.

// Imposta la proprietà "Multiline" su "false" per consentire solo il contenuto
// di questo tag di documento strutturato di occupare una sola riga.
// Imposta la proprietà "Multiline" su "true" per consentire al tag di contenere più righe di contenuto.
tag->set_Multiline(true);

// Imposta la proprietà "Appearance" su "SdtAppearance.Tags" per mostrare i tag attorno al contenuto.
// Per impostazione predefinita il tag di documento strutturato viene visualizzato come BoundingBox.
tag->set_Appearance(Aspose::Words::Markup::SdtAppearance::Tags);

auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->InsertNode(tag);

// Inserisci una copia del nostro tag di documento strutturato in un nuovo paragrafo.
auto tagClone = System::ExplicitCast<Aspose::Words::Markup::StructuredDocumentTag>(System::ExplicitCast<Aspose::Words::Node>(tag)->Clone(true));
builder->InsertParagraph();
builder->InsertNode(tagClone);

// Usa il metodo "RemoveSelfOnly" per rimuovere un tag di documento strutturato, mantenendo i suoi contenuti nel documento.
tagClone->RemoveSelfOnly();

doc->Save(get_ArtifactsDir() + u"StructuredDocumentTag.PlainText.docx");
```

## Vedi anche

* Class [Font](../../../aspose.words/font/)
* Class [StructuredDocumentTag](../)
* Namespace [Aspose::Words::Markup](../../)
* Library [Aspose.Words for C++](../../../)
