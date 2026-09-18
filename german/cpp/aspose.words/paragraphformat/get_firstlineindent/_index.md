---
title: "Aspose::Words::ParagraphFormat::get_FirstLineIndent‑Methode"
linktitle: "get_FirstLineIndent"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::ParagraphFormat::get_FirstLineIndent‑Methode. Gibt den Wert (in Punkten) für einen Erstzeileneinzug oder hängenden Einzug zurück oder setzt ihn. Verwenden Sie positive Werte, um den Erstzeileneinzug festzulegen, und negative Werte, um den hängenden Einzug in C++ festzulegen."
type: docs
weight: 13000
url: /de/cpp/aspose.words/paragraphformat/get_firstlineindent/
---
## ParagraphFormat::get_FirstLineIndent method


Liest oder legt den Wert (in Punkten) für einen Erstzeileneinzug oder hängenden Einzug fest. Verwenden Sie positive Werte, um den Erstzeileneinzug festzulegen, und negative Werte, um den hängenden Einzug festzulegen.

```cpp
double Aspose::Words::ParagraphFormat::get_FirstLineIndent()
```


## Beispiele



Zeigt, wie man einen Absatz in das Dokument einfügt.
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

// Die Methode "Writeln" beendet den Absatz nach dem Anhängen von Text
// und startet dann eine neue Zeile, wodurch ein neuer Absatz hinzugefügt wird.
builder->Writeln(u"Hello world!");

ASSERT_TRUE(builder->get_CurrentParagraph()->get_IsEndOfDocument());
```

## Siehe auch

* Class [ParagraphFormat](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
