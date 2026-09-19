---
title: "Aspose::Words::Markup::StructuredDocumentTag::get_Id method"
linktitle: "get_Id"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::Markup::StructuredDocumentTag::get_Id. Specifica un Id numerico unico, di sola lettura e persistente per questo SDT in C++."
type: docs
weight: 17000
url: /it/cpp/aspose.words.markup/structureddocumenttag/get_id/
---
## StructuredDocumentTag::get_Id method


Specifica un Id numerico persistente univoco di sola lettura per questo **SDT**.

```cpp
int32_t Aspose::Words::Markup::StructuredDocumentTag::get_Id() override
```

## Note


L'attributo Id deve seguire queste regole:* Il documento deve conservare gli Id SDT solo se l'intero documento è clonato [Clone](../../../aspose.words/document/clone/).
* During [ImportNode()](../) Id shall be retained if import does not cause conflicts with other SDT Ids in the target document.
* If multiple SDT nodes specify the same decimal number value for the Id attribute, then the first SDT in the document shall maintain this original Id, and all subsequent SDT nodes shall have new identifiers assigned to them when the document is loaded.
* During standalone SDT [Clone()](../) operation new unique ID will be generated for the cloned SDT node.
* If Id is not specified in the source document, then the SDT node shall have a new unique identifier assigned to it when the document is loaded.



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

* Class [StructuredDocumentTag](../)
* Namespace [Aspose::Words::Markup](../../)
* Library [Aspose.Words for C++](../../../)
