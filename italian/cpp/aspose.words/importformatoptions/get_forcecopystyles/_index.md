---
title: "Aspose::Words::ImportFormatOptions::get_ForceCopyStyles metodo"
linktitle: "get_ForceCopyStyles"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::ImportFormatOptions::get_ForceCopyStyles metodo. Ottiene o imposta un valore booleano che indica se copiare gli stili in conflitto nella modalità KeepSourceFormatting. Il valore predefinito è false in C++."
type: docs
weight: 4000
url: /it/cpp/aspose.words/importformatoptions/get_forcecopystyles/
---
## ImportFormatOptions::get_ForceCopyStyles method


Ottiene o imposta un valore booleano che indica se copiare gli stili in conflitto nella modalità [KeepSourceFormatting](../../importformatmode/). Il valore predefinito è **false**.

```cpp
bool Aspose::Words::ImportFormatOptions::get_ForceCopyStyles() const
```

## Note


Per impostazione predefinita, se uno stile corrispondente esiste già in un documento di destinazione, la formattazione dello stile di origine viene espansa in attributi di nodo diretti e lo stile di questo nodo viene ripristinato al valore predefinito.

Quando questa opzione è impostata su **true**, lo stile di origine verrà copiato forzatamente nel documento di destinazione con un nome univoco e applicato al nodo importato.

Nota, in questo caso non è garantito che la formattazione del nodo importato nel documento di destinazione venga preservata.

## Esempi



Mostra come copiare forzatamente gli stili di origine con nomi univoci.
```cpp
// Entrambi i documenti contengono MyStyle1 e MyStyle2, MyStyle3 esiste solo in un documento di origine.
auto srcDoc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Styles source.docx");
auto dstDoc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Styles destination.docx");

auto options = System::MakeObject<Aspose::Words::ImportFormatOptions>();
options->set_ForceCopyStyles(true);
dstDoc->AppendDocument(srcDoc, Aspose::Words::ImportFormatMode::KeepSourceFormatting, options);

System::SharedPtr<Aspose::Words::ParagraphCollection> paras = dstDoc->get_Sections()->idx_get(1)->get_Body()->get_Paragraphs();

ASSERT_EQ(paras->idx_get(0)->get_ParagraphFormat()->get_Style()->get_Name(), u"MyStyle1_0");
ASSERT_EQ(paras->idx_get(1)->get_ParagraphFormat()->get_Style()->get_Name(), u"MyStyle2_0");
ASSERT_EQ(paras->idx_get(2)->get_ParagraphFormat()->get_Style()->get_Name(), u"MyStyle3");
```

## Vedi anche

* Class [ImportFormatOptions](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
