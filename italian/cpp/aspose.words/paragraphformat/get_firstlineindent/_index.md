---
title: "Metodo Aspose::Words::ParagraphFormat::get_FirstLineIndent"
linktitle: "get_FirstLineIndent"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::ParagraphFormat::get_FirstLineIndent. Ottiene o imposta il valore (in punti) per un rientro della prima linea o sospeso. Usa valori positivi per impostare il rientro della prima linea e valori negativi per impostare il rientro sospeso in C++."
type: docs
weight: 13000
url: /it/cpp/aspose.words/paragraphformat/get_firstlineindent/
---
## ParagraphFormat::get_FirstLineIndent method


Ottiene o imposta il valore (in punti) per un rientro della prima riga o sospeso. Usa valori positivi per impostare il rientro della prima riga e valori negativi per impostare il rientro sospeso.

```cpp
double Aspose::Words::ParagraphFormat::get_FirstLineIndent()
```


## Esempi



Mostra come inserire un paragrafo nel documento.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Font> font = builder->get_Font();
font->set_Size(16);
font->set_Bold(true);
font->set_Color(System::Drawing::Color::get_Blue());
font->set_Name(u"Arial");
font->set_Underline(Aspose::Words::Underline::Dash);

System::SharedPtr<Aspose::Words::ParagraphFormat> paragraphFormat = builder->get_ParagraphFormat();
paragraphFormat->set_FirstLineIndent(8);
paragraphFormat->set_Alignment(Aspose::Words::ParagraphAlignment::Justify);
paragraphFormat->set_AddSpaceBetweenFarEastAndAlpha(true);
paragraphFormat->set_AddSpaceBetweenFarEastAndDigit(true);
paragraphFormat->set_KeepTogether(true);

// Il metodo "Writeln" termina il paragrafo dopo aver aggiunto il testo
// e poi avvia una nuova riga, aggiungendo un nuovo paragrafo.
builder->Writeln(u"Hello world!");

ASSERT_TRUE(builder->get_CurrentParagraph()->get_IsEndOfDocument());
```

## Vedi anche

* Class [ParagraphFormat](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
